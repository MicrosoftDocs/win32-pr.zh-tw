---
description: 您可以使用 Wbemscripting.swbemlocator 物件的方法來取得 SWbemServices 物件，該物件代表本機電腦或遠端主機電腦上的命名空間連接。
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: 'Wbemscripting.swbemlocator 物件 (>wbemdisp.tlb) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984208"
---
# <a name="swbemlocator-object"></a><span data-ttu-id="bf7a9-103">Wbemscripting.swbemlocator 物件</span><span class="sxs-lookup"><span data-stu-id="bf7a9-103">SWbemLocator object</span></span>

<span data-ttu-id="bf7a9-104">您可以使用 **wbemscripting.swbemlocator** 物件的方法來取得 [**SWbemServices**](swbemservices.md) 物件，該物件代表本機電腦或遠端主機電腦上的命名空間連接。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-104">You can use the methods of the **SWbemLocator** object to obtain an [**SWbemServices**](swbemservices.md) object that represents a connection to a namespace on either a local computer or a remote host computer.</span></span> <span data-ttu-id="bf7a9-105">然後，您可以使用 **SWbemServices** 物件的方法來存取 WMI。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-105">You can then use the methods of the **SWbemServices** object to access WMI.</span></span> <span data-ttu-id="bf7a9-106">這個物件可以由 VBScript **CreateObject** 呼叫建立。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="bf7a9-107">成員</span><span class="sxs-lookup"><span data-stu-id="bf7a9-107">Members</span></span>

<span data-ttu-id="bf7a9-108">**Wbemscripting.swbemlocator** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bf7a9-108">The **SWbemLocator** object has these types of members:</span></span>

-   [<span data-ttu-id="bf7a9-109">方法</span><span class="sxs-lookup"><span data-stu-id="bf7a9-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="bf7a9-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bf7a9-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="bf7a9-111">方法</span><span class="sxs-lookup"><span data-stu-id="bf7a9-111">Methods</span></span>

<span data-ttu-id="bf7a9-112">**Wbemscripting.swbemlocator** 物件有這些方法。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-112">The **SWbemLocator** object has these methods.</span></span>



| <span data-ttu-id="bf7a9-113">方法</span><span class="sxs-lookup"><span data-stu-id="bf7a9-113">Method</span></span>                                              | <span data-ttu-id="bf7a9-114">描述</span><span class="sxs-lookup"><span data-stu-id="bf7a9-114">Description</span></span>                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [<span data-ttu-id="bf7a9-115">**ConnectServer**</span><span class="sxs-lookup"><span data-stu-id="bf7a9-115">**ConnectServer**</span></span>](swbemlocator-connectserver.md) | <span data-ttu-id="bf7a9-116">連接到指定電腦上的 WMI。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-116">Connects to WMI on the specified computer.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="bf7a9-117">屬性</span><span class="sxs-lookup"><span data-stu-id="bf7a9-117">Properties</span></span>

<span data-ttu-id="bf7a9-118">**Wbemscripting.swbemlocator** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-118">The **SWbemLocator** object has these properties.</span></span>



| <span data-ttu-id="bf7a9-119">屬性</span><span class="sxs-lookup"><span data-stu-id="bf7a9-119">Property</span></span>                                                | <span data-ttu-id="bf7a9-120">存取類型</span><span class="sxs-lookup"><span data-stu-id="bf7a9-120">Access type</span></span>          | <span data-ttu-id="bf7a9-121">Description</span><span class="sxs-lookup"><span data-stu-id="bf7a9-121">Description</span></span>                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="bf7a9-122">**安全性\_**</span><span class="sxs-lookup"><span data-stu-id="bf7a9-122">**Security\_**</span></span>](swbemlocator-security-.md)<br/> | <span data-ttu-id="bf7a9-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="bf7a9-123">Read-only</span></span><br/> | <span data-ttu-id="bf7a9-124">用來讀取或變更安全性設定。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-124">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bf7a9-125">備註</span><span class="sxs-lookup"><span data-stu-id="bf7a9-125">Remarks</span></span>

