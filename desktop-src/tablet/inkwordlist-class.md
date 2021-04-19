---
description: 表示可以用來改善辨識結果的單字清單。
ms.assetid: d189fd13-ec69-45dc-8be4-fea48f337636
title: 'InkWordList 類別 (Msinkaut) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkWordList
- InkWordList.IInkWordList
api_type:
- COM
api_location:
- InkObj.dll
- InkObj.dll.dll
ms.openlocfilehash: 7f3bbf077758bfd0449f5bca1ba3739342fa3658
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984240"
---
# <a name="inkwordlist-class"></a><span data-ttu-id="42a09-103">InkWordList 類別</span><span class="sxs-lookup"><span data-stu-id="42a09-103">InkWordList class</span></span>

<span data-ttu-id="42a09-104">表示可以用來改善辨識結果的單字清單。</span><span class="sxs-lookup"><span data-stu-id="42a09-104">Represents a list of words that can be used to improve the recognition result.</span></span>

<span data-ttu-id="42a09-105">**InkWordList** 具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="42a09-105">**InkWordList** has these types of members:</span></span>

-   [<span data-ttu-id="42a09-106">介面</span><span class="sxs-lookup"><span data-stu-id="42a09-106">Interfaces</span></span>](#interfaces)
-   [<span data-ttu-id="42a09-107">方法</span><span class="sxs-lookup"><span data-stu-id="42a09-107">Methods</span></span>](#methods)

### <a name="interfaces"></a><span data-ttu-id="42a09-108">介面</span><span class="sxs-lookup"><span data-stu-id="42a09-108">Interfaces</span></span>

<span data-ttu-id="42a09-109">**InkWordList** 類別會定義這些介面。</span><span class="sxs-lookup"><span data-stu-id="42a09-109">The **InkWordList** class defines these interfaces.</span></span>



| <span data-ttu-id="42a09-110">介面</span><span class="sxs-lookup"><span data-stu-id="42a09-110">Interface</span></span>        | <span data-ttu-id="42a09-111">描述</span><span class="sxs-lookup"><span data-stu-id="42a09-111">Description</span></span>                                                           |
|:-----------------|:----------------------------------------------------------------------|
| <span data-ttu-id="42a09-112">**IInkWordList**</span><span class="sxs-lookup"><span data-stu-id="42a09-112">**IInkWordList**</span></span> | <span data-ttu-id="42a09-113">這個物件會實 **IInkWordList** COM 介面。</span><span class="sxs-lookup"><span data-stu-id="42a09-113">This object implements the **IInkWordList** COM interface.</span></span><br/> |



 

### <a name="methods"></a><span data-ttu-id="42a09-114">方法</span><span class="sxs-lookup"><span data-stu-id="42a09-114">Methods</span></span>

<span data-ttu-id="42a09-115">**InkWordList** 類別有這些方法。</span><span class="sxs-lookup"><span data-stu-id="42a09-115">The **InkWordList** class has these methods.</span></span>



| <span data-ttu-id="42a09-116">方法</span><span class="sxs-lookup"><span data-stu-id="42a09-116">Method</span></span>                                       | <span data-ttu-id="42a09-117">描述</span><span class="sxs-lookup"><span data-stu-id="42a09-117">Description</span></span>                                                             |
|:---------------------------------------------|:------------------------------------------------------------------------|
| [<span data-ttu-id="42a09-118">**AddWord**</span><span class="sxs-lookup"><span data-stu-id="42a09-118">**AddWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-addword)       | <span data-ttu-id="42a09-119">將單一單字加入至 **InkWordList**。</span><span class="sxs-lookup"><span data-stu-id="42a09-119">Adds a single word to the **InkWordList**.</span></span><br/>                   |
| [<span data-ttu-id="42a09-120">**合併**</span><span class="sxs-lookup"><span data-stu-id="42a09-120">**Merge**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-merge)           | <span data-ttu-id="42a09-121">將另一個 **InkWordList** 合併到這個 **InkWordList** 中。</span><span class="sxs-lookup"><span data-stu-id="42a09-121">Merges another **InkWordList** to into this **InkWordList**.</span></span><br/> |
| [<span data-ttu-id="42a09-122">**RemoveWord**</span><span class="sxs-lookup"><span data-stu-id="42a09-122">**RemoveWord**</span></span>](/windows/win32/api/msinkaut/nf-msinkaut-iinkwordlist-removeword) | <span data-ttu-id="42a09-123">從 **InkWordList** 中移除單一單字。</span><span class="sxs-lookup"><span data-stu-id="42a09-123">Removes a single word from a **InkWordList**.</span></span><br/>                |



 

## <a name="remarks"></a><span data-ttu-id="42a09-124">備註</span><span class="sxs-lookup"><span data-stu-id="42a09-124">Remarks</span></span>

<span data-ttu-id="42a09-125">此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。</span><span class="sxs-lookup"><span data-stu-id="42a09-125">This object can be instantiated by calling the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) method in C++.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a09-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="42a09-126">Requirements</span></span>



| <span data-ttu-id="42a09-127">需求</span><span class="sxs-lookup"><span data-stu-id="42a09-127">Requirement</span></span> | <span data-ttu-id="42a09-128">值</span><span class="sxs-lookup"><span data-stu-id="42a09-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42a09-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="42a09-129">Minimum supported client</span></span><br/> | <span data-ttu-id="42a09-130">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="42a09-130">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="42a09-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="42a09-131">Minimum supported server</span></span><br/> | <span data-ttu-id="42a09-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="42a09-132">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="42a09-133">標頭</span><span class="sxs-lookup"><span data-stu-id="42a09-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="42a09-134"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="42a09-134"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="42a09-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="42a09-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="42a09-136"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="42a09-136"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="42a09-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42a09-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42a09-138">**單詞表屬性**</span><span class="sxs-lookup"><span data-stu-id="42a09-138">**WordList Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist)
</dt> <dt>

[<span data-ttu-id="42a09-139">模擬常數</span><span class="sxs-lookup"><span data-stu-id="42a09-139">Factoid Constants</span></span>](factoid-constants.md)
</dt> <dt>

[<span data-ttu-id="42a09-140">**InkRecognizerCoNtext 類別**</span><span class="sxs-lookup"><span data-stu-id="42a09-140">**InkRecognizerContext Class**</span></span>](inkrecognizercontext-class.md)
</dt> </dl>

 

