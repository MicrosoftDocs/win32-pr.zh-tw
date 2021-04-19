---
title: IWMPSettings autoStart 屬性
description: AutoStart 屬性會取得或設定值，指出目前的媒體專案是否會自動開始播放。
ms.assetid: 01a1cb78-9951-478a-8ea3-1ae06164beab
keywords:
- autoStart 屬性 Windows Media Player
- autoStart 屬性 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player、autoStart 屬性
topic_type:
- apiref
api_name:
- IWMPSettings.autoStart
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6c1fb43107df11462737286e26fa7801360d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997774"
---
# <a name="iwmpsettingsautostart-property"></a><span data-ttu-id="bd0db-106">IWMPSettings：： autoStart 屬性</span><span class="sxs-lookup"><span data-stu-id="bd0db-106">IWMPSettings::autoStart property</span></span>

<span data-ttu-id="bd0db-107">**AutoStart** 屬性會取得或設定值，指出目前的媒體專案是否會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="bd0db-107">The **autoStart** property gets or sets a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd0db-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd0db-108">Syntax</span></span>


```CSharp
public System.Boolean autoStart {get; set;}
```


```VB

Public Property autoStart As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="bd0db-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd0db-109">Property value</span></span>

<span data-ttu-id="bd0db-110">System.string **值，** 指出目前的媒體專案是否會自動開始播放。</span><span class="sxs-lookup"><span data-stu-id="bd0db-110">A **System.Boolean** value that indicates whether the current media item begins playing automatically.</span></span> <span data-ttu-id="bd0db-111">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="bd0db-111">The default is **true**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd0db-112">備註</span><span class="sxs-lookup"><span data-stu-id="bd0db-112">Remarks</span></span>

<span data-ttu-id="bd0db-113">如果 **自動啟動** 設定為 **true** **，則在** 設定 **AxWindowsMediaPlayer\*\*\*\*時，會** 開始播放媒體專案。</span><span class="sxs-lookup"><span data-stu-id="bd0db-113">If **autoStart** is set to **true**, the media item will begin playing when **AxWindowsMediaPlayer.URL**, **AxWindowsMediaPlayer.currentPlaylist**, or **AxWindowsMediaPlayer.currentMedia** is set.</span></span> <span data-ttu-id="bd0db-114">否則，在呼叫 **IWMPControls** 方法之前，媒體專案將不會開始播放。</span><span class="sxs-lookup"><span data-stu-id="bd0db-114">Otherwise, the media item will not start playing until the **IWMPControls.play** method is called.</span></span>

<span data-ttu-id="bd0db-115">除非您在指定媒體專案之前立即將 **自動啟動** 設定為 **true** ，否則您不應該依賴這項設定來替代使用 **IWMPControls** 方法。</span><span class="sxs-lookup"><span data-stu-id="bd0db-115">Unless you set **autoStart** to **true** immediately before specifying a media item, you should not rely on this setting as a substitute for using the **IWMPControls.play** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd0db-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd0db-116">Requirements</span></span>



| <span data-ttu-id="bd0db-117">需求</span><span class="sxs-lookup"><span data-stu-id="bd0db-117">Requirement</span></span> | <span data-ttu-id="bd0db-118">值</span><span class="sxs-lookup"><span data-stu-id="bd0db-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd0db-119">版本</span><span class="sxs-lookup"><span data-stu-id="bd0db-119">Version</span></span><br/>   | <span data-ttu-id="bd0db-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="bd0db-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="bd0db-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="bd0db-121">Namespace</span></span><br/> | <span data-ttu-id="bd0db-122">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="bd0db-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="bd0db-123">組件</span><span class="sxs-lookup"><span data-stu-id="bd0db-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="bd0db-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="bd0db-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd0db-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd0db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd0db-126">**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bd0db-126">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bd0db-127">**AxWindowsMediaPlayer. currentPlaylist (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bd0db-127">**AxWindowsMediaPlayer.currentPlaylist (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bd0db-128">**AxWindowsMediaPlayer (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bd0db-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bd0db-129">**IWMPControls (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bd0db-129">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="bd0db-130">**IWMPSettings 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="bd0db-130">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





