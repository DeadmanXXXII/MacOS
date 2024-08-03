# MacOS

Here’s a comprehensive list of macOS commands.

# macOS Commands

## System Information

- **Check macOS version:**
  ```bash
  sw_vers
  ```

- **Get detailed system information:**
  ```bash
  system_profiler
  ```

- **Check hardware details:**
  ```bash
  system_profiler SPHardwareDataType
  ```

- **List all installed applications:**
  ```bash
  ls /Applications
  ```

- **Check for available software updates:**
  ```bash
  softwareupdate --list
  ```

- **Apply available software updates:**
  ```bash
  sudo softwareupdate --install --all
  ```

## Package Management (Homebrew)

- **Install Homebrew (if not installed):**
  ```bash
  /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
  ```

- **Update Homebrew:**
  ```bash
  brew update
  ```

- **Upgrade Homebrew packages:**
  ```bash
  brew upgrade
  ```

- **Install a package:**
  ```bash
  brew install packagename
  ```

- **List installed packages:**
  ```bash
  brew list
  ```

- **Remove a package:**
  ```bash
  brew uninstall packagename
  ```

- **Search for a package:**
  ```bash
  brew search packagename
  ```

## File and Directory Management

- **List files and directories:**
  ```bash
  ls
  ```

- **Change directory:**
  ```bash
  cd directoryname
  ```

- **Create a directory:**
  ```bash
  mkdir directoryname
  ```

- **Remove a directory:**
  ```bash
  rmdir directoryname
  ```

- **Copy files:**
  ```bash
  cp sourcefile destinationfile
  ```

- **Move files:**
  ```bash
  mv sourcefile destinationfile
  ```

- **Delete files:**
  ```bash
  rm filename
  ```

- **Find files:**
  ```bash
  find /path/to/search -name "filename"
  ```

- **Search for text within files:**
  ```bash
  grep "searchtext" filename
  ```

## System Monitoring and Management

- **Check disk usage:**
  ```bash
  df -h
  ```

- **Check disk space usage by directory:**
  ```bash
  du -sh /path/to/directory
  ```

- **List all running processes:**
  ```bash
  ps aux
  ```

- **Monitor system performance:**
  ```bash
  top
  ```

- **View system logs:**
  ```bash
  log show
  ```

- **Check network configuration:**
  ```bash
  ifconfig
  ```

- **List all network interfaces:**
  ```bash
  networksetup -listallhardwareports
  ```

- **Flush DNS cache:**
  ```bash
  sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder
  ```

## User and Permissions Management

- **List all users:**
  ```bash
  dscl . -list /Users
  ```

- **Add a new user:**
  ```bash
  sudo dscl . -create /Users/username
  sudo dscl . -create /Users/username UserShell /bin/bash
  sudo dscl . -create /Users/username RealName "Full Name"
  sudo dscl . -create /Users/username UniqueID "1001"
  sudo dscl . -create /Users/username PrimaryGroupID 20
  sudo dscl . -create /Users/username NFSHomeDirectory /Users/username
  sudo passwd username
  ```

- **Delete a user:**
  ```bash
  sudo dscl . -delete /Users/username
  ```

- **Change file permissions:**
  ```bash
  chmod permissions filename
  ```

- **Change file ownership:**
  ```bash
  chown owner:group filename
  ```

## System Maintenance

- **Run disk repair:**
  ```bash
  diskutil repairDisk /dev/disk0
  ```

- **Verify disk structure:**
  ```bash
  diskutil verifyVolume /
  ```

- **Repair disk permissions (for macOS versions before El Capitan):**
  ```bash
  sudo diskutil repairPermissions /
  ```

- **Check system status and health:**
  ```bash
  sudo spindump
  ```

- **Rebuild Spotlight index:**
  ```bash
  sudo mdutil -E /
  ```

## Networking

- **Ping a host:**
  ```bash
  ping hostname
  ```

- **Trace route to a host:**
  ```bash
  traceroute hostname
  ```

- **Open network ports:**
  ```bash
  sudo pfctl -e
  sudo pfctl -f /etc/pf.conf
  ```

## Security

- **Check for open ports:**
  ```bash
  lsof -i -P
  ```

- **Manage firewall rules:**
  ```bash
  sudo /usr/libexec/ApplicationFirewall/socketfilterfw --listapps
  ```

- **Enable firewall:**
  ```bash
  sudo /usr/libexec/ApplicationFirewall/socketfilterfw --setglobalstate on
  ```

- **Disable firewall:**
  ```bash
  sudo /usr/libexec/ApplicationFirewall/socketfilterfw --setglobalstate off
  ```

## Miscellaneous

- **Generate a system report:**
  ```bash
  system_profiler SPSoftwareDataType
  ```

- **Update macOS via Terminal:**
  ```bash
  softwareupdate --install --all
  ```

This list provides a broad range of macOS commands for managing and troubleshooting your system. These commands cover everything from basic file operations to advanced system configuration and maintenance.
