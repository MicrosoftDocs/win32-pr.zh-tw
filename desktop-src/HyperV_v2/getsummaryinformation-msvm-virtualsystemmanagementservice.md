---
description: 傳回虛擬機器摘要資訊。
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Msvm_VirtualSystemManagementService 類別的 GetSummaryInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1399acd40f768fdb857d6a4a26e80a52d29111b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318096"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 GetSummaryInformation 方法 \_

傳回虛擬機器摘要資訊。

## <a name="syntax"></a>語法


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SettingData* \[在\]
</dt> <dd>

類型： **CIM \_ VirtualSystemSettingData \[ \]**

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))實例的陣列，可指定要抓取資訊的虛擬機器或快照集。 如果此參數為 **Null**，則會取出所有虛擬機器的資訊。

</dd> <dt>

*RequestedInformation* \[在\]
</dt> <dd>

類型： **uint32 \[ \]**

列舉值的陣列，這些值會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md) 類別中的屬性，以指定要針對在 *SettingData* 陣列中指定的虛擬機器和快照集取得的資料。

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**名稱** (0) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **Name** 屬性。

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**元素名稱** (1) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ElementName** 屬性。

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**建立時間** (2) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **CreationTime** 屬性。

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**附注** (3) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **Notes** 屬性。

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**處理器數目** (4) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **NumberOfProcessors** 屬性。

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**小型縮圖影像 (80x60)** (5) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ThumbnailImage** 屬性。 將會取出維度為 80 60 的縮圖影像。

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**中縮圖影像 (160x120)** (6) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ThumbnailImage** 屬性。 將會取出維度為 160 120 的縮圖影像。

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**大型縮圖影像 (320x240)** (7) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ThumbnailImage** 屬性。 將會取出維度為 320 240 的縮圖影像。

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **AllocatedGPU** 屬性。

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9) 


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**版本** (10) 


</dt> <dd>

> [!Note]  
> 在 Windows 10 和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**受防護** 的 (11) 


</dt> <dd>

> [!Note]  
> 已在 Windows 10、1703版和 Windows Server 2016 中新增。

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **EnabledState** 屬性。

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ProcessorLoad** 屬性。

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ProcessorLoadHistory** 屬性。

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **MemoryUsage** 屬性。

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**心跳** (104) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 [**心跳**] 屬性。

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**執行時間** (105) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **執行時間** 屬性。

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **GuestOperatingSystem** 屬性。

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span> (107) 的 **快照** 集


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **快照** 集屬性。

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **AsynchronousTasks** 屬性。

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **HealthState** 屬性。

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110) 


</dt> <dd>

這會對應到 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **OperationalStatus** 屬性。

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **StatusDescriptions** 屬性。

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **MemoryAvailable** 屬性。

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **AvailableMemoryBuffer** 屬性。

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>複寫 **模式** (114) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ReplicationMode** 屬性。

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>複寫 **狀態** (115) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ReplicationState** 屬性。

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **ReplicationHealth** 屬性。

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**應用程式健全狀況** (117) 


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118) 


</dt> <dd>

這會對應至 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationState** 屬性。 這是跨主要和延伸關聯性的所有複寫狀態值的陣列。 0索引值一律適用于主要關聯性，如果已啟用延伸複寫，則會在索引1中傳回。

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119) 


</dt> <dd>

這會對應至 [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md)類別的 **ReplicationHealth** 屬性。 這是跨主要和延伸關聯性的所有複寫健全狀況值的陣列。 0索引值一律適用于主要關聯性，如果已啟用延伸複寫，則會在索引1中傳回。

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **SwapFilesInUse** 屬性。

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121) 


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122) 


</dt> <dd>

這會對應到 [**Msvm \_ ReplicationProvider**](msvm-replicationprovider.md)類別的 **Name** 屬性。

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123) 


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **IntegrationServicesVersionState** 屬性。

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132) 


</dt> <dd>

這會對應至 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)類別的 **OtherEnabledState** 屬性。

</dd> <dt>



  (133) 


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[擴展\]
</dt> <dd>

類型： **[ **Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)實例的陣列，其中包含在 *SettingData* 陣列中指定的虛擬機器和/或快照集所要求的資訊。 此陣列的元素數會與 *SettingData* 陣列相同。 這些專案中的每一個都會包含 **Name** 屬性，即使沒有要求這個屬性也是一樣。 如果找不到虛擬機器或快照集，或無法使用，則對應摘要資訊專案的 [ **名稱** ] 屬性會是空的。

未在 *RequestedInformation* 參數中指定的屬性會有 **Null** 值。

> [!Note]  
> 從 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)的1703版 Windows 10 中更新的資料類型。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **uint32**

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

## <a name="remarks"></a>備註

存取 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

下列 c # 範例會顯示摘要資訊。 您可以在 [虛擬化範例 (V2) 的一般公用程式 ](common-utilities-for-the-virtualization-samples-v2.md)中找到參考的公用程式。

> [!IMPORTANT]
> 若要正常運作，必須在虛擬機器主機伺服器上執行下列程式碼，且必須以系統管理員許可權執行。

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

