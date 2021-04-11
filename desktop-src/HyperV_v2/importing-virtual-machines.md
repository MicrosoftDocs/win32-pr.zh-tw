---
description: '下列 c # 範例示範如何使用 MigrateVirtualSystemToHost 方法來執行簡單的虛擬機器遷移。'
ms.assetid: A3E4AAA2-3AE6-4D7D-8D7B-1ED367D398C0
title: 正在遷移虛擬機器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4446830b61e2fabb79d0938520d0b503da167c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691799"
---
# <a name="migrating-virtual-machines"></a><span data-ttu-id="361b9-103">正在遷移虛擬機器</span><span class="sxs-lookup"><span data-stu-id="361b9-103">Migrating virtual machines</span></span>

<span data-ttu-id="361b9-104">下列 c # 範例示範如何使用 [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) 方法來執行簡單的虛擬機器遷移。</span><span class="sxs-lookup"><span data-stu-id="361b9-104">The following C# sample demonstrates how to use the [**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md) method to perform a simple migration of a virtual machine.</span></span> <span data-ttu-id="361b9-105">此範例會使用資源集區來取得正確的 VHD 路徑。</span><span class="sxs-lookup"><span data-stu-id="361b9-105">This example uses resource pools to obtain the correct VHD paths.</span></span> <span data-ttu-id="361b9-106">這段程式碼是從 [hyper-v 虛擬機器遷移範例](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Hyper-V%20virtual%20machine%20migration%20sample)取得。</span><span class="sxs-lookup"><span data-stu-id="361b9-106">This code is taken from the [Hyper-V virtual machine migration sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Hyper-V%20virtual%20machine%20migration%20sample).</span></span>

<span data-ttu-id="361b9-107">執行此範例的命令列語法為：</span><span class="sxs-lookup"><span data-stu-id="361b9-107">The command-line syntax to run this sample is:</span></span>

<span data-ttu-id="361b9-108">**MigrationSamples.exe vm 和儲存體-簡單的** *SourceHost* *DestinationHost* *VmName*</span><span class="sxs-lookup"><span data-stu-id="361b9-108">**MigrationSamples.exe vm-and-storage-simple** *SourceHost* *DestinationHost* *VmName*</span></span>

<span data-ttu-id="361b9-109">其中的參數如下：</span><span class="sxs-lookup"><span data-stu-id="361b9-109">where the parameters are as follows:</span></span>

-   <span data-ttu-id="361b9-110">*SourceHost* 是目前虛擬機器主機的名稱。</span><span class="sxs-lookup"><span data-stu-id="361b9-110">*SourceHost* is the name of the current host of the virtual machine.</span></span>
-   <span data-ttu-id="361b9-111">*DestinationHost* 是目的地主機的名稱。</span><span class="sxs-lookup"><span data-stu-id="361b9-111">*DestinationHost* is the name of the destination host.</span></span>
-   <span data-ttu-id="361b9-112">*VmName* 是虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="361b9-112">*VmName* is the name of the virtual machine.</span></span>


