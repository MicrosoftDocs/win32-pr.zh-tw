---
title: IWMPControls3 currentAudioLanguage 屬性
description: CurrentAudioLanguage 屬性會取得或設定用於播放之音訊語言 (LCID) 的地區設定識別碼。
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- currentAudioLanguage 屬性 Windows Media Player
- currentAudioLanguage 屬性 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，currentAudioLanguage 屬性
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996052"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="59214-106">IWMPControls3：： currentAudioLanguage 屬性</span><span class="sxs-lookup"><span data-stu-id="59214-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="59214-107">**CurrentAudioLanguage** 屬性會取得或設定用於播放之音訊語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="59214-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="59214-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59214-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="59214-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="59214-109">Property value</span></span>

<span data-ttu-id="59214-110">System.string **，它** 是音訊語言的 LCID。</span><span class="sxs-lookup"><span data-stu-id="59214-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="59214-111">備註</span><span class="sxs-lookup"><span data-stu-id="59214-111">Remarks</span></span>

<span data-ttu-id="59214-112">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="59214-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="59214-113">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="59214-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="59214-114">使用 DVD 內容時，指定 LCID 將會導致第一個可用的音訊播放軌選取指定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="59214-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="59214-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="59214-115">Requirements</span></span>



| <span data-ttu-id="59214-116">需求</span><span class="sxs-lookup"><span data-stu-id="59214-116">Requirement</span></span> | <span data-ttu-id="59214-117">值</span><span class="sxs-lookup"><span data-stu-id="59214-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59214-118">版本</span><span class="sxs-lookup"><span data-stu-id="59214-118">Version</span></span><br/>   | <span data-ttu-id="59214-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="59214-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="59214-120">命名空間</span><span class="sxs-lookup"><span data-stu-id="59214-120">Namespace</span></span><br/> | <span data-ttu-id="59214-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="59214-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="59214-122">組件</span><span class="sxs-lookup"><span data-stu-id="59214-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="59214-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="59214-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59214-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59214-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59214-125">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59214-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59214-126">**IWMPControls3. audioLanguageCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59214-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59214-127">**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59214-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59214-128">**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59214-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59214-129">**IWMPControls3. getAudioLanguageID (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59214-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="59214-130">**IWMPControls3. getLanguageName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="59214-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





