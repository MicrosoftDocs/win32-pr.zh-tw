---
description: 您可以使用 WMI 腳本類型程式庫，從 Microsoft Visual Studio 和 Windows Script Host W2KMIGUSER.WSF 檔中呼叫 WMI 腳本 API 方法。
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: 使用 WMI 腳本型別程式庫
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987694"
---
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="1fa01-103">使用 WMI 腳本型別程式庫</span><span class="sxs-lookup"><span data-stu-id="1fa01-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="1fa01-104">您可以使用 WMI 腳本類型程式庫，從 Microsoft Visual Studio 和 Windows Script Host W2KMIGUSER.WSF 檔中呼叫 WMI 腳本 API 方法。</span><span class="sxs-lookup"><span data-stu-id="1fa01-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="1fa01-105">使用 WMI 腳本類型程式庫搭配 Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1fa01-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="1fa01-106">Visual InterDev 6.0 功能已整合至 [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx)中。</span><span class="sxs-lookup"><span data-stu-id="1fa01-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="1fa01-107">下列程式描述如何啟用 (IDE) 的整合式開發環境，以感知 WbemScripting 型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="1fa01-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="1fa01-108">**將 WMI 腳本類型程式庫加入至專案參考**</span><span class="sxs-lookup"><span data-stu-id="1fa01-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="1fa01-109">從 [**專案**] 功能表選取 [**加入參考**]。</span><span class="sxs-lookup"><span data-stu-id="1fa01-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="1fa01-110">在 [ **加入參考** ] 方塊的 [COM] 索引標籤中，選取 [Microsoft WMI 腳本1.2 程式庫]。</span><span class="sxs-lookup"><span data-stu-id="1fa01-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="1fa01-111">如果 [參考] 清單中沒有出現適當的選項，請使用 [**參考**] 方塊中的 **[流覽]** 將它加入。</span><span class="sxs-lookup"><span data-stu-id="1fa01-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="1fa01-112">**流覽** 會開啟 [**新增參考**] 方塊，讓您找出 WbemScripting 型別程式庫。</span><span class="sxs-lookup"><span data-stu-id="1fa01-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="1fa01-113">WbemScripting 類型程式庫位於% windir% \\ System32 Wbem 目錄中的 >wbemdisp.tlb 檔案。 \\</span><span class="sxs-lookup"><span data-stu-id="1fa01-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="1fa01-114">選取檔案，然後按一下 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="1fa01-114">Select the file and click **Open**.</span></span> <span data-ttu-id="1fa01-115">[參考] 清單中會顯示 Microsoft WMI 腳本1.2 程式庫。</span><span class="sxs-lookup"><span data-stu-id="1fa01-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="1fa01-116">確定您在清單中選取此專案旁的方塊。</span><span class="sxs-lookup"><span data-stu-id="1fa01-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="1fa01-117">使用 WMI 腳本類型程式庫搭配 Windows Script Host 2。0</span><span class="sxs-lookup"><span data-stu-id="1fa01-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="1fa01-118">您可以在 Windows Script Host W2KMIGUSER.WSF 檔中包含 WbemScripting 的參考，而不像撰寫 Visual Basic、腳本撰寫版或其他指令碼語言的腳本 **。**</span><span class="sxs-lookup"><span data-stu-id="1fa01-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="1fa01-119">這可讓您使用常數名稱，而不是值。</span><span class="sxs-lookup"><span data-stu-id="1fa01-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="1fa01-120">例如，在設定驗證時，請使用 **WbemAuthenticationLevelPktPrivacy** ，而不是值6。</span><span class="sxs-lookup"><span data-stu-id="1fa01-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="1fa01-121">腳本可以使用下列方法，與 WMI 類型程式庫的腳本 API 連接：</span><span class="sxs-lookup"><span data-stu-id="1fa01-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="1fa01-122">在 VBScript 方法 [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) 和 [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx)中指定 WbemScripting GUID。</span><span class="sxs-lookup"><span data-stu-id="1fa01-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="1fa01-123">這會警示 Windows Script Host 以連接至 WMI 物件集。</span><span class="sxs-lookup"><span data-stu-id="1fa01-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="1fa01-124">下列 VBScript 程式碼範例會建立新的 [**SWbemDateTime**](swbemdatetime.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="1fa01-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="1fa01-125">取得新的或現有的物件時，使用 [標記字串](constructing-a-moniker-string.md) "winmgmts："。</span><span class="sxs-lookup"><span data-stu-id="1fa01-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="1fa01-126">下列 VBScript 程式碼範例會使用 "winmgmts：" 標記來取得具有 **控制碼** 屬性 0 (零) 的 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process)實例。</span><span class="sxs-lookup"><span data-stu-id="1fa01-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="1fa01-127">**控制碼** 是這個類別的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="1fa01-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="1fa01-128">使用 <reference> WSH 2.0 XML 檔案格式的標記參考 WMI 類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="1fa01-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="1fa01-129">如果您使用 <reference> 標記，標記必須有一個 **uuid** 屬性，其值為 WMI 類型程式庫的 **GUID** ，或 (建議) 物件屬性，其值是您可以建立的任何 WMI 腳本物件的 **PROGID** 。</span><span class="sxs-lookup"><span data-stu-id="1fa01-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="1fa01-130">下列 VBScript 程式碼範例會使用 "WbemScripting" 的 PROGID。</span><span class="sxs-lookup"><span data-stu-id="1fa01-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="1fa01-131">若要執行腳本，請將文字儲存在副檔名為 w2kmiguser.wsf 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="1fa01-131">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   <span data-ttu-id="1fa01-132">使用 <**物件**> 標記來建立 WMI 腳本物件。</span><span class="sxs-lookup"><span data-stu-id="1fa01-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="1fa01-133">您可以使用參考您想要建立之 WMI 腳本物件的名稱值來指定 **id** 屬性，讓 **PROGID** 屬性等於 WMI 腳本物件的 PROID。</span><span class="sxs-lookup"><span data-stu-id="1fa01-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="1fa01-134">下列 WSH 腳本會顯示主機名稱和本機電腦上的處理器數目。</span><span class="sxs-lookup"><span data-stu-id="1fa01-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="1fa01-135">若要執行腳本，請將文字儲存在副檔名為 w2kmiguser.wsf 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="1fa01-135">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a><span data-ttu-id="1fa01-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="1fa01-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa01-137">WMI 中的腳本</span><span class="sxs-lookup"><span data-stu-id="1fa01-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="1fa01-138">適用于 WMI 的腳本 API</span><span class="sxs-lookup"><span data-stu-id="1fa01-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
