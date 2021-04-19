---
title: IWMPControls3 getAudioLanguageDescription 方法
description: GetAudioLanguageDescription 方法會傳回對應至指定之以一為基礎之索引的音訊語言描述。
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- getAudioLanguageDescription 方法 Windows Media Player
- getAudioLanguageDescription 方法 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，getAudioLanguageDescription 方法
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991208"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="2293e-106">IWMPControls3：： getAudioLanguageDescription 方法</span><span class="sxs-lookup"><span data-stu-id="2293e-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="2293e-107">**GetAudioLanguageDescription** 方法會傳回對應至指定之以一為基礎之索引的音訊語言描述。</span><span class="sxs-lookup"><span data-stu-id="2293e-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2293e-108">語法</span><span class="sxs-lookup"><span data-stu-id="2293e-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="2293e-109">參數</span><span class="sxs-lookup"><span data-stu-id="2293e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2293e-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2293e-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2293e-111">以一為基礎的音訊語言索引的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="2293e-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2293e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="2293e-112">Return value</span></span>

<span data-ttu-id="2293e-113">**System.string** ，這是音訊語言的描述。</span><span class="sxs-lookup"><span data-stu-id="2293e-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="2293e-114">備註</span><span class="sxs-lookup"><span data-stu-id="2293e-114">Remarks</span></span>

<span data-ttu-id="2293e-115">針對以 Windows Media 為基礎的內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="2293e-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="2293e-116">使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目，然後使用以一為基礎的索引個別存取音訊語言。</span><span class="sxs-lookup"><span data-stu-id="2293e-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="2293e-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2293e-117">Requirements</span></span>



| <span data-ttu-id="2293e-118">需求</span><span class="sxs-lookup"><span data-stu-id="2293e-118">Requirement</span></span> | <span data-ttu-id="2293e-119">值</span><span class="sxs-lookup"><span data-stu-id="2293e-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2293e-120">版本</span><span class="sxs-lookup"><span data-stu-id="2293e-120">Version</span></span><br/>   | <span data-ttu-id="2293e-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="2293e-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2293e-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="2293e-122">Namespace</span></span><br/> | <span data-ttu-id="2293e-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2293e-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2293e-124">組件</span><span class="sxs-lookup"><span data-stu-id="2293e-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2293e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="2293e-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2293e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2293e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2293e-127">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2293e-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2293e-128">**IWMPControls3. audioLanguageCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2293e-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2293e-129">**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2293e-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2293e-130">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2293e-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2293e-131">**IWMPControls3. getAudioLanguageID (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2293e-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2293e-132">**IWMPControls3. getLanguageName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="2293e-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





