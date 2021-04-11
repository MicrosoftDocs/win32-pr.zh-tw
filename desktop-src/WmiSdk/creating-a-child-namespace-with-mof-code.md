---
description: 建立命名空間最簡單的方式，就是使用受控物件格式 (MOF) 程式碼，在目前的目錄中建立命名空間。 當您登入時，會定義目前的目錄。
ms.assetid: 2b83cd96-079f-4178-9e5a-68ede3a92066
ms.tgt_platform: multiple
title: 使用 MOF 程式碼建立子命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f80aa04e2ef4f5c7bbfc43d9020727b3b2a6e0d
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104027692"
---
# <a name="creating-a-child-namespace-with-mof-code"></a><span data-ttu-id="65dc6-104">使用 MOF 程式碼建立子命名空間</span><span class="sxs-lookup"><span data-stu-id="65dc6-104">Creating a Child Namespace with MOF Code</span></span>

<span data-ttu-id="65dc6-105">建立命名空間最簡單的方式，就是使用受控物件格式 (MOF) 程式碼，在目前的目錄中建立命名空間。</span><span class="sxs-lookup"><span data-stu-id="65dc6-105">The simplest way of creating a namespace is to use Managed Object Format (MOF) code to create the namespace inside the current directory.</span></span> <span data-ttu-id="65dc6-106">當您登入時，會定義目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="65dc6-106">The current directory is defined when you log on.</span></span>

<span data-ttu-id="65dc6-107">下列程式說明如何使用 MOF 程式碼建立子命名空間。</span><span class="sxs-lookup"><span data-stu-id="65dc6-107">The following procedure describes how to create a child namespace using MOF code.</span></span>

<span data-ttu-id="65dc6-108">**使用 MOF 程式碼建立子命名空間**</span><span class="sxs-lookup"><span data-stu-id="65dc6-108">**To create a child namespace using MOF code**</span></span>

1.  <span data-ttu-id="65dc6-109">建立 [**\_ \_ 命名空間**](--namespace.md)類別的實例。</span><span class="sxs-lookup"><span data-stu-id="65dc6-109">Create an instance of the [**\_\_Namespace**](--namespace.md) class.</span></span>

    <span data-ttu-id="65dc6-110">下列程式碼範例顯示如何建立子命名空間。</span><span class="sxs-lookup"><span data-stu-id="65dc6-110">The following code example shows how to create a child namespace.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
    };
    ```

2.  <span data-ttu-id="65dc6-111">如果您想要要求使用者對命名空間進行加密的連接，請使用 **RequiresEncryption** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="65dc6-111">If you want to require the user to make an encrypted connection to the namespace, use the **RequiresEncryption** qualifier.</span></span> <span data-ttu-id="65dc6-112">如需詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="65dc6-112">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

    <span data-ttu-id="65dc6-113">下列程式碼範例示範如何要求加密的連接。</span><span class="sxs-lookup"><span data-stu-id="65dc6-113">The following code example shows how to require an encrypted connection.</span></span>

    ``` syntax
    instance of __Namespace 
    {
        Name = "MyNamespace";
        [RequiresEncryption(TRUE)] 
        instance of __MyNamespace { };
    };
    ```

3.  <span data-ttu-id="65dc6-114">如果您想要在命名空間上設定安全描述項，而不是使用預設的命名空間安全性，請使用 **NamespaceSecuritySDDL** 限定詞。</span><span class="sxs-lookup"><span data-stu-id="65dc6-114">If you want to set a security descriptor on the namespace rather than using the default namespace security, use the **NamespaceSecuritySDDL** qualifier.</span></span> <span data-ttu-id="65dc6-115">如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。</span><span class="sxs-lookup"><span data-stu-id="65dc6-115">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>

    <span data-ttu-id="65dc6-116">下列程式碼範例顯示如何在命名空間上設定安全描述項。</span><span class="sxs-lookup"><span data-stu-id="65dc6-116">The following code example shows how to set a security descriptor on the namespace.</span></span>

    ``` syntax
    #pragma namespace("\\\\.\\root\\MyNamespace")

    [NamespaceSecuritySDDL ("O:AUG:AUD:(A;CI;0x00060033;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

4.  <span data-ttu-id="65dc6-117">使用 [mofcomp.exe](mofcomp.md)公用程式或 [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)介面，編譯和載入 [**\_ \_ 命名空間**](--namespace.md)實例。</span><span class="sxs-lookup"><span data-stu-id="65dc6-117">Compile and load the [**\_\_Namespace**](--namespace.md) instance using the [mofcomp](mofcomp.md) utility or the [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) interface.</span></span> <span data-ttu-id="65dc6-118">Mofcomp.exe 和 **IMofCompiler** 介面都會將命名空間自動載入至目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="65dc6-118">Both mofcomp and the **IMofCompiler** interface automatically load the namespace into the current directory.</span></span> <span data-ttu-id="65dc6-119">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="65dc6-119">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="65dc6-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="65dc6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65dc6-121">**標準 WMI 限定詞**</span><span class="sxs-lookup"><span data-stu-id="65dc6-121">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> </dl>

 

 



