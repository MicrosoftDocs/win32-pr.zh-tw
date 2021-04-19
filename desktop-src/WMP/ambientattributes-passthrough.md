---
title: AmbientAttributes
description: 傳遞屬性會指定或抓取值，指出控制項是否會將所有滑鼠事件傳遞至其下的控制項。
ms.assetid: 907ae233-3421-4e80-84be-64db4a3ab654
keywords:
- AmbientAttributes 傳遞 Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.passThrough
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27b786aeefc182caab904c644dfd00ab4e76fec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987030"
---
# <a name="ambientattributespassthrough"></a><span data-ttu-id="c9719-104">AmbientAttributes</span><span class="sxs-lookup"><span data-stu-id="c9719-104">AmbientAttributes.passThrough</span></span>

<span data-ttu-id="c9719-105">**傳遞** 屬性會指定或抓取值，指出控制項是否會將所有滑鼠事件傳遞至其下的控制項。</span><span class="sxs-lookup"><span data-stu-id="c9719-105">The **passThrough** attribute specifies or retrieves a value indicating whether the control will pass all mouse events through to the control under it.</span></span>

``` syntax
        elementID.passThrough
```

## <a name="possible-values"></a><span data-ttu-id="c9719-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="c9719-106">Possible Values</span></span>

<span data-ttu-id="c9719-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="c9719-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="c9719-108">值</span><span class="sxs-lookup"><span data-stu-id="c9719-108">Value</span></span> | <span data-ttu-id="c9719-109">描述</span><span class="sxs-lookup"><span data-stu-id="c9719-109">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="c9719-110">true</span><span class="sxs-lookup"><span data-stu-id="c9719-110">true</span></span>  | <span data-ttu-id="c9719-111">控制權會將事件傳遞至其下的控制項。</span><span class="sxs-lookup"><span data-stu-id="c9719-111">Control passes events through to the control under it.</span></span> |
| <span data-ttu-id="c9719-112">false</span><span class="sxs-lookup"><span data-stu-id="c9719-112">false</span></span> | <span data-ttu-id="c9719-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="c9719-113">Default.</span></span> <span data-ttu-id="c9719-114">控制項不會透過傳遞事件。</span><span class="sxs-lookup"><span data-stu-id="c9719-114">Control does not pass events through.</span></span>         |



 

## <a name="remarks"></a><span data-ttu-id="c9719-115">備註</span><span class="sxs-lookup"><span data-stu-id="c9719-115">Remarks</span></span>

<span data-ttu-id="c9719-116">例如，如果文字控制項位於按鈕控制項上方，只提供標籤，這個屬性就很有用。</span><span class="sxs-lookup"><span data-stu-id="c9719-116">This attribute is useful if, for example, a text control sits on top of a button control only to provide labeling.</span></span> <span data-ttu-id="c9719-117">在此情況下，必須將文字控制項的按一下動作傳遞至按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="c9719-117">In this case, clicks on the text control must be passed through to the button control.</span></span>

<span data-ttu-id="c9719-118">**VIEW**、子 **視圖** 和 **播放清單** 元素不支援 **傳遞** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c9719-118">The **passThrough** attribute is not supported by the **VIEW**, **SUBVIEW**, and **PLAYLIST** elements.</span></span> <span data-ttu-id="c9719-119">如果 *影片* 是 **影片** 專案，它將無法使用。[**無視窗**] 會設定為 false，而效果元素 *則會* 設定為 [**效果**]。**視窗** 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="c9719-119">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if *EFFECTS*.**windowed** is set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9719-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9719-120">Requirements</span></span>



| <span data-ttu-id="c9719-121">需求</span><span class="sxs-lookup"><span data-stu-id="c9719-121">Requirement</span></span> | <span data-ttu-id="c9719-122">值</span><span class="sxs-lookup"><span data-stu-id="c9719-122">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c9719-123">版本</span><span class="sxs-lookup"><span data-stu-id="c9719-123">Version</span></span><br/> | <span data-ttu-id="c9719-124">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="c9719-124">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c9719-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9719-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9719-126">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="c9719-126">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





