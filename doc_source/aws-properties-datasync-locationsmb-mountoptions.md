# AWS::DataSync::LocationSMB MountOptions<a name="aws-properties-datasync-locationsmb-mountoptions"></a>

Specifies the version of the SMB protocol that DataSync uses to access your SMB file server\.

## Syntax<a name="aws-properties-datasync-locationsmb-mountoptions-syntax"></a>

To declare this entity in your AWS CloudFormation template, use the following syntax:

### JSON<a name="aws-properties-datasync-locationsmb-mountoptions-syntax.json"></a>

```
{
  "[Version](#cfn-datasync-locationsmb-mountoptions-version)" : String
}
```

### YAML<a name="aws-properties-datasync-locationsmb-mountoptions-syntax.yaml"></a>

```
  [Version](#cfn-datasync-locationsmb-mountoptions-version): String
```

## Properties<a name="aws-properties-datasync-locationsmb-mountoptions-properties"></a>

`Version`  <a name="cfn-datasync-locationsmb-mountoptions-version"></a>
By default, DataSync automatically chooses an SMB protocol version based on negotiation with your SMB file server\. You also can configure DataSync to use a specific SMB version, but we recommend doing this only if DataSync has trouble negotiating with the SMB file server automatically\.  
These are the following options for configuring the SMB version:  
+  `AUTOMATIC` \(default\): DataSync and the SMB file server negotiate a protocol version that they mutually support\. \(DataSync supports SMB versions 1\.0 and later\.\)

  This is the recommended option\. If you instead choose a specific version that your file server doesn't support, you may get an `Operation Not Supported` error\.
+  `SMB3`: Restricts the protocol negotiation to only SMB version 3\.0\.2\.
+  `SMB2`: Restricts the protocol negotiation to only SMB version 2\.1\.
+  `SMB2_0`: Restricts the protocol negotiation to only SMB version 2\.0\.
+  `SMB1`: Restricts the protocol negotiation to only SMB version 1\.0\.
**Note**  
The `SMB1` option isn't available when [creating an Amazon FSx for NetApp ONTAP location](https://docs.aws.amazon.com/datasync/latest/userguide/API_CreateLocationFsxOntap.html)\.
*Required*: No  
*Type*: String  
*Allowed values*: `AUTOMATIC | SMB1 | SMB2 | SMB2_0 | SMB3`  
*Update requires*: [No interruption](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/using-cfn-updating-stacks-update-behaviors.html#update-no-interrupt)