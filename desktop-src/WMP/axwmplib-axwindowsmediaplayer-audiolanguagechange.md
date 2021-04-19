---
title: AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件
description: 當目前的音訊語言變更時，就會發生 AudioLanguageChange 事件。 |AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件
ms.assetid: 35e4ff82-fc59-4d28-b7fc-1527fb46b960
keywords:
- AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件 Windows Media Player
topic_type:
- apiref
api_name:
- AudioLanguageChange Event of the AxWindowsMediaPlayer Object
api_location:
- AxInterop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 354a34f30df237827e3d369721963ec2c1797e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986142"
---
# <a name="audiolanguagechange-event-of-the-axwindowsmediaplayer-object"></a><span data-ttu-id="7af62-105">AxWindowsMediaPlayer 物件的 AudioLanguageChange 事件</span><span class="sxs-lookup"><span data-stu-id="7af62-105">AudioLanguageChange Event of the AxWindowsMediaPlayer Object</span></span>

<span data-ttu-id="7af62-106">當目前的音訊語言變更時，就會發生 AudioLanguageChange 事件。</span><span class="sxs-lookup"><span data-stu-id="7af62-106">The AudioLanguageChange event occurs when the current audio language changes.</span></span>

``` syntax
[C#]
private void player_AudioLanguageChange(
  object sender,
  _WMPOCXEvents_AudioLanguageChangeEvent e
)

[Visual Basic]
Private Sub player_AudioLanguageChange(
  sender As Object,
  e As _WMPOCXEvents_AudioLanguageChangeEvent
) Handles player.AudioLanguageChange
```

## <a name="event-data"></a><span data-ttu-id="7af62-107">事件資料</span><span class="sxs-lookup"><span data-stu-id="7af62-107">Event Data</span></span>

<span data-ttu-id="7af62-108">與這個事件相關聯的處理常式屬於 **AxWMPLib 型別。 \_WMPOCXEvents \_ AudioLanguageChangeEventHandler**。</span><span class="sxs-lookup"><span data-stu-id="7af62-108">The handler associated with this event is of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEventHandler**.</span></span> <span data-ttu-id="7af62-109">這個處理常式會接收 AxWMPLib 型別的引數 **。 \_WMPOCXEvents \_ AudioLanguageChangeEvent**，其中包含與這個事件相關的下列屬性。</span><span class="sxs-lookup"><span data-stu-id="7af62-109">This handler receives an argument of type **AxWMPLib.\_WMPOCXEvents\_AudioLanguageChangeEvent**, which contains the following property related to this event.</span></span>



| <span data-ttu-id="7af62-110">屬性</span><span class="sxs-lookup"><span data-stu-id="7af62-110">Property</span></span>   | <span data-ttu-id="7af62-111">描述</span><span class="sxs-lookup"><span data-stu-id="7af62-111">Description</span></span>                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af62-112">**langID**</span><span class="sxs-lookup"><span data-stu-id="7af62-112">**langID**</span></span> | <span data-ttu-id="7af62-113">**System.object** 唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="7af62-113">**System.Int32** Uniquely identifies a particular language dialect, called a locale.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7af62-114">備註</span><span class="sxs-lookup"><span data-stu-id="7af62-114">Remarks</span></span>

<span data-ttu-id="7af62-115">地區設定識別碼 (LCID) 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="7af62-115">A locale identifier (LCID) uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="7af62-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7af62-116">Requirements</span></span>



| <span data-ttu-id="7af62-117">需求</span><span class="sxs-lookup"><span data-stu-id="7af62-117">Requirement</span></span> | <span data-ttu-id="7af62-118">值</span><span class="sxs-lookup"><span data-stu-id="7af62-118">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7af62-119">版本</span><span class="sxs-lookup"><span data-stu-id="7af62-119">Version</span></span><br/>   | <span data-ttu-id="7af62-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="7af62-120">Windows Media Player 9 Series or later</span></span><br/>                                                                          |
| <span data-ttu-id="7af62-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="7af62-121">Namespace</span></span><br/> | <span data-ttu-id="7af62-122">**AxWMPLib**</span><span class="sxs-lookup"><span data-stu-id="7af62-122">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="7af62-123">組件</span><span class="sxs-lookup"><span data-stu-id="7af62-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="7af62-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="7af62-124"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7af62-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7af62-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7af62-126">**AxWindowsMediaPlayer 物件 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="7af62-126">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="7af62-127">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="7af62-127">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> </dl>

 

 





