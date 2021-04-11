---
description: 從存放庫中刪除現有的類別及其實例。
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852475"
---
# <a name="pragma-deleteclass"></a><span data-ttu-id="8c63a-103">pragma deleteclass</span><span class="sxs-lookup"><span data-stu-id="8c63a-103">pragma deleteclass</span></span>

<span data-ttu-id="8c63a-104">**Pragma deleteclass** 預處理器命令會從存放庫中刪除現有的類別及其實例。</span><span class="sxs-lookup"><span data-stu-id="8c63a-104">The **pragma deleteclass** preprocessor command deletes an existing class and its instances from the repository.</span></span>

<span data-ttu-id="8c63a-105">以下說明語法：</span><span class="sxs-lookup"><span data-stu-id="8c63a-105">The following describes the syntax:</span></span>


```mof
#pragma deleteclass("ClassName", [Flag])
```



<span data-ttu-id="8c63a-106">*ClassName* 是 MOF 編譯器從目前的命名空間中刪除之類別的名稱。</span><span class="sxs-lookup"><span data-stu-id="8c63a-106">*ClassName* is the name of the class that the MOF compiler deletes from the current namespace.</span></span>

<span data-ttu-id="8c63a-107">*\[ 旗 \]* 標必須是下列其中一個引數。</span><span class="sxs-lookup"><span data-stu-id="8c63a-107">*\[Flag\]* must be one of the following arguments.</span></span>



| <span data-ttu-id="8c63a-108">旗標</span><span class="sxs-lookup"><span data-stu-id="8c63a-108">Flag</span></span>   | <span data-ttu-id="8c63a-109">描述</span><span class="sxs-lookup"><span data-stu-id="8c63a-109">Description</span></span>                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c63a-110">失敗</span><span class="sxs-lookup"><span data-stu-id="8c63a-110">fail</span></span>   | <span data-ttu-id="8c63a-111">如果該類別不存在於存放庫中，則會導致 MOF 編譯器以錯誤訊息結束。</span><span class="sxs-lookup"><span data-stu-id="8c63a-111">Causes the MOF compiler to quit with an error message if the class does not already exist in the repository.</span></span> |
| <span data-ttu-id="8c63a-112">nofail</span><span class="sxs-lookup"><span data-stu-id="8c63a-112">nofail</span></span> | <span data-ttu-id="8c63a-113">即使類別不存在，也會使 MOF 編譯器繼續進行。</span><span class="sxs-lookup"><span data-stu-id="8c63a-113">Causes the MOF compiler to continue even if the class does not already exist.</span></span>                                |



 

## <a name="examples"></a><span data-ttu-id="8c63a-114">範例</span><span class="sxs-lookup"><span data-stu-id="8c63a-114">Examples</span></span>

<span data-ttu-id="8c63a-115">下列範例顯示如何使用此命令。</span><span class="sxs-lookup"><span data-stu-id="8c63a-115">The following example shows how to use this command.</span></span>


```mof
#pragma deleteclass("MyClass1",FAIL)
```



## <a name="requirements"></a><span data-ttu-id="8c63a-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c63a-116">Requirements</span></span>



| <span data-ttu-id="8c63a-117">需求</span><span class="sxs-lookup"><span data-stu-id="8c63a-117">Requirement</span></span> | <span data-ttu-id="8c63a-118">值</span><span class="sxs-lookup"><span data-stu-id="8c63a-118">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="8c63a-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c63a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="8c63a-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8c63a-120">Windows Vista</span></span><br/>       |
| <span data-ttu-id="8c63a-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c63a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="8c63a-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8c63a-122">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c63a-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c63a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c63a-124">預處理器命令</span><span class="sxs-lookup"><span data-stu-id="8c63a-124">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




