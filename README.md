# WD-BossMenu

![WD-BossMenu Preview](https://cdn.discordapp.com/attachments/1377513657738596503/1378242035362037852/2025-05-31_08-16-11.mp4?ex=683be36b&is=683a91eb&hm=3825f5eb8bac824defc8dfe98e2bb5bd7ab5de0e10ea23878594bf4d47f06072&)

## Overview

WD-BossMenu is a comprehensive job management system for FiveM servers using the QBCore framework. This resource provides a modern, feature-rich interface for job bosses to manage their employees, finances, and job applications.

## Features

- **Modern UI Design**: Clean, responsive interface with dark mode support
- **Employee Management**: Hire, fire, promote, and manage employee permissions
- **Financial System**: Track society funds, manage transactions, and pay employees
- **Job Application System**: Customizable application forms for each job
- **Activity Tracking**: Monitor employee activity and playtime
- **Multi-Location Support**: Configure multiple management points for each job
- **Compatibility**: Works with multiple banking systems (qb-banking, wd-banking, renewed-banking)
- **Target System Integration**: Compatible with qb-target and ox_target
- **Customizable Settings**: Personalize the interface with themes and preferences

## Demo

[Watch Demo Video]( https://cdn.discordapp.com/attachments/1377513657738596503/1378242035362037852/2025-05-31_08-16-11.mp4?ex=683be36b&is=683a91eb&hm=3825f5eb8bac824defc8dfe98e2bb5bd7ab5de0e10ea23878594bf4d47f06072& )

## Dependencies

- [qb-core](https://github.com/qbcore-framework/qb-core)
- [oxmysql](https://github.com/overextended/oxmysql)
- One of the following banking systems:
  - [qb-banking](https://github.com/qbcore-framework/qb-banking)
  - [wd-banking](https://github.com/YourUsername/wd-banking)
  - [renewed-banking](https://github.com/Renewed-Scripts/Renewed-Banking)
- One of the following target systems:
  - [qb-target](https://github.com/qbcore-framework/qb-target)
  - [ox_target](https://github.com/overextended/ox_target)

## Installation

1. **Download the resource** and place it in your server's resources folder
2. **Import the SQL file** (`bossmenusql.sql`) to your database
3. **Configure the resource** in `config.lua` to match your server's setup
4. **Add to server.cfg**: `ensure wd-bossmenu`

## Configuration

The `config.lua` file allows you to customize various aspects of the resource:

```lua
-- Banking System Selection
Config.BankingSystem = "qb-banking"  -- Options: "wd-banking", "qb-banking", "renewed-banking"

-- Target System Selection
Config.TargetSystem = "qb-target"  -- Options: "qb-target", "ox_target"

-- Job Application System Settings
Config.EnableApplicationSystem = true  -- Set to false to disable job application system
```

### Adding Job Locations

You can add management points for each job in the config:

```lua
Config.Locations = {
    ["police"] = {
        label = "Police Department",
        logoImage = "police.png",
        locations = {
            {
                coords = vector3(433.86, -983.08, 31.02),
                width = 1.0,
                length = 1.0,
                heading = 0,
                minZ = 30.0,
                maxZ = 31.0,
            }
        }
    }
}
```

### Customizing Application Forms

Create custom application forms for each job:

```lua
Config.ApplicationQuestions = {
    ["police"] = {
        {
            question = "Why do you want to join the Police Department?",
            type = "text",
            required = true,
            min = 1,
            max = 1024
        }
    }
}
```

## Features Explained

### Employee Management
- View all employees with their information
- Promote/demote employees to different job grades
- Fire employees
- Assign custom permissions to employees

### Society Funds
- View current society balance
- Deposit/withdraw funds
- View transaction history
- Pay employees directly from society funds

### Job Applications
- Customizable application forms for each job
- Review and manage incoming applications
- Accept or reject applicants with feedback

### Activity Tracking
- Monitor employee activity and playtime
- Track last login times
- View employee performance metrics

## Permissions System

The resource includes a detailed permissions system allowing job bosses to grant specific permissions to employees:

- `hire` - Permission to hire new employees
- `fire` - Permission to fire employees
- `promote` - Permission to promote/demote employees
- `funds` - Permission to manage society funds
- `applications` - Permission to review job applications

## Credits

- Developed by: DaniWorld
- UI Design: AlphaDev
- Special thanks to the QBCore community

## License

This resource is protected under copyright law. All rights reserved to AlphaDev.

## Support

For support, join our Discord: [Your Discord Link]

---

© 2025 AlphaDev. All Rights Reserved.
