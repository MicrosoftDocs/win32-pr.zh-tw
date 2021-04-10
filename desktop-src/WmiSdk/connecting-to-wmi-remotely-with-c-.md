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
# <a name="connecting-to-wmi-remotely-with-c"></a><span data-ttu-id="7b529-103">使用 C 遠端連線至 WMI#</span><span class="sxs-lookup"><span data-stu-id="7b529-103">Connecting to WMI Remotely with C#</span></span>

<span data-ttu-id="7b529-104">如同 PowerShell、VBScript 或 c + + 等其他語言，您可以使用 c # 從遠端監視遠端電腦上的硬體和軟體。</span><span class="sxs-lookup"><span data-stu-id="7b529-104">As with other languages such as PowerShell, VBScript, or C++, you can use C# to remotely monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="7b529-105">管理程式碼的遠端連線是透過 [Microsoft. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間來完成。</span><span class="sxs-lookup"><span data-stu-id="7b529-105">Remote connections for managed code are accomplished through the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace.</span></span> <span data-ttu-id="7b529-106"> (舊版的 WMI 使用了 [System. Management](/dotnet/api/system.management) 命名空間，此命名空間包含在此命名空間，以提供完整性。 ) </span><span class="sxs-lookup"><span data-stu-id="7b529-106">(Previous versions of WMI used the [System.Management](/dotnet/api/system.management) namespace, which is included here for completeness.)</span></span>

> [!Note]  
> <span data-ttu-id="7b529-107">**系統管理** 是用來存取 WMI 的原始 .net 命名空間;不過，這個命名空間中的 Api 通常會較慢，而且也不會相對於其較新式的 **Microsoft 管理元件** 對應專案。</span><span class="sxs-lookup"><span data-stu-id="7b529-107">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="7b529-108">使用 Microsoft 中的類別遠端連線。 [基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) 命名空間使用 DCOM 作為基礎遠端機制。</span><span class="sxs-lookup"><span data-stu-id="7b529-108">Connecting remotely using classes in the [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace uses DCOM as the underlying remote mechanism.</span></span> <span data-ttu-id="7b529-109">WMI 遠端連線必須符合模擬和驗證的 DCOM 安全性需求。</span><span class="sxs-lookup"><span data-stu-id="7b529-109">WMI remote connections must comply with DCOM security requirements for impersonation and authentication.</span></span> <span data-ttu-id="7b529-110">根據預設，範圍會系結至本機電腦和「根 CIMv2」 \\ 系統命名空間。</span><span class="sxs-lookup"><span data-stu-id="7b529-110">By default, a scope is bound to the local computer and the "Root\\CIMv2" system namespace.</span></span> <span data-ttu-id="7b529-111">不過，您可以變更您所存取的電腦、網域和 WMI 命名空間。</span><span class="sxs-lookup"><span data-stu-id="7b529-111">However, you can change both the computer, domain, and WMI namespace that you access.</span></span> <span data-ttu-id="7b529-112">您也可以設定授權單位、模擬、認證和其他連接選項。</span><span class="sxs-lookup"><span data-stu-id="7b529-112">You can also set authority, impersonation, credentials, and other connection options.</span></span>

<span data-ttu-id="7b529-113">**若要使用 c # 從遠端連線到 WMI (Microsoft 管理. 基礎結構)**</span><span class="sxs-lookup"><span data-stu-id="7b529-113">**To connect to WMI remotely with C# (Microsoft.Management.Infrastructure)**</span></span>

1.  <span data-ttu-id="7b529-114">使用 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85))的呼叫，在遠端電腦上建立會話。</span><span class="sxs-lookup"><span data-stu-id="7b529-114">Create a session on the remote machine with a call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)).</span></span>

    <span data-ttu-id="7b529-115">如果您要使用相同的認證連接到遠端電腦 (網域和使用者名稱) 您登入時，您可以在 [建立](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) 呼叫中指定電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="7b529-115">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you can specify the name of the computer in the [Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832539(v=vs.85)) call.</span></span> <span data-ttu-id="7b529-116">一旦有傳回的 [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) 物件之後，您就可以進行 WMI 查詢。</span><span class="sxs-lookup"><span data-stu-id="7b529-116">Once you have the returned [CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832509(v=vs.85)) object, you can then make your WMI query.</span></span>

    ```CSharp
    using Microsoft.Management.Infrastructure;
    ...
    string Namespace = @"root\cimv2";
    string OSQuery = "SELECT * FROM Win32_OperatingSystem";
    CimSession mySession = CimSession.Create("Computer_B");
    IEnumerable<CimInstance> queryInstance = mySession.QueryInstances(Namespace, "WQL", OSQuery);
    ```

    

    <span data-ttu-id="7b529-117">如需在 c # 中使用 **Microsoft.** API API 進行 wmi 查詢的詳細資訊，請參閱抓取 [Wmi 類別或實例資料](retrieving-class-or-instance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="7b529-117">For more information on making WMI queries with the **Microsoft.Management.Infrastructure** API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="7b529-118">如果您想要為連接設定不同的選項，例如不同的認證、地區設定或模擬層級，您必須在呼叫[CimSession](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))時使用[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))物件。</span><span class="sxs-lookup"><span data-stu-id="7b529-118">If you wish to set different options for your connection, such as different credentials, locale or Impersonation levels, you need to use a [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) object in your call to [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)).</span></span>

    <span data-ttu-id="7b529-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) 是 [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) 和 [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85))的基類。</span><span class="sxs-lookup"><span data-stu-id="7b529-119">[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)) is a base class for [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) and [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)).</span></span> <span data-ttu-id="7b529-120">您可以使用來分別設定 WS-Man 和 DCOM 會話的選項。</span><span class="sxs-lookup"><span data-stu-id="7b529-120">You can use either to set the options on your WS-Man and DCOM sessions, respectively.</span></span> <span data-ttu-id="7b529-121">下列程式碼範例說明如何使用 [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) 物件將模擬層級設定為模擬。</span><span class="sxs-lookup"><span data-stu-id="7b529-121">The following code sample describes using a [DComSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832688(v=vs.85)) object to set the Impersonation level to Impersonate.</span></span>

    ```CSharp
    string computer = "Computer_B"
    DComSessionOptions DComOptions = new DComSessionOptions();
    DComOptions.Impersonation = ImpersonationType.Impersonate;

    CimSession Session = CimSession.Create(computer, DComOptions);
    ```

    

