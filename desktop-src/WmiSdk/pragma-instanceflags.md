---
description: 根據指定的旗標，控制建立或更新實例的方式。
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195058"
---
# <a name="pragma-instanceflags"></a><span data-ttu-id="fed16-103">pragma instanceflags</span><span class="sxs-lookup"><span data-stu-id="fed16-103">pragma instanceflags</span></span>

<span data-ttu-id="fed16-104">**Pragma instanceflags** 預處理器命令會根據指定的旗標，控制建立或更新實例的方式。</span><span class="sxs-lookup"><span data-stu-id="fed16-104">The **pragma instanceflags** preprocessor command controls the way instances are created or updated depending on the flags specified.</span></span>

<span data-ttu-id="fed16-105">以下說明語法：</span><span class="sxs-lookup"><span data-stu-id="fed16-105">The following describes the syntax:</span></span>


```mof
#pragma instanceflags ([Flag])
```



<span data-ttu-id="fed16-106">*\[ 旗 \]* 標必須是下列其中一個引數。</span><span class="sxs-lookup"><span data-stu-id="fed16-106">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="fed16-107">旗標</span><span class="sxs-lookup"><span data-stu-id="fed16-107">Flag</span></span>       | <span data-ttu-id="fed16-108">描述</span><span class="sxs-lookup"><span data-stu-id="fed16-108">Description</span></span>                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed16-109">以</span><span class="sxs-lookup"><span data-stu-id="fed16-109">createonly</span></span> | <span data-ttu-id="fed16-110">防止編譯器變更 MOF 檔案中的任何現有實例。</span><span class="sxs-lookup"><span data-stu-id="fed16-110">Prevents the compiler from changing any existing instances in the MOF file.</span></span>                                |
| <span data-ttu-id="fed16-111">updateonly</span><span class="sxs-lookup"><span data-stu-id="fed16-111">updateonly</span></span> | <span data-ttu-id="fed16-112">防止編譯器在 MOF 檔案中指定的實例不存在時建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="fed16-112">Prevents the compiler from creating new instances if an instance specified in the MOF file does not exist.</span></span> |



 

## <a name="examples"></a><span data-ttu-id="fed16-113">範例</span><span class="sxs-lookup"><span data-stu-id="fed16-113">Examples</span></span>

<span data-ttu-id="fed16-114">下列範例顯示如何使用此命令。</span><span class="sxs-lookup"><span data-stu-id="fed16-114">The following example shows how to use this command.</span></span>


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a><span data-ttu-id="fed16-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fed16-115">Requirements</span></span>



| <span data-ttu-id="fed16-116">需求</span><span class="sxs-lookup"><span data-stu-id="fed16-116">Requirement</span></span> | <span data-ttu-id="fed16-117">值</span><span class="sxs-lookup"><span data-stu-id="fed16-117">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fed16-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fed16-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fed16-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fed16-119">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fed16-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fed16-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fed16-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fed16-121">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fed16-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fed16-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed16-123">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="fed16-123">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




