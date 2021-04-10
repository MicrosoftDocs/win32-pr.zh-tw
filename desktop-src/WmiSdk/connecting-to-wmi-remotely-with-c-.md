---
description: '如同 PowerShell、VBScript 或 c + + 等其他語言，您可以使用 c # 從遠端監視遠端電腦上的硬體和軟體。'
ms.assetid: 9E03A8D0-01AB-4B7E-99B6-FEEF9C1CAE17
ms.tgt_platform: multiple
title: 使用 C 遠端連線至 WMI#
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ad9fe2008b52276a8f68149b33ae3729daaf7d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027171"
---
# <a name="connecting-to-wmi-remotely-with-c"></a>使用 C 遠端連線至 WMI#

如同 PowerShell、VBScript 或 c + + 等其他語言，您可以使用 c # 從遠端監視遠端電腦上的硬體和軟體。 管理程式碼的遠端連線是透過 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間來完成。  (舊版的 WMI 使用了 [System. Management](/dotnet/api/system.management) 命名空間，此命名空間包含在此命名空間，以提供完整性。 ) 

> [!Note]  
> **系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。

 

使用 Microsoft 中的類別遠端連線。 [基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間使用 DCOM 作為基礎遠端機制。 WMI 遠端連線必須符合模擬和驗證的 DCOM 安全性需求。 根據預設，範圍會系結至本機電腦和「根 CIMv2」 \\ 系統命名空間。 不過，您可以變更您所存取的電腦、網域和 WMI 命名空間。 您也可以設定授權單位、模擬、認證和其他連接選項。

**若要使用 c # 從遠端連線到 WMI (Microsoft 管理. 基礎結構)**

1.  使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85))的呼叫，在遠端電腦上建立會話。

    如果您要使用相同的認證連接到遠端電腦 (網域和使用者名稱) 您登入時，您可以在 [建立](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) 呼叫中指定電腦的名稱。 一旦有傳回的 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) 物件之後，您就可以進行 WMI 查詢。

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    如需在 c # 中使用 **Microsoft.** API API 進行 wmi 查詢的詳細資訊，請參閱抓取 [Wmi 類別或實例資料](retrieving-class-or-instance-data.md)。

2.  如果您想要為連接設定不同的選項，例如不同的認證、地區設定或模擬層級，您必須在呼叫[CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))時使用[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))物件。

    [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) 是 [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) 和 [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85))的基類。 您可以使用來分別設定 WS-Man 和 DCOM 會話的選項。 下列程式碼範例說明如何使用 [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) 物件將模擬層級設定為模擬。

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  如果您想要設定連接的認證，您必須建立 [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) 物件，並將其新增至您的 [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))。

    下列程式碼範例說明如何建立[WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85))類別、將它填入適當的[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))，以及在 CimSession 中使用它[。](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))

    ```CSharp
    string computer = “Computer_B”;
    string domain = “Domain1″;
    string username = “User1″;

    string plaintextpassword; 

    //Retrieve password from the user. 
    //For the complete code, see the sample at the bottom of this topic.

    CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, domain, username, securepassword); 

    WSManSessionOptions SessionOptions = new WSManSessionOptions();
    SessionOptions.AddDestinationCredentials(Credentials); 

    CimSession Session = CimSession.Create(computer, SessionOptions);
    ```

    

    一般來說，建議您不要將密碼硬式編碼到您的應用程式中;如上述程式碼範例所示，盡可能地嘗試查詢使用者的密碼，並將其儲存在安全的地方。

WMI 是用於監視遠端電腦上的硬體和軟體。 WMI v1 的遠端連線是透過 [ManagementScope](/dotnet/api/system.management.managementscope) 物件來完成。

**若要使用 c # 從遠端連線到 WMI (System. Management)**

1.  使用電腦名稱稱和 WMI 路徑建立 [ManagementScope](/dotnet/api/system.management.managementscope) 物件，並使用 ManagementScope 的呼叫連接到您的目標。 () 連線。

    如果您要使用相同的認證來連線到遠端電腦 (網域和使用者名稱) 登入，則您只需要指定 WMI 路徑。 一旦連線之後，您就可以進行 WMI 查詢。

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    如需使用 c # 中的 [系統管理](/dotnet/api/system.management) API 進行 wmi 查詢的詳細資訊，請參閱抓取 [Wmi 類別或實例資料](retrieving-class-or-instance-data.md)。