<span data-ttu-id="bf7a9-126">WMI 腳本程式庫物件模型的頂端是 Wbemscripting.swbemlocator 物件。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-126">At the top of the WMI scripting library object model is the SWbemLocator object.</span></span> <span data-ttu-id="bf7a9-127">Wbemscripting.swbemlocator 是用來建立與 WMI 命名空間的已驗證連接，相當於 VBScript GetObject 函數和 WMI 名字 "winmgmts：" 用來建立與 WMI 的已驗證連線。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-127">SWbemLocator is used to establish an authenticated connection to a WMI namespace, much as the VBScript GetObject function and the WMI moniker "winmgmts:" are used to establish an authenticated connection to WMI.</span></span> <span data-ttu-id="bf7a9-128">不過，Wbemscripting.swbemlocator 的設計目的是要解決兩個無法使用 GetObject 和 WMI 標記來執行的特定腳本案例。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-128">However, SWbemLocator is designed to address two specific scripting scenarios that cannot be performed using GetObject and the WMI moniker.</span></span> <span data-ttu-id="bf7a9-129">如果需要的話，您必須使用 Wbemscripting.swbemlocator：</span><span class="sxs-lookup"><span data-stu-id="bf7a9-129">You must use SWbemLocator if you need to:</span></span>

-   <span data-ttu-id="bf7a9-130">提供使用者和密碼認證，以連接到遠端電腦上的 WMI。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-130">Provide user and password credentials to connect to WMI on a remote computer.</span></span> <span data-ttu-id="bf7a9-131">與 GetObject 函數搭配使用的 WMI 標記不包含用來指定認證的機制。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-131">The WMI moniker used with the GetObject function does not include a mechanism for specifying credentials.</span></span> <span data-ttu-id="bf7a9-132">大部分的 WMI 活動 (包括在遠端電腦上執行的所有作業) 都需要系統管理員許可權。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-132">Most WMI activities (including all of those carried out on remote computers) require administrator rights.</span></span> <span data-ttu-id="bf7a9-133">如果您通常使用一般使用者帳戶而非系統管理員帳戶登入，除非您在 [其他認證] 下執行腳本，否則無法執行大部分的 WMI 工作。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-133">If you typically log on using a regular user account instead of an administrator account, you will not be able to perform most WMI tasks unless you run the script under alternate credentials.</span></span>
-   <span data-ttu-id="bf7a9-134">如果您是從網頁內執行 WMI 腳本，請連接至 WMI。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-134">Connect to WMI if you are running a WMI script from within a Web page.</span></span> <span data-ttu-id="bf7a9-135">當您執行內嵌于 HTML 網頁中的腳本時，不能使用 GetObject 函式，因為基於安全考慮，Internet Explorer 不允許使用 GetObject。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-135">You cannot use the GetObject function when running scripts embedded within an HTML page because Internet Explorer disallows the use of GetObject for security reasons.</span></span>

<span data-ttu-id="bf7a9-136">此外，如果您發現與 GetObject 混淆或很難使用的 WMI 連接字串，您可能會想要使用 Wbemscripting.swbemlocator 連接到 WMI。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-136">In addition, you might want to use SWbemLocator to connect to WMI if you find the WMI connection string used with GetObject confusing or difficult.</span></span>

