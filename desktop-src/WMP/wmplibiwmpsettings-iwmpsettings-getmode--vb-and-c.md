---
title: IWMPSettings getMode 方法
description: GetMode 方法會傳回值，指出迴圈模式或隨機播放模式是否為使用中狀態。
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- getMode 方法 Windows Media Player
- getMode 方法 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，getMode 方法
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994053"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="05f00-106">IWMPSettings：： getMode 方法</span><span class="sxs-lookup"><span data-stu-id="05f00-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="05f00-107">**GetMode** 方法會傳回值，指出迴圈模式或隨機播放模式是否為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="05f00-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="05f00-108">語法</span><span class="sxs-lookup"><span data-stu-id="05f00-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="05f00-109">參數</span><span class="sxs-lookup"><span data-stu-id="05f00-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05f00-110">*bstrMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="05f00-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05f00-111">**System.string** ，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="05f00-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="05f00-112">值</span><span class="sxs-lookup"><span data-stu-id="05f00-112">Value</span></span>      | <span data-ttu-id="05f00-113">描述</span><span class="sxs-lookup"><span data-stu-id="05f00-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f00-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="05f00-114">autoRewind</span></span> | <span data-ttu-id="05f00-115">播放結束之後，會從頭開始重新開機追蹤。</span><span class="sxs-lookup"><span data-stu-id="05f00-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="05f00-116">loop</span><span class="sxs-lookup"><span data-stu-id="05f00-116">loop</span></span>       | <span data-ttu-id="05f00-117">追蹤順序會自行重複。</span><span class="sxs-lookup"><span data-stu-id="05f00-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="05f00-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="05f00-118">showFrame</span></span>  | <span data-ttu-id="05f00-119">未播放時，會顯示最接近的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="05f00-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="05f00-120">此模式與音訊播放軌無關。</span><span class="sxs-lookup"><span data-stu-id="05f00-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="05f00-121">隨機播放</span><span class="sxs-lookup"><span data-stu-id="05f00-121">shuffle</span></span>    | <span data-ttu-id="05f00-122">曲目會以隨機順序播放。</span><span class="sxs-lookup"><span data-stu-id="05f00-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05f00-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="05f00-123">Return value</span></span>

<span data-ttu-id="05f00-124">System.string **值，** 指出指定的模式是否為使用中。</span><span class="sxs-lookup"><span data-stu-id="05f00-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="05f00-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="05f00-125">Requirements</span></span>



| <span data-ttu-id="05f00-126">需求</span><span class="sxs-lookup"><span data-stu-id="05f00-126">Requirement</span></span> | <span data-ttu-id="05f00-127">值</span><span class="sxs-lookup"><span data-stu-id="05f00-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05f00-128">版本</span><span class="sxs-lookup"><span data-stu-id="05f00-128">Version</span></span><br/>   | <span data-ttu-id="05f00-129">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="05f00-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="05f00-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="05f00-130">Namespace</span></span><br/> | <span data-ttu-id="05f00-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="05f00-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="05f00-132">組件</span><span class="sxs-lookup"><span data-stu-id="05f00-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="05f00-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="05f00-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05f00-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05f00-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05f00-135">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="05f00-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="05f00-136">**IWMPSettings. setMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="05f00-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





