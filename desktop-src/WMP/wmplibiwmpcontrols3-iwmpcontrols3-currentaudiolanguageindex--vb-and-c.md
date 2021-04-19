---
title: IWMPControls3 currentAudioLanguageIndex 屬性
description: CurrentAudioLanguageIndex 屬性會取得或設定對應至播放音訊語言的單一索引。
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- currentAudioLanguageIndex 屬性 Windows Media Player
- currentAudioLanguageIndex 屬性 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，currentAudioLanguageIndex 屬性
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980203"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="57763-106">IWMPControls3：： currentAudioLanguageIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="57763-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="57763-107">**CurrentAudioLanguageIndex** 屬性會取得或設定對應至播放音訊語言的單一索引。</span><span class="sxs-lookup"><span data-stu-id="57763-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="57763-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="57763-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="57763-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="57763-109">Property value</span></span>

<span data-ttu-id="57763-110">以一為基礎的語言索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="57763-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="57763-111">備註</span><span class="sxs-lookup"><span data-stu-id="57763-111">Remarks</span></span>

<span data-ttu-id="57763-112">針對以 Windows Media 為基礎的內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="57763-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="57763-113">使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目。</span><span class="sxs-lookup"><span data-stu-id="57763-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="57763-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="57763-114">Requirements</span></span>



| <span data-ttu-id="57763-115">需求</span><span class="sxs-lookup"><span data-stu-id="57763-115">Requirement</span></span> | <span data-ttu-id="57763-116">值</span><span class="sxs-lookup"><span data-stu-id="57763-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57763-117">版本</span><span class="sxs-lookup"><span data-stu-id="57763-117">Version</span></span><br/>   | <span data-ttu-id="57763-118">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="57763-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="57763-119">命名空間</span><span class="sxs-lookup"><span data-stu-id="57763-119">Namespace</span></span><br/> | <span data-ttu-id="57763-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="57763-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="57763-121">組件</span><span class="sxs-lookup"><span data-stu-id="57763-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="57763-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="57763-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57763-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57763-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57763-124">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="57763-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="57763-125">**IWMPControls3. audioLanguageCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="57763-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="57763-126">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="57763-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="57763-127">**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="57763-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="57763-128">**IWMPControls3. getAudioLanguageID (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="57763-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="57763-129">**IWMPControls3. getLanguageName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="57763-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





