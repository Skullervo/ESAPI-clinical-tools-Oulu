# ESAPI Clinical Tools - Oulu

A professional collection of Eclipse ESAPI scripts for clinical radiotherapy workflows, developed for hospital use.

## ⚠️ Clinical Safety Notice

**CRITICAL - READ BEFORE USE**

This software is provided as-is for research and development purposes. These tools are intended to **ASSIST** clinical workflows but **DO NOT** replace professional medical judgment, manual verification, or institutional quality assurance procedures.

**Important Safety Requirements:**
- ✅ All scripts must be thoroughly validated at your institution before clinical use
- ✅ Independent verification by qualified medical physics staff is required
- ✅ Scripts must be reviewed and approved according to your institutional policies
- ✅ Regular audits and validation testing must be performed
- ✅ All treatment plans must receive final approval by authorized personnel
- ⛔ Never use scripts clinically without proper validation and approval
- ⛔ Never bypass institutional safety procedures or manual review requirements
- ⛔ Never assume scripts are error-free or suitable for your specific clinical environment

**User Responsibility:**
By using this software, you accept full responsibility for validation, testing, and verification in your clinical environment. The authors and contributors assume no liability for clinical use.
These scripts have not been certified or approved as a medical device under any regulatory framework.

## 📋 Validation Disclaimer

**NO WARRANTY - VALIDATION REQUIRED**

This software is provided under the MIT License with **ABSOLUTELY NO WARRANTY**. 

**You are solely responsible for:**
- Validating all scripts for accuracy and suitability in your clinical environment
- Performing comprehensive testing before any clinical use
- Ensuring compliance with local regulations and standards (FDA, IEC, national requirements)
- Maintaining documentation of validation testing
- Training staff on proper usage and limitations
- Implementing appropriate error handling and safety checks
- Monitoring for software updates and security issues

**Regulatory Compliance:**
Users must ensure compliance with all applicable regulatory requirements including but not limited to:
- FDA regulations (US)
- IEC 62304 (Medical Device Software)
- Local/national medical device regulations
- Institutional IRB/ethics requirements for research use
- Data protection regulations (HIPAA, GDPR, etc.)

## 📁 Repository Structure

```
ESAPI-clinical-tools-Oulu/
├── src/
│   ├── Common/              # Shared utilities and helper classes
│   └── Scripts/
│       ├── PlanChecks/      # Automated plan validation scripts
│       ├── QA/              # Quality assurance automation
│       ├── Reporting/       # Clinical reports and data export
│       └── Automation/      # Workflow automation tools
├── docs/                    # Documentation and guides
├── examples/                # Example scripts and templates
├── LICENSE                  # MIT License
└── README.md               # This file
```

## 🚀 Installation

### Prerequisites

**Required:**
- Varian Eclipse Treatment Planning System (TPS) with ESAPI enabled
- Eclipse API version: 15.6 or later (recommended)
- Visual Studio 2019 or later
- .NET Framework 4.8 or later
- Varian ESAPI DLLs (obtained from Varian, not included in this repository)

**Recommended:**
- C# development experience
- Understanding of radiotherapy treatment planning
- Familiarity with Eclipse TPS workflow

