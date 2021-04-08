---
description: 要求編譯器將 MOF 檔案載入至指定為 namespacepath 的命名空間。 如果 MOF 編譯器-n 命名空間參數和 \# pragma 命名空間都&\# 32; namespacepath 命令，則命令優先于參數。
ms.assetid: d280f67a-a798-47c0-b8de-071c290dd216
ms.tgt_platform: multiple
title: pragma 命名空間
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: b5f5e164632fef5a41e7233caf4fd154d1dafe16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691520"
---
# <a name="pragma-namespace"></a><span data-ttu-id="27a1d-104">pragma 命名空間</span><span class="sxs-lookup"><span data-stu-id="27a1d-104">pragma namespace</span></span>

<span data-ttu-id="27a1d-105">**Pragma 命名空間** 預處理器命令要求編譯器將 MOF 檔案載入指定為 *namespacepath* 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="27a1d-105">The **pragma namespace** preprocessor command requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="27a1d-106">如果同時使用 MOF 編譯器 **-n** namespace 參數和 **\# pragma namespace** *namespacepath* 命令，則命令優先于參數。</span><span class="sxs-lookup"><span data-stu-id="27a1d-106">If both the MOF compiler **-n** namespace switch and the **\#pragma namespace** *namespacepath* command are used, the command takes priority over the switch.</span></span>

<span data-ttu-id="27a1d-107">以下說明語法：</span><span class="sxs-lookup"><span data-stu-id="27a1d-107">The following describes the syntax:</span></span>


```mof
#pragma namespace ("[Namespace]")
```



<span data-ttu-id="27a1d-108">*\[ 命名 \] 空間* 是指定的命名空間。</span><span class="sxs-lookup"><span data-stu-id="27a1d-108">*\[Namespace\]* is the specified namespace.</span></span>

<span data-ttu-id="27a1d-109">如果您未指定此命令或對等的命令列參數，MOF 編譯器預設會使用根 \\ 預設命名空間。</span><span class="sxs-lookup"><span data-stu-id="27a1d-109">If you do not specify this command or the equivalent command-line switch, the MOF compiler uses the root\\default namespace by default.</span></span>

## <a name="remarks"></a><span data-ttu-id="27a1d-110">備註</span><span class="sxs-lookup"><span data-stu-id="27a1d-110">Remarks</span></span>

<span data-ttu-id="27a1d-111">您可以要求用戶端腳本和應用程式使用加密的連接來進行驗證，方法是將 **RequiresEncryption** 限定詞新增至建立命名空間的 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="27a1d-111">You can require that client scripts and applications use an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the .mof file that creates the namespace.</span></span> <span data-ttu-id="27a1d-112">您也可以藉由新增這個屬性來修改現有的命名空間，然後再次編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="27a1d-112">You can also modify an existing namespace by adding this attribute and compile the MOF file again.</span></span> <span data-ttu-id="27a1d-113">如需如何使用 **RequiresEncryption** 的詳細資訊，請參閱 [要求命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)。</span><span class="sxs-lookup"><span data-stu-id="27a1d-113">For more information about how to use **RequiresEncryption**, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

## <a name="examples"></a><span data-ttu-id="27a1d-114">範例</span><span class="sxs-lookup"><span data-stu-id="27a1d-114">Examples</span></span>

<span data-ttu-id="27a1d-115">下列範例示範如何將類別或實例放在「根 \\ 測試」命名空間中。</span><span class="sxs-lookup"><span data-stu-id="27a1d-115">The following example shows how place classes or instances in the "Root\\Test" namespace.</span></span>


```mof
#pragma namespace ("\\\\.\\Root\\Test")
```



## <a name="requirements"></a><span data-ttu-id="27a1d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="27a1d-116">Requirements</span></span>



| <span data-ttu-id="27a1d-117">需求</span><span class="sxs-lookup"><span data-stu-id="27a1d-117">Requirement</span></span> | <span data-ttu-id="27a1d-118">值</span><span class="sxs-lookup"><span data-stu-id="27a1d-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="27a1d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27a1d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="27a1d-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27a1d-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="27a1d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27a1d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="27a1d-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27a1d-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="27a1d-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27a1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27a1d-124">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="27a1d-124">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="27a1d-125">**標準 WMI 限定詞**</span><span class="sxs-lookup"><span data-stu-id="27a1d-125">**Standard WMI Qualifiers**</span></span>](standard-wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="27a1d-126">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="27a1d-126">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




