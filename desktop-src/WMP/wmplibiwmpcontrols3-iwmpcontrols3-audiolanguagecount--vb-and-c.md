---
title: IWMPControls3 audioLanguageCount 屬性
description: AudioLanguageCount 屬性會取得支援的音訊語言計數。
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- audioLanguageCount 屬性 Windows Media Player
- audioLanguageCount 屬性 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，audioLanguageCount 屬性
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980204"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="3c55e-106">IWMPControls3：： audioLanguageCount 屬性</span><span class="sxs-lookup"><span data-stu-id="3c55e-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="3c55e-107">**AudioLanguageCount** 屬性會取得支援的音訊語言計數。</span><span class="sxs-lookup"><span data-stu-id="3c55e-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c55e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c55e-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="3c55e-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="3c55e-109">Property value</span></span>

<span data-ttu-id="3c55e-110">支援的音訊語言計數的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="3c55e-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="3c55e-111">備註</span><span class="sxs-lookup"><span data-stu-id="3c55e-111">Remarks</span></span>

<span data-ttu-id="3c55e-112">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="3c55e-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c55e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c55e-113">Requirements</span></span>



| <span data-ttu-id="3c55e-114">需求</span><span class="sxs-lookup"><span data-stu-id="3c55e-114">Requirement</span></span> | <span data-ttu-id="3c55e-115">值</span><span class="sxs-lookup"><span data-stu-id="3c55e-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c55e-116">版本</span><span class="sxs-lookup"><span data-stu-id="3c55e-116">Version</span></span><br/>   | <span data-ttu-id="3c55e-117">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="3c55e-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3c55e-118">命名空間</span><span class="sxs-lookup"><span data-stu-id="3c55e-118">Namespace</span></span><br/> | <span data-ttu-id="3c55e-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3c55e-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3c55e-120">組件</span><span class="sxs-lookup"><span data-stu-id="3c55e-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3c55e-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="3c55e-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c55e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c55e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c55e-123">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3c55e-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c55e-124">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3c55e-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c55e-125">**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3c55e-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c55e-126">**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3c55e-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c55e-127">**IWMPControls3. getAudioLanguageID (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3c55e-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3c55e-128">**IWMPControls3. getLanguageName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="3c55e-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





