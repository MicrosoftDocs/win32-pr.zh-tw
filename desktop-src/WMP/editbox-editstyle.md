---
title: 編輯方塊. editStyle
description: EditStyle 屬性會指定或抓取編輯方塊控制項的樣式。
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- 編輯方塊. editStyle Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999290"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="dd5cc-104">編輯方塊. editStyle</span><span class="sxs-lookup"><span data-stu-id="dd5cc-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="dd5cc-105">**EditStyle** 屬性會指定或抓取編輯方塊控制項的樣式。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="dd5cc-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="dd5cc-106">Possible Values</span></span>

<span data-ttu-id="dd5cc-107">這個屬性是包含下列其中一個值的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="dd5cc-108">值</span><span class="sxs-lookup"><span data-stu-id="dd5cc-108">Value</span></span>     | <span data-ttu-id="dd5cc-109">描述</span><span class="sxs-lookup"><span data-stu-id="dd5cc-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="dd5cc-110">正常</span><span class="sxs-lookup"><span data-stu-id="dd5cc-110">normal</span></span>    | <span data-ttu-id="dd5cc-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-111">Default.</span></span> <span data-ttu-id="dd5cc-112">在單一行上顯示一般文字。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="dd5cc-113">密碼</span><span class="sxs-lookup"><span data-stu-id="dd5cc-113">password</span></span>  | <span data-ttu-id="dd5cc-114"> () 顯示星號 \* 來取代文字。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="dd5cc-115">只能在設計階段指定。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="dd5cc-116">小寫</span><span class="sxs-lookup"><span data-stu-id="dd5cc-116">uppercase</span></span> | <span data-ttu-id="dd5cc-117">將文字顯示為全部大寫。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="dd5cc-118">小寫</span><span class="sxs-lookup"><span data-stu-id="dd5cc-118">lowercase</span></span> | <span data-ttu-id="dd5cc-119">將文字顯示為全部小寫。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="dd5cc-120">number</span><span class="sxs-lookup"><span data-stu-id="dd5cc-120">number</span></span>    | <span data-ttu-id="dd5cc-121">只會顯示數位。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="dd5cc-122">適用</span><span class="sxs-lookup"><span data-stu-id="dd5cc-122">multiline</span></span> | <span data-ttu-id="dd5cc-123">顯示多行文字。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-123">Displays multiple lines of text.</span></span> <span data-ttu-id="dd5cc-124">只能在設計階段指定。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="dd5cc-125">備註</span><span class="sxs-lookup"><span data-stu-id="dd5cc-125">Remarks</span></span>

<span data-ttu-id="dd5cc-126">這個屬性只能在設計階段設定為 "password" 或 "多行"。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="dd5cc-127">如果設定為 "多行"，就無法在執行時間變更該值。</span><span class="sxs-lookup"><span data-stu-id="dd5cc-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd5cc-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd5cc-128">Requirements</span></span>



| <span data-ttu-id="dd5cc-129">需求</span><span class="sxs-lookup"><span data-stu-id="dd5cc-129">Requirement</span></span> | <span data-ttu-id="dd5cc-130">值</span><span class="sxs-lookup"><span data-stu-id="dd5cc-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="dd5cc-131">版本</span><span class="sxs-lookup"><span data-stu-id="dd5cc-131">Version</span></span><br/> | <span data-ttu-id="dd5cc-132">適用于 Windows XP 或更新版本的 Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="dd5cc-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="dd5cc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd5cc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd5cc-134">**編輯方塊元素**</span><span class="sxs-lookup"><span data-stu-id="dd5cc-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





