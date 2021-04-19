---
title: AmbientAttributes. zIndex
description: ZIndex 屬性會指定或抓取控制項的呈現順序。
ms.assetid: b05c9efc-5d1d-4cba-89f4-b4200ce99e09
keywords:
- AmbientAttributes. zIndex Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.zIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52480cc387c0a9e5e45c4b8e8fd2dae4199dbd16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996439"
---
# <a name="ambientattributeszindex"></a><span data-ttu-id="f6989-104">AmbientAttributes. zIndex</span><span class="sxs-lookup"><span data-stu-id="f6989-104">AmbientAttributes.zIndex</span></span>

<span data-ttu-id="f6989-105">**ZIndex** 屬性會指定或抓取控制項的呈現順序。</span><span class="sxs-lookup"><span data-stu-id="f6989-105">The **zIndex** attribute specifies or retrieves the order in which the control is rendered.</span></span>

``` syntax
        elementID.zIndex
```

## <a name="possible-values"></a><span data-ttu-id="f6989-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="f6989-106">Possible Values</span></span>

<span data-ttu-id="f6989-107">此屬性是讀取/寫入 **號碼** (**長**) ，預設值為零。</span><span class="sxs-lookup"><span data-stu-id="f6989-107">This attribute is a read/write **Number** (**long**) with a default value of zero.</span></span> <span data-ttu-id="f6989-108">範圍是帶正負號長整數的範圍。</span><span class="sxs-lookup"><span data-stu-id="f6989-108">The range is that of a signed long integer.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6989-109">備註</span><span class="sxs-lookup"><span data-stu-id="f6989-109">Remarks</span></span>

<span data-ttu-id="f6989-110">**視圖\*\*\*\*或子視圖的** 背景點陣圖具有固定的 z 索引（零）。</span><span class="sxs-lookup"><span data-stu-id="f6989-110">The background bitmap of a **VIEW** or **SUBVIEW** has a fixed z index of zero.</span></span> <span data-ttu-id="f6989-111">如果您希望控制項位於背景後方， **zIndex** 必須設定為負數。</span><span class="sxs-lookup"><span data-stu-id="f6989-111">If you want a control to be behind the background, the **zIndex** must be set to a negative number.</span></span>

<span data-ttu-id="f6989-112">**視圖\*\*\*\*或子視圖的** z 索引是絕對索引，而控制項的 z 索引是相對於包含它的視圖 **或子\*\*\*\*視圖** 的 z 索引。</span><span class="sxs-lookup"><span data-stu-id="f6989-112">The z index of a **VIEW** or **SUBVIEW** is an absolute index, while the z index of a control is relative to the z index of the **VIEW** or **SUBVIEW** that contains it.</span></span>

<span data-ttu-id="f6989-113">**瀏覽器** 和 **播放清單** 元素不支援 **zIndex** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6989-113">The **zIndex** attribute is not supported by the **BROWSER** and **PLAYLIST** elements.</span></span> <span data-ttu-id="f6989-114">如果 *影片* 是 **影片** 專案，它將無法使用。[**無視窗**] 會設定為 false，而效果元素 **則會** 設定為 [**效果**]。**視窗** 設定為 true。</span><span class="sxs-lookup"><span data-stu-id="f6989-114">It will not work with the **VIDEO** element if *VIDEO*.**windowless** is set to false, nor with the **EFFECTS** element if **EFFECTS**.**windowed** is set to true.</span></span>

<span data-ttu-id="f6989-115">**BUTTONELEMENT** 元素會使用其 **BUTTONGROUP** 的 **zIndex** 。</span><span class="sxs-lookup"><span data-stu-id="f6989-115">**BUTTONELEMENT** elements use the **zIndex** of their **BUTTONGROUP**.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6989-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6989-116">Requirements</span></span>



| <span data-ttu-id="f6989-117">需求</span><span class="sxs-lookup"><span data-stu-id="f6989-117">Requirement</span></span> | <span data-ttu-id="f6989-118">值</span><span class="sxs-lookup"><span data-stu-id="f6989-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f6989-119">版本</span><span class="sxs-lookup"><span data-stu-id="f6989-119">Version</span></span><br/> | <span data-ttu-id="f6989-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="f6989-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6989-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6989-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6989-122">**環境屬性**</span><span class="sxs-lookup"><span data-stu-id="f6989-122">**Ambient Attributes**</span></span>](ambient-attributes.md)
</dt> </dl>

 

 





