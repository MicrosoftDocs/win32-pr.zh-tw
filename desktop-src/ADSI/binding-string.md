---
title: 系結字串
description: 由於可從目錄服務存取的物件數目，因此可能會發生命名衝突。
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- 系結字串 ADSI
- ADsPath ADSI、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933604"
---
# <a name="binding-string"></a><span data-ttu-id="df58c-105">系結字串</span><span class="sxs-lookup"><span data-stu-id="df58c-105">Binding String</span></span>

<span data-ttu-id="df58c-106">由於可從目錄服務存取的物件數目，因此可能會發生命名衝突。</span><span class="sxs-lookup"><span data-stu-id="df58c-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="df58c-107">系結字串（通常稱為 ADsPath）可讓您指定特定物件，而不會造成命名衝突。</span><span class="sxs-lookup"><span data-stu-id="df58c-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="df58c-108">這可套用至單一目錄服務提供者，或跨多個目錄服務提供者。</span><span class="sxs-lookup"><span data-stu-id="df58c-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="df58c-109">ADsPath 是可唯一識別目錄服務上 ADSI 物件的字串。</span><span class="sxs-lookup"><span data-stu-id="df58c-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="df58c-110">由於 ADSI 物件存在於基礎目錄服務的命名空間內容中，因此 ADsPath 名稱語法的一部分是提供者特定的。</span><span class="sxs-lookup"><span data-stu-id="df58c-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="df58c-111">下表列出預設提供的 ADSI 提供者。</span><span class="sxs-lookup"><span data-stu-id="df58c-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="df58c-112">提供者</span><span class="sxs-lookup"><span data-stu-id="df58c-112">Provider</span></span>         | <span data-ttu-id="df58c-113">描述</span><span class="sxs-lookup"><span data-stu-id="df58c-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df58c-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="df58c-114">WinNT</span></span><br/> | <span data-ttu-id="df58c-115">用來與 Windows 網域控制站通訊。</span><span class="sxs-lookup"><span data-stu-id="df58c-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="df58c-116">如需 WinNT ADsPath 的詳細資訊，請參閱 [Winnt adspath](winnt-adspath.md)。</span><span class="sxs-lookup"><span data-stu-id="df58c-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="df58c-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="df58c-117">LDAP</span></span><br/>  | <span data-ttu-id="df58c-118">用來與 LDAP 伺服器通訊，例如 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="df58c-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="df58c-119">如需有關 LDAP ADsPath 的詳細資訊，請參閱 [Ldap adspath](ldap-adspath.md)。</span><span class="sxs-lookup"><span data-stu-id="df58c-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="df58c-120">廣告</span><span class="sxs-lookup"><span data-stu-id="df58c-120">ADs</span></span><br/>   | <span data-ttu-id="df58c-121">提供可用於列舉用戶端上安裝之所有 ADSI 提供者的 [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) 執行。</span><span class="sxs-lookup"><span data-stu-id="df58c-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="df58c-122">使用這些提供者名稱來存取預設的提供者命名空間。</span><span class="sxs-lookup"><span data-stu-id="df58c-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="df58c-123">例如，如果您系結至 LDAP，ADSI 會系結至包含目前登入之網域物件的容器。</span><span class="sxs-lookup"><span data-stu-id="df58c-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="df58c-124">如果您系結至 WinNT，ADSI 會系結至保存與網路上所有網域相互關聯之物件的容器。</span><span class="sxs-lookup"><span data-stu-id="df58c-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="df58c-125">ADsPath 字串的初始元素是 ADSI 提供者 (progID) 的程式設計識別碼，後面接著 "：//"，後面接著提供者命名空間所指示的語法。</span><span class="sxs-lookup"><span data-stu-id="df58c-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="df58c-126">ProgID 字串可能會區分大小寫，視提供者而定。</span><span class="sxs-lookup"><span data-stu-id="df58c-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="df58c-127">上列提供者的 progID 字串會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="df58c-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="df58c-128">視提供者而定，路徑字串可能會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="df58c-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="df58c-129">上述提供者的路徑字串不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="df58c-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="df58c-130">以下是 ADsPaths 的範例。</span><span class="sxs-lookup"><span data-stu-id="df58c-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="df58c-131">若要尋找電腦上安裝的所有提供者，請系結至 ADs 提供者，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="df58c-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="df58c-132">使用 LDAP 提供者時，您可以在 (DN) 表單的 x.500 辨別名稱中指定 ADsPath，從 CN 標記開始，或者可以指定其階層式反向，從 O 標記開始。</span><span class="sxs-lookup"><span data-stu-id="df58c-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="df58c-133">您在初始 ADsPath 中使用的表單決定了標記的順序。</span><span class="sxs-lookup"><span data-stu-id="df58c-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="df58c-134">下表列出 ADsPath 特殊字元。</span><span class="sxs-lookup"><span data-stu-id="df58c-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="df58c-135">Name</span><span class="sxs-lookup"><span data-stu-id="df58c-135">Name</span></span>                      | <span data-ttu-id="df58c-136">字元</span><span class="sxs-lookup"><span data-stu-id="df58c-136">Character</span></span>           | <span data-ttu-id="df58c-137">描述</span><span class="sxs-lookup"><span data-stu-id="df58c-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df58c-138">雙引號</span><span class="sxs-lookup"><span data-stu-id="df58c-138">Double quote</span></span><br/>   | <span data-ttu-id="df58c-139">"</span><span class="sxs-lookup"><span data-stu-id="df58c-139">"</span></span><br/>        | <span data-ttu-id="df58c-140">用來括住 ADsPath 的任何部分，其可能包含特殊字元，因此字串會以字面方式解讀。</span><span class="sxs-lookup"><span data-stu-id="df58c-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="df58c-141">例如，"CN = Name/Prefix"。</span><span class="sxs-lookup"><span data-stu-id="df58c-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="df58c-142">反斜線</span><span class="sxs-lookup"><span data-stu-id="df58c-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="df58c-143">用在特殊字元之前，表示它們應該當做常值使用。</span><span class="sxs-lookup"><span data-stu-id="df58c-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="df58c-144">如需詳細資訊和特殊字元清單，請參閱 [分辨名稱](/previous-versions/windows/desktop/ldap/distinguished-names)。</span><span class="sxs-lookup"><span data-stu-id="df58c-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="df58c-145">斜線</span><span class="sxs-lookup"><span data-stu-id="df58c-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="df58c-146">元件分隔符號。</span><span class="sxs-lookup"><span data-stu-id="df58c-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="df58c-147">角括號</span><span class="sxs-lookup"><span data-stu-id="df58c-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="df58c-148">在另一個命名慣例中分隔 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="df58c-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="df58c-149">若要在搜尋規格中分隔 ADsPath 或作為 URL 的一部分，請使用左和右角括弧 (< >) 。</span><span class="sxs-lookup"><span data-stu-id="df58c-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="df58c-150">例如，" &lt; WinNT://MyDomain/UserAccount &gt; "。</span><span class="sxs-lookup"><span data-stu-id="df58c-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="df58c-151">由於命名空間需求，某些 ADSI 提供者可能已新增語法限制。</span><span class="sxs-lookup"><span data-stu-id="df58c-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="df58c-152">Active Directory 系結選項</span><span class="sxs-lookup"><span data-stu-id="df58c-152">Active Directory Binding Options</span></span>

<span data-ttu-id="df58c-153">Active Directory 可讓您使用數種其他類型的系結字串系結至物件，例如 COM 全域唯一識別碼 (GUID) 或 (SID) 的安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="df58c-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="df58c-154">如需詳細資訊，請參閱系結 [至 Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services)。</span><span class="sxs-lookup"><span data-stu-id="df58c-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