### Setup Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Skullervo/ESAPI-clinical-tools-Oulu.git
   cd ESAPI-clinical-tools-Oulu
   ```

2. **Obtain Varian ESAPI DLLs**
   - Contact Varian to obtain the ESAPI libraries
   - These are proprietary and **NOT** included in this repository
   - Typically located in: `C:\Program Files (x86)\Varian\RTM\<version>\esapi\`
   - Required DLLs include:
     - VMS.TPS.Common.Model.API.dll
     - VMS.TPS.Common.Model.Types.dll
     - Additional dependencies as needed

3. **Configure Your Project**
   - Open your script project in Visual Studio
   - Add references to the Varian ESAPI DLLs
   - Set "Copy Local" to False for ESAPI references
   - Configure build output directory according to Eclipse requirements

4. **Review and Customize**
   - Review all code before use
   - Customize scripts to match your institutional protocols
   - Update hard-coded values, file paths, and configuration
   - Implement institutional-specific validation rules

## 📖 Usage

### General Workflow

1. **Select Appropriate Script**
   - Browse the `src/Scripts/` folders for relevant functionality
   - Review the script documentation and purpose
   - Check the example implementations

2. **Customize for Your Institution**
   - Modify configuration values
   - Update dose constraints and protocols
   - Adjust output formats and paths
   - Add institution-specific checks

3. **Validation Testing**
   - Test with phantom data first
   - Perform comprehensive validation with clinical test cases
   - Document all validation results
   - Obtain required approvals

4. **Clinical Deployment**
   - Deploy through your institution's IT and medical physics approval process
   - Train users on proper usage
   - Implement monitoring and error reporting
   - Schedule regular re-validation

### Running Scripts

**Binary Plugin Scripts:**
```csharp
// Scripts are typically executed from within Eclipse
// through the Scripts menu or External Beam Planning
```

**Standalone Applications:**
```csharp
// Configure ESAPI context and patient information
// Run as external application with appropriate credentials
```

See the `examples/` folder for specific implementation patterns.

## 🔧 Compatibility

### Varian Eclipse Versions
- **Tested with:** Eclipse 15.6, 16.1
- **Recommended:** Eclipse 16.1 or later
- **Note:** API compatibility may vary between versions

### ESAPI Versions
- **Target:** ESAPI 15.6+
- **API Mode:** Binary Plugin and Standalone supported
- **Legacy Support:** May require modifications for older versions

### .NET Framework
- **Minimum:** .NET Framework 4.6.1
- **Recommended:** .NET Framework 4.8
- **Future:** .NET Core support under consideration

### Operating System
- **Required:** Windows 10 or Windows Server 2016+
- **Architecture:** x64
- **Note:** Must match Eclipse TPS server environment

### Clinical Environment
- **Deployment:** Hospital network with Eclipse TPS access
- **Permissions:** Appropriate ARIA/Eclipse user credentials
- **Network:** Access to Eclipse database and file systems
- **Security:** Compliance with institutional IT security policies

## 🤝 Contributing

Contributions are welcome! Please:
1. Fork the repository
2. Create a feature branch
3. Follow C# coding standards
4. Include clear documentation
5. Add appropriate safety notices
6. Submit a pull request

**Important:** Never commit:
- Varian proprietary DLLs
- Patient data or PHI
- Institutional credentials
- Licensed/proprietary content

## 📚 Resources

- [Eclipse ESAPI Documentation](https://varianapis.github.io/)
- [Varian Developer Portal](https://developer.varian.com/)
- [ESAPI GitHub Community](https://github.com/VarianAPIs)
- [Clinical ESAPI Scripts Community](https://github.com/topics/esapi)

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

**Summary:** Free to use, modify, and distribute with attribution. Provided without warranty.

## ⚖️ Liability and Use

**THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED.**

Users assume all risks and responsibilities for:
- Clinical validation and testing
- Regulatory compliance
- Patient safety
- Data security and privacy
- Professional liability

## 📞 Support

This is a community project. For support:
- Open an issue on GitHub
- Review existing documentation
- Consult with your medical physics team
- Contact Varian for ESAPI-specific questions

## 🏥 Institutional Use

Before deploying in your institution:
- [ ] Complete comprehensive validation testing
- [ ] Document all test results and validation protocols
- [ ] Obtain medical physics approval
- [ ] Obtain IT security approval
- [ ] Obtain radiation oncology approval
- [ ] Train all users thoroughly
- [ ] Implement error reporting procedures
- [ ] Schedule regular re-validation
- [ ] Maintain version control and change logs

---

**Developed for the radiotherapy medical physics community**

**Always prioritize patient safety in clinical applications.**
