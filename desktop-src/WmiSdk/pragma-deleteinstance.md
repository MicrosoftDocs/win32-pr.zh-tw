---
description: 從存放庫中刪除類別的現有實例。
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026377"
---
# <a name="pragma-deleteinstance"></a><span data-ttu-id="5c472-103">pragma deleteinstance</span><span class="sxs-lookup"><span data-stu-id="5c472-103">pragma deleteinstance</span></span>

<span data-ttu-id="5c472-104">**Pragma deleteinstance** 命令會從存放庫中刪除類別的現有實例。</span><span class="sxs-lookup"><span data-stu-id="5c472-104">The **pragma deleteinstance** command deletes an existing instance of a class from the repository.</span></span>

<span data-ttu-id="5c472-105">以下說明此命令的語法：</span><span class="sxs-lookup"><span data-stu-id="5c472-105">The following describes the syntax for this command:</span></span>


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



<span data-ttu-id="5c472-106">*InstanceId* 是 MOF 編譯器從目前的命名空間中刪除之實例的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="5c472-106">*InstanceId* is a unique identifier of the instance the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="5c472-107">*\[ 旗 \]* 標必須是下列其中一個引數。</span><span class="sxs-lookup"><span data-stu-id="5c472-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="5c472-108">旗標</span><span class="sxs-lookup"><span data-stu-id="5c472-108">Flag</span></span>   | <span data-ttu-id="5c472-109">描述</span><span class="sxs-lookup"><span data-stu-id="5c472-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c472-110">失敗</span><span class="sxs-lookup"><span data-stu-id="5c472-110">fail</span></span>   | <span data-ttu-id="5c472-111">如果該類別不存在於存放庫中，則會導致 MOF 編譯器以錯誤訊息結束。</span><span class="sxs-lookup"><span data-stu-id="5c472-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="5c472-112">nofail</span><span class="sxs-lookup"><span data-stu-id="5c472-112">nofail</span></span> | <span data-ttu-id="5c472-113">即使類別不存在，也會使 MOF 編譯器繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5c472-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="5c472-114">範例</span><span class="sxs-lookup"><span data-stu-id="5c472-114">Examples</span></span>

<span data-ttu-id="5c472-115">下列範例顯示如何使用此命令。</span><span class="sxs-lookup"><span data-stu-id="5c472-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a><span data-ttu-id="5c472-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c472-116">Requirements</span></span>



| <span data-ttu-id="5c472-117">需求</span><span class="sxs-lookup"><span data-stu-id="5c472-117">Requirement</span></span> | <span data-ttu-id="5c472-118">值</span><span class="sxs-lookup"><span data-stu-id="5c472-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5c472-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c472-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c472-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c472-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5c472-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c472-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c472-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c472-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c472-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c472-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c472-124">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="5c472-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




