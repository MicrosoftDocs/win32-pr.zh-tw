---
title: IWMPSettings setMode 方法
description: SetMode 方法會將迴圈模式或隨機模式設定為作用中或非作用中。
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setMode 方法 Windows Media Player
- setMode 方法 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，setMode 方法
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989258"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="d1359-106">IWMPSettings：： setMode 方法</span><span class="sxs-lookup"><span data-stu-id="d1359-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="d1359-107">**SetMode** 方法會將迴圈模式或隨機模式設定為作用中或非作用中。</span><span class="sxs-lookup"><span data-stu-id="d1359-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1359-108">語法</span><span class="sxs-lookup"><span data-stu-id="d1359-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="d1359-109">參數</span><span class="sxs-lookup"><span data-stu-id="d1359-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1359-110">*bstrMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1359-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1359-111">**System.string** ，這是要變更的模式名稱，其中包含下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="d1359-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="d1359-112">值</span><span class="sxs-lookup"><span data-stu-id="d1359-112">Value</span></span>      | <span data-ttu-id="d1359-113">描述</span><span class="sxs-lookup"><span data-stu-id="d1359-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1359-114">autoRewind</span><span class="sxs-lookup"><span data-stu-id="d1359-114">autoRewind</span></span> | <span data-ttu-id="d1359-115">播放結束之後，會從頭開始重新開機追蹤。</span><span class="sxs-lookup"><span data-stu-id="d1359-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="d1359-116">loop</span><span class="sxs-lookup"><span data-stu-id="d1359-116">loop</span></span>       | <span data-ttu-id="d1359-117">追蹤順序會自行重複。</span><span class="sxs-lookup"><span data-stu-id="d1359-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="d1359-118">showFrame</span><span class="sxs-lookup"><span data-stu-id="d1359-118">showFrame</span></span>  | <span data-ttu-id="d1359-119">未播放時，會顯示最接近的主要畫面格。</span><span class="sxs-lookup"><span data-stu-id="d1359-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="d1359-120">此模式與音訊播放軌無關。</span><span class="sxs-lookup"><span data-stu-id="d1359-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="d1359-121">隨機播放</span><span class="sxs-lookup"><span data-stu-id="d1359-121">shuffle</span></span>    | <span data-ttu-id="d1359-122">曲目會以隨機順序播放。</span><span class="sxs-lookup"><span data-stu-id="d1359-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="d1359-123">*varfMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d1359-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d1359-124">System.string **值，** 指定新指定的模式是否為使用中。</span><span class="sxs-lookup"><span data-stu-id="d1359-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1359-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="d1359-125">Return value</span></span>

<span data-ttu-id="d1359-126">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d1359-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1359-127">備註</span><span class="sxs-lookup"><span data-stu-id="d1359-127">Remarks</span></span>

<span data-ttu-id="d1359-128">當 showFrame 模式為使用中時，Windows Media Player 必須存取曲目內容才能取出影片畫面。</span><span class="sxs-lookup"><span data-stu-id="d1359-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="d1359-129">播放非本機的內容時，請謹慎使用這個模式。</span><span class="sxs-lookup"><span data-stu-id="d1359-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1359-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1359-130">Requirements</span></span>



| <span data-ttu-id="d1359-131">需求</span><span class="sxs-lookup"><span data-stu-id="d1359-131">Requirement</span></span> | <span data-ttu-id="d1359-132">值</span><span class="sxs-lookup"><span data-stu-id="d1359-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1359-133">版本</span><span class="sxs-lookup"><span data-stu-id="d1359-133">Version</span></span><br/>   | <span data-ttu-id="d1359-134">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="d1359-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d1359-135">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1359-135">Namespace</span></span><br/> | <span data-ttu-id="d1359-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="d1359-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d1359-137">組件</span><span class="sxs-lookup"><span data-stu-id="d1359-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d1359-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="d1359-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1359-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1359-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1359-140">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d1359-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d1359-141">**IWMPSettings. getMode (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="d1359-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





