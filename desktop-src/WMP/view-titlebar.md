---
title: VIEW. 標題列
description: 標題列屬性會抓取值，指出是否顯示視窗標題列。
ms.assetid: 996aa2e0-0313-4a48-adcb-b82f76f38b6a
keywords:
- VIEW. 標題列 Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.titleBar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea225103913e3906cf6cd3b129943fbf9b9f165
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985560"
---
# <a name="viewtitlebar"></a><span data-ttu-id="3675a-104">VIEW. 標題列</span><span class="sxs-lookup"><span data-stu-id="3675a-104">VIEW.titleBar</span></span>

<span data-ttu-id="3675a-105">**標題** 欄屬性會抓取值，指出是否顯示視窗標題列。</span><span class="sxs-lookup"><span data-stu-id="3675a-105">The **titleBar** attribute retrieves a value indicating whether the window title bar is shown.</span></span>

``` syntax
        elementID.titleBar
```

## <a name="possible-values"></a><span data-ttu-id="3675a-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="3675a-106">Possible Values</span></span>

<span data-ttu-id="3675a-107">這個屬性是唯讀的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="3675a-107">This attribute is a read-only **Boolean**.</span></span>



| <span data-ttu-id="3675a-108">值</span><span class="sxs-lookup"><span data-stu-id="3675a-108">Value</span></span> | <span data-ttu-id="3675a-109">描述</span><span class="sxs-lookup"><span data-stu-id="3675a-109">Description</span></span>                             |
|-------|-----------------------------------------|
| <span data-ttu-id="3675a-110">true</span><span class="sxs-lookup"><span data-stu-id="3675a-110">true</span></span>  | <span data-ttu-id="3675a-111">預設值。</span><span class="sxs-lookup"><span data-stu-id="3675a-111">Default.</span></span> <span data-ttu-id="3675a-112">視窗標題列會顯示。</span><span class="sxs-lookup"><span data-stu-id="3675a-112">The window title bar is shown.</span></span> |
| <span data-ttu-id="3675a-113">false</span><span class="sxs-lookup"><span data-stu-id="3675a-113">false</span></span> | <span data-ttu-id="3675a-114">不會顯示視窗標題列。</span><span class="sxs-lookup"><span data-stu-id="3675a-114">The window title bar is not shown.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="3675a-115">備註</span><span class="sxs-lookup"><span data-stu-id="3675a-115">Remarks</span></span>

<span data-ttu-id="3675a-116">如果顯示標題列，則會顯示 [控制台]、[最小化] 和 [關閉] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="3675a-116">If the title bar is shown, the control box, minimize, and close buttons will be shown.</span></span> <span data-ttu-id="3675a-117">視窗的標題將會是 **VIEW** 元素的標題。</span><span class="sxs-lookup"><span data-stu-id="3675a-117">The title of the window will be the title of the **VIEW** element.</span></span>

<span data-ttu-id="3675a-118">如果 [ **標題** ] 設定為 [true]，而使用者嘗試變更 [ **視頻**] 的值，則不會進行變更，除非面板監視 **縮放比例** 並採取適當的動作來調整其本身的大小。</span><span class="sxs-lookup"><span data-stu-id="3675a-118">If **titleBar** is set to true and the user attempts to change the value of **Video.zoom**, the change will not take place unless the skin monitors **zoom** and takes appropriate action to resize itself.</span></span>

## <a name="requirements"></a><span data-ttu-id="3675a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3675a-119">Requirements</span></span>



| <span data-ttu-id="3675a-120">需求</span><span class="sxs-lookup"><span data-stu-id="3675a-120">Requirement</span></span> | <span data-ttu-id="3675a-121">值</span><span class="sxs-lookup"><span data-stu-id="3675a-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3675a-122">版本</span><span class="sxs-lookup"><span data-stu-id="3675a-122">Version</span></span><br/> | <span data-ttu-id="3675a-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="3675a-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3675a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3675a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3675a-125">**VIEW 元素**</span><span class="sxs-lookup"><span data-stu-id="3675a-125">**VIEW Element**</span></span>](view-element.md)
</dt> <dt>

[<span data-ttu-id="3675a-126">**VIEW. 標題**</span><span class="sxs-lookup"><span data-stu-id="3675a-126">**VIEW.title**</span></span>](view-title.md)
</dt> <dt>

[<span data-ttu-id="3675a-127">**影片。縮放**</span><span class="sxs-lookup"><span data-stu-id="3675a-127">**VIDEO.zoom**</span></span>](video-zoom.md)
</dt> </dl>

 

 