```CSharp
/// <summary>
/// Migrates a VM without any modification, using all defaults.
/// Resource pools will be used to get correct path for the VHDs.
/// </summary>
/// <param name="sourceHost">Migration source hostname</param>
/// <param name="destinationHost">
/// Migration destination hostname
/// </param>
/// <param name="vmName">VM name.</param>
public
void
VmAndStorageMigrationSimple(
    string sourceHost,
    string destinationHost,
    string vmName
    )
{
    ManagementScope srcScope = new ManagementScope(
        @"\\" + sourceHost + @"\root\virtualization\v2", null);

    using (ManagementObject migrationSettingData = GetMigrationSettingData(srcScope))
    using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, srcScope))
    {
        migrationSettingData["MigrationType"] = MigrationType.VirtualSystemAndStorage;
        migrationSettingData["TransportType"] = TransportType.TCP;

        // Get the VHD SASDs
        string[] sasds = null;
        ManagementObject[] vhdList = WmiUtilities.GetVhdSettings(vm);
        if (vhdList != null)
        {
            sasds = new string[vhdList.Length];

            for (uint index = 0; index < vhdList.Length; ++index)
            {
                using (ManagementObject vhd = vhdList[index])
                {
                    // Change the VHD path to an empty string which will force
                    // the system to use resource pools to get the right path at
                    // the destination node.
                    vhd["HostResource"] = new string[] { "" };

                    // Create array of embedded instances.
                    sasds[index] = vhd.GetText(TextFormat.CimDtd20);
                }
            }
        }
        else
        {
            Console.WriteLine("No VHDs found associated with the VM. Skipping VHDs...");
        }

        // Perform migration.
        Console.WriteLine("Performing migration...");
        Migrate(srcScope,
            vmName,
            destinationHost,
            migrationSettingData.GetText(TextFormat.CimDtd20),
            null,
            sasds);
    }
}
```



<span data-ttu-id="361b9-113">下列 c # 程式碼包含從上述範例中呼叫的大部分公用程式方法的執行。</span><span class="sxs-lookup"><span data-stu-id="361b9-113">The following C# code contains the implementation of most of the utility methods called from the example above.</span></span>