3.  <span data-ttu-id="7b529-122">如果您想要設定連接的認證，您必須建立 [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) 物件，並將其新增至您的 [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="7b529-122">If you wish to set the credentials for your connection, you will need to create and add a [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) object to your [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)).</span></span>

    <span data-ttu-id="7b529-123">下列程式碼範例說明如何建立[WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85))類別、將它填入適當的[CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85))，以及在 CimSession 中使用它[。](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b529-123">The following code sample describes creating a [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) class, filling it with the proper [CimSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832510(v=vs.85)), and using it in a [CimSession.Create](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832529(v=vs.85)) call.</span></span>

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

    

    <span data-ttu-id="7b529-124">一般來說，建議您不要將密碼硬式編碼到您的應用程式中;如上述程式碼範例所示，盡可能地嘗試查詢使用者的密碼，並將其儲存在安全的地方。</span><span class="sxs-lookup"><span data-stu-id="7b529-124">It is generally recommended that you do not hardcode a password into your applications; as the above code sample indicates, whenever possible try to query your user for the password, and store it securely.</span></span>

<span data-ttu-id="7b529-125">WMI 是用於監視遠端電腦上的硬體和軟體。</span><span class="sxs-lookup"><span data-stu-id="7b529-125">WMI is intended to monitor the hardware and software on remote computers.</span></span> <span data-ttu-id="7b529-126">WMI v1 的遠端連線是透過 [ManagementScope](/dotnet/api/system.management.managementscope) 物件來完成。</span><span class="sxs-lookup"><span data-stu-id="7b529-126">Remote connections for WMI v1 is accomplished through the [ManagementScope](/dotnet/api/system.management.managementscope) object.</span></span>

<span data-ttu-id="7b529-127">**若要使用 c # 從遠端連線到 WMI (System. Management)**</span><span class="sxs-lookup"><span data-stu-id="7b529-127">**To connect to WMI remotely with C# (System.Management)**</span></span>

1.  <span data-ttu-id="7b529-128">使用電腦名稱稱和 WMI 路徑建立 [ManagementScope](/dotnet/api/system.management.managementscope) 物件，並使用 ManagementScope 的呼叫連接到您的目標。 () 連線。</span><span class="sxs-lookup"><span data-stu-id="7b529-128">Create a [ManagementScope](/dotnet/api/system.management.managementscope) object, using the name of the computer and the WMI path, and connect to your target with a call to ManagementScope.Connect().</span></span>

    <span data-ttu-id="7b529-129">如果您要使用相同的認證來連線到遠端電腦 (網域和使用者名稱) 登入，則您只需要指定 WMI 路徑。</span><span class="sxs-lookup"><span data-stu-id="7b529-129">If you are connecting to a remote computer using the same credentials (domain and user name) you are logged on with, then you only have to specify the WMI path.</span></span> <span data-ttu-id="7b529-130">一旦連線之後，您就可以進行 WMI 查詢。</span><span class="sxs-lookup"><span data-stu-id="7b529-130">Once you have connected, you can make your WMI query.</span></span>

    ```CSharp
    using System.Management;
    ...
    ManagementScope scope = new ManagementScope("\\\\Computer_B\\root\\cimv2");
    scope.Connect();
    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope, query);
    ```

    

    <span data-ttu-id="7b529-131">如需使用 c # 中的 [系統管理](/dotnet/api/system.management) API 進行 wmi 查詢的詳細資訊，請參閱抓取 [Wmi 類別或實例資料](retrieving-class-or-instance-data.md)。</span><span class="sxs-lookup"><span data-stu-id="7b529-131">For more information on making WMI queries with the [System.Management](/dotnet/api/system.management) API in C#, see [Retrieving WMI Class or Instance Data](retrieving-class-or-instance-data.md).</span></span>

2.  <span data-ttu-id="7b529-132">如果您連接到不同網域中的遠端電腦，或是使用不同的使用者名稱和密碼，則必須在呼叫[ManagementScope](/dotnet/api/system.management.managementscope)時使用[ConnectionOptions](/dotnet/api/system.management.connectionoptions)物件。</span><span class="sxs-lookup"><span data-stu-id="7b529-132">If you connect to a remote computer in a different domain or using a different user name and password, then you must use a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) object in the call to the [ManagementScope](/dotnet/api/system.management.managementscope).</span></span>

    <span data-ttu-id="7b529-133">[ConnectionOptions](/dotnet/api/system.management.connectionoptions)包含用來描述驗證、模擬、使用者名稱、密碼和其他連接選項的屬性。</span><span class="sxs-lookup"><span data-stu-id="7b529-133">The [ConnectionOptions](/dotnet/api/system.management.connectionoptions) contains properties for describing the Authentication, Impersonation, username, password, and other connection options.</span></span> <span data-ttu-id="7b529-134">下列程式碼範例說明如何使用 [ConnectionOptions](/dotnet/api/system.management.connectionoptions) 將模擬層級設定為模擬。</span><span class="sxs-lookup"><span data-stu-id="7b529-134">The following code sample describes using a [ConnectionOptions](/dotnet/api/system.management.connectionoptions) to set the Impersonation Level to Impersonate.</span></span>

    ```CSharp
    ConnectionOptions options = new ConnectionOptions();
    options.Impersonation = System.Management.ImpersonationLevel.Impersonate;

    ManagementScope scope = new ManagementScope("\\\\FullComputerName\\root\\cimv2", options);
    scope.Connect();

    ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_OperatingSystem");
    ManagementObjectSearcher searcher = new ManagementObjectSearcher(scope,query);
    ```

    

    <span data-ttu-id="7b529-135">一般來說，除非明確需要，否則建議您將模擬層級設定為模擬。</span><span class="sxs-lookup"><span data-stu-id="7b529-135">Generally speaking, it is recommended that you set your Impersonation level to Impersonate unless explicitly needed otherwise.</span></span> <span data-ttu-id="7b529-136">此外，請嘗試避免將您的名稱和密碼寫入 c # 程式碼中。</span><span class="sxs-lookup"><span data-stu-id="7b529-136">Further, try to avoid writing your name and password into C# code.</span></span> <span data-ttu-id="7b529-137"> (可能的話，請查看您是否可以查詢使用者，以便在執行時間動態提供這些使用者。 ) </span><span class="sxs-lookup"><span data-stu-id="7b529-137">(If possible, see if you can query the user to dynamically supply them at runtime.)</span></span>

    <span data-ttu-id="7b529-138">如需在遠端 WMI 連接上設定不同屬性的更多範例，請參閱 [ConnectionOptions](/dotnet/api/system.management.connectionoptions) 參考頁面的範例一節。</span><span class="sxs-lookup"><span data-stu-id="7b529-138">For more examples of setting different properties on a remote WMI connection, see the Examples section of the [ConnectionOptions](/dotnet/api/system.management.connectionoptions) reference page.</span></span>

