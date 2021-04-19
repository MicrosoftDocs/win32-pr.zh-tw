---
title: IWMPControls2 步驟方法
description: Step 方法會讓目前的影片媒體專案進入下一個畫面格，或上一個畫面格，並凍結播放。
ms.assetid: c5cb720f-527f-45b6-ae8a-4da0e3e34618
keywords:
- 步驟方法 Windows Media Player
- 步驟方法 Windows Media Player，IWMPControls2 介面
- IWMPControls2 介面 Windows Media Player，step 方法
topic_type:
- apiref
api_name:
- IWMPControls2.step
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cfb65dd20de506a8f303121b23668e2fbf14dc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995474"
---
# <a name="iwmpcontrols2step-method"></a><span data-ttu-id="dd9b6-106">IWMPControls2：： step 方法</span><span class="sxs-lookup"><span data-stu-id="dd9b6-106">IWMPControls2::step method</span></span>

<span data-ttu-id="dd9b6-107">**Step** 方法會讓目前的影片媒體專案進入下一個畫面格，或上一個畫面格，並凍結播放。</span><span class="sxs-lookup"><span data-stu-id="dd9b6-107">The **step** method causes the current video media item to step to the next frame or the previous frame and freeze playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd9b6-108">語法</span><span class="sxs-lookup"><span data-stu-id="dd9b6-108">Syntax</span></span>


```CSharp
public void step(
  System.Int32 lStep
);
```


```VB

Public Sub step( _
  ByVal lStep As System.Int32 _
)
Implements IWMPControls2.step
```





## <a name="parameters"></a><span data-ttu-id="dd9b6-109">參數</span><span class="sxs-lookup"><span data-stu-id="dd9b6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd9b6-110">*lStep* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd9b6-110">*lStep* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd9b6-111">System.string **值，** 表示凍結前要執行的畫面格數目。</span><span class="sxs-lookup"><span data-stu-id="dd9b6-111">A **System.Int32** value indicating how many frames to step before freezing.</span></span> <span data-ttu-id="dd9b6-112">必須設定為1或-1。</span><span class="sxs-lookup"><span data-stu-id="dd9b6-112">Must be set to 1 or -1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd9b6-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd9b6-113">Return value</span></span>

<span data-ttu-id="dd9b6-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="dd9b6-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd9b6-115">備註</span><span class="sxs-lookup"><span data-stu-id="dd9b6-115">Remarks</span></span>

<span data-ttu-id="dd9b6-116">這個方法目前僅支援參數1或-1，因此您一次只能執行一個畫面格。</span><span class="sxs-lookup"><span data-stu-id="dd9b6-116">This method currently supports only the parameters 1 or -1, so you can only step one frame at a time.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd9b6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd9b6-117">Requirements</span></span>



| <span data-ttu-id="dd9b6-118">需求</span><span class="sxs-lookup"><span data-stu-id="dd9b6-118">Requirement</span></span> | <span data-ttu-id="dd9b6-119">值</span><span class="sxs-lookup"><span data-stu-id="dd9b6-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd9b6-120">版本</span><span class="sxs-lookup"><span data-stu-id="dd9b6-120">Version</span></span><br/>   | <span data-ttu-id="dd9b6-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="dd9b6-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="dd9b6-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="dd9b6-122">Namespace</span></span><br/> | <span data-ttu-id="dd9b6-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="dd9b6-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="dd9b6-124">組件</span><span class="sxs-lookup"><span data-stu-id="dd9b6-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="dd9b6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="dd9b6-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd9b6-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd9b6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd9b6-127">**IWMPControls2 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dd9b6-127">**IWMPControls2 Interface (VB and C#)**</span></span>](iwmpcontrols2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="dd9b6-128">**IWMPDVD 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="dd9b6-128">**IWMPDVD Interface (VB and C#)**</span></span>](iwmpdvd--vb-and-c.md)
</dt> </dl>

 

 