```CSharp
class MigrationCommon
{
    ///////////////////////////////////////////////////////////////////////
    // Common values and methods for all migration types.
    ///////////////////////////////////////////////////////////////////////

    /// <summary>
    /// Defines the migration types.
    /// </summary>
    public enum MigrationType
    {
        VirtualSystem = 32768,
        Storage = 32769,
        Staged = 32770,
        VirtualSystemAndStorage = 32771
    };

    /// <summary>
    /// Defines migration transport types.
    /// </summary>
    public enum TransportType
    {
        TCP = 5
    };

    /// <summary>
    /// Gets the virtual system migration service.
    /// </summary>
    /// <param name="scope">The scope to use when connecting to WMI.</param>
    /// <returns>The virtual system migration service.</returns>
    public
    ManagementObject
    GetVirtualMachineMigrationService(
        ManagementScope scope)
    {
        using (ManagementClass migrationServiceClass = new ManagementClass("Msvm_VirtualSystemMigrationService"))
        {
            migrationServiceClass.Scope = scope;

            ManagementObject migrationService =
                WmiUtilities.GetFirstObjectFromCollection(migrationServiceClass.GetInstances());

            return migrationService;
        }
    }

    /// <summary>
    /// Returns the instance of
    /// Msvm_VirtualSystemMigrationServiceSettingData
    /// associated with the service.
    /// </summary>
    /// <param name="service">Migration service instance</param>
    /// <returns>
    /// Instance of Msvm_VirtualSystemMigrationServiceSettingData
    /// </returns>
    public
    ManagementObject
    GetMigrationServiceSettings(
        ManagementObject service
        )
    {
        ManagementObject serviceSetting = null;
        using (ManagementObjectCollection settingCollection =
            service.GetRelated("Msvm_VirtualSystemMigrationServiceSettingData"))
        {
            foreach (ManagementObject mgmtObj in settingCollection)
            {
                serviceSetting = mgmtObj;
                break;
            }
        }

        return serviceSetting;
    }

    /// <summary>
    /// Retuns the migration setting data object to be used for
    /// migration.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <returns>Migration setting data object</returns>
    public
    ManagementObject
    GetMigrationSettingData(
        ManagementScope scope
        )
    {
        ManagementObject migrationSettingData = null;
        ManagementPath settingPath =
            new ManagementPath("Msvm_VirtualSystemMigrationSettingData");

        using (ManagementClass migrationSettingDataClass = new ManagementClass(scope, settingPath, null))
        {
            migrationSettingData = migrationSettingDataClass.CreateInstance();
        }

        return migrationSettingData;
    }

    /// <summary>
    /// Performs the migration.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <param name="vmName">The virtual machine name.</param>
    /// <param name="destinationHost">Migration destination host</param>
    /// <param name="migrationSetting">Embedded instance of
    /// Msvm_VirtualSystemMigrationSettingData.</param>
    /// <param name="vssd">Embedded instance of
    /// Msvm_VirtualSystemSettingData.</param>
    /// <param name="rasds">Array of embedded instances of
    /// Msvm_ResourceAllocationSettingData.</param>
    public
    void
    Migrate(
        ManagementScope scope,
        string vmName,
        string destinationHost,
        string migrationSetting,
        string vssd,
        string[] rasds
        )
    {
        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementBaseObject inParams = service.GetMethodParameters("MigrateVirtualSystemToHost"))
        using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
        {
            inParams["ComputerSystem"] = vm.Path.Path;
            inParams["DestinationHost"] = destinationHost;
            inParams["MigrationSettingData"] = migrationSetting;
            inParams["NewSystemSettingData"] = vssd;
            inParams["NewResourceSettingData"] = rasds;

            using (ManagementBaseObject outParams =
                service.InvokeMethod("MigrateVirtualSystemToHost", inParams, null))
            {
                WmiUtilities.ValidateOutput(outParams, scope);
            }
        }
    }

    /// <summary>
    /// Performs migratability check.
    /// </summary>
    /// <param name="scope">The namespace to be used.</param>
    /// <param name="vmName">The virtual machine name.</param>
    /// <param name="destinationHost">Migration destination host</param>
    /// <param name="migrationSetting">Embedded instance of
    /// Msvm_VirtualSystemMigrationSettingData.</param>
    /// <param name="vssd">Embedded instance of
    /// Msvm_VirtualSystemSettingData.</param>
    /// <param name="rasds">Array of embedded instances of
    /// Msvm_ResourceAllocationSettingData.</param>
    /// <returns>true if virtual machine is migratable, false otherwise</returns>
    public
    bool
    CheckMigratability(
        ManagementScope scope,
        string vmName,
        string destinationHost,
        string migrationSetting,
        string vssd,
        string[] rasds
        )
    {
        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementBaseObject inParams =
            service.GetMethodParameters("MigrateVirtualSystemToHost"))
        using (ManagementObject vm = WmiUtilities.GetVirtualMachine(vmName, scope))
        {
            inParams["ComputerSystem"] = vm.Path.Path;
            inParams["DestinationHost"] = destinationHost;
            inParams["MigrationSettingData"] = migrationSetting;
            inParams["NewSystemSettingData"] = vssd;
            inParams["NewResourceSettingData"] = rasds;

            using (ManagementBaseObject outParams =
                service.InvokeMethod("CheckVirtualSystemIsMigratable", inParams, null))
            {
                return WmiUtilities.ValidateOutput(outParams, scope, false, true);
            }
        }
    }

    /// <summary>
    /// Returns array of IP addresses on which the migration destination
    /// host is listening for incoming VM migration request.
    /// </summary>
    /// <param name="destinationHost">
    /// Migration destination hostname
    /// </param>
    /// <returns>Listening IP addresses</returns>
    public
    string[]
    GetMigrationDestinationListenAddresses(
        string destinationHost
        )
    {
        string[] ipAddresses = null;

        ManagementScope scope = new ManagementScope(
            @"\\" + destinationHost + @"\root\virtualization\v2", null);

        using (ManagementObject service = GetVirtualMachineMigrationService(scope))
        using (ManagementObject serviceSetting = GetMigrationServiceSettings(service))
        {
            if (!((bool)serviceSetting["EnableVirtualSystemMigration"]))
            {
                throw new Exception("Destination host does not " +
                    "allow VM migration");
            }

            ipAddresses =
                (string[])service["MigrationServiceListenerIPAddressList"];
            if (ipAddresses == null)
            {
                throw new Exception("Destination host does not have " +
                    "networks set for VM migration");
            }
        }

        return ipAddresses;
    }
}
```



 

 