## <a name="microsoftmanagementinfrastructure-example"></a><span data-ttu-id="7b529-139">Microsoft. 管理基礎結構範例</span><span class="sxs-lookup"><span data-stu-id="7b529-139">Microsoft.Management.Infrastructure Example</span></span>

<span data-ttu-id="7b529-140">下列 c # 程式碼範例以 [TechNet 上的下列 blog 文章](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage)為基礎，說明如何使用 [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) 和 [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) 來設定遠端連線的認證。</span><span class="sxs-lookup"><span data-stu-id="7b529-140">The following C# code example, based on the following [blog post on TechNet](/archive/blogs/josebda/sample-c-code-for-using-the-latest-wmi-classes-to-manage-windows-storage), describes how to use [CimCredentials](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832293(v=vs.85)) and [WSManSessionOptions](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh833297(v=vs.85)) to set credentials on a remote connection.</span></span>


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



## <a name="systemmanagement-example"></a><span data-ttu-id="7b529-141">系統管理範例</span><span class="sxs-lookup"><span data-stu-id="7b529-141">System.Management Example</span></span>

<span data-ttu-id="7b529-142">下列 c # 程式碼範例說明一般遠端連線，使用系統管理物件。</span><span class="sxs-lookup"><span data-stu-id="7b529-142">The following C# code sample describes a general remote connection, using the System.Management objects.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="7b529-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b529-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b529-144">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="7b529-144">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
