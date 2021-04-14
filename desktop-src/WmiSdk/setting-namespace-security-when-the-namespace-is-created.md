---
title: 設定命名空間建立時的安全性
description: 建立命名空間的受控物件格式 (MOF) 檔也可以定義命名空間的安全描述項，方法是將 NamespaceSecuritySDDL 限定詞包含在安全描述項定義語言 (SDDL) 格式的安全描述項中。
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514085"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="26d47-103">設定命名空間建立時的安全性</span><span class="sxs-lookup"><span data-stu-id="26d47-103">Setting security on namespace creation</span></span>

<span data-ttu-id="26d47-104">建立命名空間的受控物件格式 (MOF) 檔也可以定義命名空間的 [*安全描述項*](/windows/desktop/SecGloss/s-gly) ，方法是將 **NamespaceSecuritySDDL** 限定詞包含在 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) 格式的安全描述項中。</span><span class="sxs-lookup"><span data-stu-id="26d47-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="26d47-105">您可以使用 **NamespaceSecuritySDDL** 來保護任何命名空間。</span><span class="sxs-lookup"><span data-stu-id="26d47-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="26d47-106">您也可以在簡單的 MOF 檔案中使用這個辨識符號，以改變現有命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="26d47-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="26d47-107">SDDL 字串是由 WMI 處理來建立命名空間安全性，但不會儲存為字串。</span><span class="sxs-lookup"><span data-stu-id="26d47-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="26d47-108">如果未指定任何安全描述項，則會使用預設安全性。</span><span class="sxs-lookup"><span data-stu-id="26d47-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="26d47-109">如需詳細資訊，請參閱 [設定命名空間安全描述項](setting-namespace-security-descriptors.md)。</span><span class="sxs-lookup"><span data-stu-id="26d47-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="26d47-110">下列程式會設定 *根 \\ MyNamespace* 命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="26d47-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="26d47-111">SDDL 字串會將擁有者和群組設定為已驗證的使用者，並指定子命名空間繼承 [*(DACL) 的任意存取控制清單*](/windows/desktop/SecGloss/d-gly) 。</span><span class="sxs-lookup"><span data-stu-id="26d47-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="26d47-112">DACL 可讓使用者讀取資料、執行方法、將資料寫入提供者類別，以及使用遠端存取： **wbem \_ 啟用**、 **wbem \_ 方法 \_ 執行**、 **wbem \_ 寫入 \_ 提供者**、 **wbem \_ 遠端 \_ 訪問**。</span><span class="sxs-lookup"><span data-stu-id="26d47-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="26d47-113">如需詳細資訊，請參閱 [WMI 命名空間的存取](access-to-wmi-namespaces.md)。</span><span class="sxs-lookup"><span data-stu-id="26d47-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="26d47-114">**設定命名空間 DACL**</span><span class="sxs-lookup"><span data-stu-id="26d47-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="26d47-115">建立受控物件格式 (MOF) 檔或修改現有的 MOF 檔案，該檔案會定義命名空間，以使用 SDDL 字串來新增 **NamespaceSecuritySDDL** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="26d47-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="26d47-116">下列程式碼範例顯示要修改的命名空間是根 \\ MyNamespace，而檔案的名稱為 MyNamespace \_ security. mof。</span><span class="sxs-lookup"><span data-stu-id="26d47-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="26d47-117">請注意，SDDL 字串會區分大小寫：字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="26d47-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="26d47-118">下列程式碼範例會將 SDDL 字串中的字母 "o" 和 "g" 顯示為小寫，而且會導致 Mofcomp.exe 傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="26d47-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="26d47-119">執行 [**Mofcomp.exe**](mofcomp.md) 以編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="26d47-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="26d47-120">**c： \\ Mofcomp.exe MyNamespace \_ security. mof**</span><span class="sxs-lookup"><span data-stu-id="26d47-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="26d47-121">在 c + + 中，請使用 [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) 方法。</span><span class="sxs-lookup"><span data-stu-id="26d47-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="26d47-122">如果您嘗試設定命名空間 DACL 失敗，請考慮下列錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="26d47-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="26d47-123">錯誤</span><span class="sxs-lookup"><span data-stu-id="26d47-123">Error</span></span>                           | <span data-ttu-id="26d47-124">描述</span><span class="sxs-lookup"><span data-stu-id="26d47-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="26d47-125">**WBEM \_ E \_ 不正確 \_ 參數**</span><span class="sxs-lookup"><span data-stu-id="26d47-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="26d47-126">沒有繼承的 DACL。</span><span class="sxs-lookup"><span data-stu-id="26d47-126">There is no inherited DACL.</span></span> <span data-ttu-id="26d47-127">或者，呼叫端違反了父命名空間中的 DACL 或 SD。</span><span class="sxs-lookup"><span data-stu-id="26d47-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="26d47-128">**WBEM \_ E \_ \_ 拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="26d47-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="26d47-129">呼叫端沒有在 MOF 中更新 SDDL 的許可權。</span><span class="sxs-lookup"><span data-stu-id="26d47-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="26d47-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="26d47-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26d47-131">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="26d47-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="26d47-132">**命名空間存取權限常數**</span><span class="sxs-lookup"><span data-stu-id="26d47-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="26d47-133">**命名空間 ACE 旗標常數**</span><span class="sxs-lookup"><span data-stu-id="26d47-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="26d47-134">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="26d47-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