2.  如果您連接到不同網域中的遠端電腦，或是使用不同的使用者名稱和密碼，則必須在呼叫[ManagementScope](/dotnet/api/system.management.managementscope)時使用[ConnectionOptions](/dotnet/api/system.management.connectionoptions)物件。

    [ConnectionOptions](/dotnet/api/system.management.connectionoptions)包含用來描述驗證、模擬、使用者名稱、密碼和其他連接選項的屬性。 下列程式碼範例說明如何使用 [ConnectionOptions](/dotnet/api/system.management.connectionoptions) 將模擬層級設定為模擬。

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    一般來說，除非明確需要，否則建議您將模擬層級設定為模擬。 此外，請嘗試避免將您的名稱和密碼寫入 c # 程式碼中。  (可能的話，請查看您是否可以查詢使用者，以便在執行時間動態提供這些使用者。 ) 

    如需在遠端 WMI 連接上設定不同屬性的更多範例，請參閱 [ConnectionOptions](/dotnet/api/system.management.connectionoptions) 參考頁面的範例一節。

## <a name="microsoftmanagementinfrastructure-example"></a>Microsoft. 管理基礎結構範例

下列 c # 程式碼範例以 [TechNet 上的下列 blog 文章](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)為基礎，說明如何使用 [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) 和 [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) 來設定遠端連線的認證。


```CSharp
using System;
using System.Text;
using System.Threading;
using Microsoft.Management.Infrastructure;
using Microsoft.Management.Infrastructure.Options;
using System.Security; 

namespace SMAPIQuery
{
    class Program
    {
        static void Main(string[] args)
        { 

            string computer = "Computer_B";
            string domain = "DOMAIN";
            string username = "AdminUserName";


            string plaintextpassword; 

            Console.WriteLine("Enter password:");
            plaintextpassword = Console.ReadLine(); 

            SecureString securepassword = new SecureString();
            foreach (char c in plaintextpassword)
            {
                securepassword.AppendChar(c);
            } 

            // create Credentials
            CimCredential Credentials = new CimCredential(PasswordAuthenticationMechanism.Default, 
                                                          domain, 
                                                          username, 
                                                          securepassword); 

            // create SessionOptions using Credentials
            WSManSessionOptions SessionOptions = new WSManSessionOptions();
            SessionOptions.AddDestinationCredentials(Credentials); 

            // create Session using computer, SessionOptions
            CimSession Session = CimSession.Create(computer, SessionOptions); 

            var allVolumes = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Volume");
            var allPDisks = Session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_DiskDrive"); 

            // Loop through all volumes
            foreach (CimInstance oneVolume in allVolumes)
            {
                // Show volume information

                if (oneVolume.CimInstanceProperties["DriveLetter"].ToString()[0] > ' '  )
                {
                    Console.WriteLine("Volume ‘{0}’ has {1} bytes total, {2} bytes available", 
                                      oneVolume.CimInstanceProperties["DriveLetter"], 
                                      oneVolume.CimInstanceProperties["Size"], 
                                      oneVolume.CimInstanceProperties["SizeRemaining"]);
                }

            } 

            // Loop through all physical disks
            foreach (CimInstance onePDisk in allPDisks)
            {
                // Show physical disk information
                Console.WriteLine("Disk {0} is model {1}, serial number {2}", 
                                  onePDisk.CimInstanceProperties["DeviceId"], 
                                  onePDisk.CimInstanceProperties["Model"].ToString().TrimEnd(), 
                                  onePDisk.CimInstanceProperties["SerialNumber"]);
            } 

            Console.ReadLine();
         }
     }
 }
```



## <a name="systemmanagement-example"></a>系統管理範例

下列 c # 程式碼範例說明一般遠端連線，使用系統管理物件。


```CSharp
using System;
using System.Management;
public class RemoteConnect 
{
    public static void Main() 
    {
        ConnectionOptions options = new ConnectionOptions();
        options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

        
        ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
        scope.Connect();

        //Query system for Operating System information
        ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
        ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);

        ManagementObjectCollection queryCollection = searcher.Get();
        foreach ( ManagementObject m in queryCollection)
        {
            // Display the remote computer information
            Console.WriteLine("Computer Name     : {0}", m["csname"]);
            Console.WriteLine("Windows Directory : {0}", m["WindowsDirectory"]);
            Console.WriteLine("Operating System  : {0}", m["Caption"]);
            Console.WriteLine("Version           : {0}", m["Version"]);
            Console.WriteLine("Manufacturer      : {0}", m["Manufacturer"]);
        }
    }
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[連接至遠端電腦上的 WMI](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