<span data-ttu-id="bf7a9-137">您可以使用 CreateObject 而非 GetObject 來建立 Wbemscripting.swbemlocator 的參考。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-137">You use CreateObject rather than GetObject to create a reference to SWbemLocator.</span></span> <span data-ttu-id="bf7a9-138">若要建立參考，您必須將 Wbemscripting.swbemlocator 程式設計識別碼 (ProgID) "WbemScripting. Wbemscripting.swbemlocator" 傳遞給 CreateObject 函式，如下列腳本範例的第2行所示。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-138">To create the reference, you must pass the CreateObject function the SWbemLocator programmatic identifier (ProgID) "WbemScripting.SWbemLocator", as shown on line 2 in the following script sample.</span></span> <span data-ttu-id="bf7a9-139">取得 Wbemscripting.swbemlocator 物件的參考之後，您可以呼叫 ConnectServer 方法來連接至 WMI，並取得 SWbemServices 物件的參考。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-139">After you obtain a reference to an SWbemLocator object, you call the ConnectServer method to connect to WMI and obtain a reference to an SWbemServices object.</span></span> <span data-ttu-id="bf7a9-140">這會在下列腳本的第3行上示範。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-140">This is demonstrated on line 3 of the following script.</span></span>


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="bf7a9-141">若要在替代認證下執行腳本，請將使用者名稱和密碼納入為傳遞給 ConnectServer 的其他參數。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-141">To run a script under alternate credentials, include the user name and password as additional parameters passed to ConnectServer.</span></span> <span data-ttu-id="bf7a9-142">例如，此腳本會使用名為 kenmyer 之使用者的認證來執行，並具有密碼 homerj。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-142">For example, this script runs under the credentials of a user named kenmyer, with the password homerj.</span></span>


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="bf7a9-143">您也可以使用網域 \\ 使用者名稱格式來指定使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-143">You can also use the Domain\\User Name format to specify a user name.</span></span> <span data-ttu-id="bf7a9-144">例如：</span><span class="sxs-lookup"><span data-stu-id="bf7a9-144">For example:</span></span>

`" fabrikam\kenmyer"`

## <a name="examples"></a><span data-ttu-id="bf7a9-145">範例</span><span class="sxs-lookup"><span data-stu-id="bf7a9-145">Examples</span></span>

<span data-ttu-id="bf7a9-146">下列 PowerShell 範例會使用 **wbemscripting.swbemlocator** 來連接到伺服器。</span><span class="sxs-lookup"><span data-stu-id="bf7a9-146">The following PowerShell example uses **SWbemLocator** to connect to a server.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="bf7a9-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf7a9-147">Requirements</span></span>



| <span data-ttu-id="bf7a9-148">需求</span><span class="sxs-lookup"><span data-stu-id="bf7a9-148">Requirement</span></span> | <span data-ttu-id="bf7a9-149">值</span><span class="sxs-lookup"><span data-stu-id="bf7a9-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf7a9-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf7a9-150">Minimum supported client</span></span><br/> | <span data-ttu-id="bf7a9-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf7a9-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf7a9-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf7a9-152">Minimum supported server</span></span><br/> | <span data-ttu-id="bf7a9-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf7a9-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf7a9-154">標頭</span><span class="sxs-lookup"><span data-stu-id="bf7a9-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf7a9-155"><dt>>wbemdisp.tlb。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a9-155"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf7a9-156">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bf7a9-156">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf7a9-157"><dt>>wbemdisp.tlb .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a9-157"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf7a9-158">DLL</span><span class="sxs-lookup"><span data-stu-id="bf7a9-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf7a9-159"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf7a9-159"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf7a9-160">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf7a9-160">CLSID</span></span><br/>                    | <span data-ttu-id="bf7a9-161">CLSID \_ wbemscripting.swbemlocator</span><span class="sxs-lookup"><span data-stu-id="bf7a9-161">CLSID\_SWbemLocator</span></span><br/>                                                          |
| <span data-ttu-id="bf7a9-162">IID</span><span class="sxs-lookup"><span data-stu-id="bf7a9-162">IID</span></span><br/>                      | <span data-ttu-id="bf7a9-163">IID \_ ISWbemLocator</span><span class="sxs-lookup"><span data-stu-id="bf7a9-163">IID\_ISWbemLocator</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="bf7a9-164">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf7a9-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf7a9-165">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="bf7a9-165">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




