---
title: IWMPControls2 (VB 和 C) 介面 (Wmp.h)
description: 提供補充 IWMPControls 介面的方法。
ms.assetid: 6a181911-9ab1-4cab-a6a2-9e1465f44029
keywords:
- IWMPControls2 (VB 和 C ) 介面 Windows Media Player
- IWMPControls2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPControls2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955ee2a8b18f1629427dfe45da802759901ab00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989824"
---
# <a name="iwmpcontrols2-vb-and-c-interface"></a><span data-ttu-id="f4f7b-105">IWMPControls2 (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="f4f7b-105">IWMPControls2 (VB and C#) interface</span></span>

<span data-ttu-id="f4f7b-106">提供補充 [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="f4f7b-106">Provides a method that supplements the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) interface.</span></span>

## <a name="members"></a><span data-ttu-id="f4f7b-107">成員</span><span class="sxs-lookup"><span data-stu-id="f4f7b-107">Members</span></span>

<span data-ttu-id="f4f7b-108">**IWMPControls2 (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f4f7b-108">The **IWMPControls2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="f4f7b-109">方法</span><span class="sxs-lookup"><span data-stu-id="f4f7b-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f4f7b-110">方法</span><span class="sxs-lookup"><span data-stu-id="f4f7b-110">Methods</span></span>

<span data-ttu-id="f4f7b-111">**IWMPControls2 (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="f4f7b-111">The **IWMPControls2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="f4f7b-112">方法</span><span class="sxs-lookup"><span data-stu-id="f4f7b-112">Method</span></span>                                                           | <span data-ttu-id="f4f7b-113">描述</span><span class="sxs-lookup"><span data-stu-id="f4f7b-113">Description</span></span>                                                                                                 |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4f7b-114">**步**</span><span class="sxs-lookup"><span data-stu-id="f4f7b-114">**step**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md) | <span data-ttu-id="f4f7b-115">將目前的影片媒體專案移至下一個畫面格，或移至上一個畫面格，並凍結播放。</span><span class="sxs-lookup"><span data-stu-id="f4f7b-115">Moves the current video media item to the next frame or the previous frame and freezes playback.</span></span><br/> |



 

<span data-ttu-id="f4f7b-116">下列範例程式碼顯示如何存取 [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) 介面。</span><span class="sxs-lookup"><span data-stu-id="f4f7b-116">The following example code shows how to access an [**IWMPControls2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2) interface.</span></span> <span data-ttu-id="f4f7b-117">範例程式碼會將 [**AxWindowsMediaPlayer Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md)屬性傳回的 [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)值轉換成 **IWMPControls2** 值。</span><span class="sxs-lookup"><span data-stu-id="f4f7b-117">The example code casts the [**IWMPControls**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols) value that the [**AxWindowsMediaPlayer.Ctlcontrols**](axwmplib-axwindowsmediaplayer-ctlcontrols--vb-and-c.md) property returns to a **IWMPControls2** value.</span></span>

<span data-ttu-id="f4f7b-118">若為 **c #**：</span><span class="sxs-lookup"><span data-stu-id="f4f7b-118">For **C#**:</span></span>


```CSharp
IWMPControls2 Ctlcontrols2 = (IWMPControls2)AxWindowsMediaPlayer.Ctlcontrols;
```



<span data-ttu-id="f4f7b-119">針對 **VB**：</span><span class="sxs-lookup"><span data-stu-id="f4f7b-119">For **VB**:</span></span>


```VB
Dim Ctlcontrols As WMPLib.IWMPControls = Me.AxWindowsMediaPlayer1.Ctlcontrols
Dim Ctlcontrols2 As WMPLib.IWMPControls2 = DirectCast(Ctlcontrols, WMPLib.IWMPControls2)
```



## <a name="requirements"></a><span data-ttu-id="f4f7b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4f7b-120">Requirements</span></span>



| <span data-ttu-id="f4f7b-121">需求</span><span class="sxs-lookup"><span data-stu-id="f4f7b-121">Requirement</span></span> | <span data-ttu-id="f4f7b-122">值</span><span class="sxs-lookup"><span data-stu-id="f4f7b-122">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="f4f7b-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f4f7b-123">Header</span></span><br/> | <dl> <span data-ttu-id="f4f7b-124"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4f7b-124"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4f7b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4f7b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4f7b-126">**IWMPControls**</span><span class="sxs-lookup"><span data-stu-id="f4f7b-126">**IWMPControls**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)
</dt> <dt>

[<span data-ttu-id="f4f7b-127">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="f4f7b-127">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4f7b-128">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4f7b-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f4f7b-129">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="f4f7b-129">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> </dl>

 

 





