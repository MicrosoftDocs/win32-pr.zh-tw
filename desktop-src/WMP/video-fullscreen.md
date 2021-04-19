---
title: 全螢幕影片
description: 全螢幕屬性會指定或抓取值，指出影片是否以全螢幕模式顯示。
ms.assetid: de74d95a-31a2-4f65-811c-4e8018ee484a
keywords:
- VIDEO. 全螢幕 Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.fullScreen
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c27fa1bde6437b55689494751410145995862d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978789"
---
# <a name="videofullscreen"></a><span data-ttu-id="ff8ae-104">全螢幕影片</span><span class="sxs-lookup"><span data-stu-id="ff8ae-104">VIDEO.fullScreen</span></span>

<span data-ttu-id="ff8ae-105">**全** 螢幕屬性會指定或抓取值，指出影片是否以全螢幕模式顯示。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-105">The **fullScreen** attribute specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span>

``` syntax
        elementID.fullScreen
```

## <a name="possible-values"></a><span data-ttu-id="ff8ae-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="ff8ae-106">Possible Values</span></span>

<span data-ttu-id="ff8ae-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="ff8ae-108">值</span><span class="sxs-lookup"><span data-stu-id="ff8ae-108">Value</span></span> | <span data-ttu-id="ff8ae-109">描述</span><span class="sxs-lookup"><span data-stu-id="ff8ae-109">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="ff8ae-110">true</span><span class="sxs-lookup"><span data-stu-id="ff8ae-110">true</span></span>  | <span data-ttu-id="ff8ae-111">影片會以全螢幕模式顯示。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-111">Video displays in full-screen mode.</span></span>                  |
| <span data-ttu-id="ff8ae-112">false</span><span class="sxs-lookup"><span data-stu-id="ff8ae-112">false</span></span> | <span data-ttu-id="ff8ae-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-113">Default.</span></span> <span data-ttu-id="ff8ae-114">影片不會以全螢幕模式顯示。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-114">Video does not display in full-screen mode.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="ff8ae-115">備註</span><span class="sxs-lookup"><span data-stu-id="ff8ae-115">Remarks</span></span>

<span data-ttu-id="ff8ae-116">在載入檔案之後，才可以在執行時間指定此屬性。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-116">This property can be specified only at run time, after a file has been loaded.</span></span> <span data-ttu-id="ff8ae-117">因此，它必須在腳本事件處理常式內設定。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-117">It must therefore be set within a script event handler.</span></span> <span data-ttu-id="ff8ae-118">[Escape] 按鈕可用來返回一般的觀賞。</span><span class="sxs-lookup"><span data-stu-id="ff8ae-118">The escape button is used to return to normal viewing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff8ae-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff8ae-119">Requirements</span></span>



| <span data-ttu-id="ff8ae-120">需求</span><span class="sxs-lookup"><span data-stu-id="ff8ae-120">Requirement</span></span> | <span data-ttu-id="ff8ae-121">值</span><span class="sxs-lookup"><span data-stu-id="ff8ae-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ff8ae-122">版本</span><span class="sxs-lookup"><span data-stu-id="ff8ae-122">Version</span></span><br/> | <span data-ttu-id="ff8ae-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="ff8ae-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff8ae-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff8ae-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff8ae-125">**影片元素**</span><span class="sxs-lookup"><span data-stu-id="ff8ae-125">**VIDEO Element**</span></span>](video-element.md)
</dt> <dt>

[<span data-ttu-id="ff8ae-126">**MaintainAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="ff8ae-126">**VIDEO.maintainAspectRatio**</span></span>](video-maintainaspectratio.md)
</dt> <dt>

[<span data-ttu-id="ff8ae-127">**ShrinkToFit**</span><span class="sxs-lookup"><span data-stu-id="ff8ae-127">**VIDEO.shrinkToFit**</span></span>](video-shrinktofit.md)
</dt> <dt>

[<span data-ttu-id="ff8ae-128">**StretchToFit**</span><span class="sxs-lookup"><span data-stu-id="ff8ae-128">**VIDEO.stretchToFit**</span></span>](video-stretchtofit.md)
</dt> </dl>

 

 





