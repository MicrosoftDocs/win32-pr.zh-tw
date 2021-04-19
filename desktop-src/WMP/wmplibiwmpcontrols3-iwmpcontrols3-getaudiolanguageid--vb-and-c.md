---
title: IWMPControls3 getAudioLanguageID 方法
description: GetAudioLanguageID 方法會針對指定的音訊語言索引，傳回 (LCID) 的地區設定識別碼。
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- getAudioLanguageID 方法 Windows Media Player
- getAudioLanguageID 方法 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，getAudioLanguageID 方法
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990998"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="12da8-106">IWMPControls3：： getAudioLanguageID 方法</span><span class="sxs-lookup"><span data-stu-id="12da8-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="12da8-107">**GetAudioLanguageID** 方法會針對指定的音訊語言索引，傳回 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="12da8-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="12da8-108">語法</span><span class="sxs-lookup"><span data-stu-id="12da8-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="12da8-109">參數</span><span class="sxs-lookup"><span data-stu-id="12da8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12da8-110">*lIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="12da8-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12da8-111">以一為基礎之音訊語言的一種類型的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="12da8-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12da8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="12da8-112">Return value</span></span>

<span data-ttu-id="12da8-113">為 LCID 的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="12da8-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="12da8-114">備註</span><span class="sxs-lookup"><span data-stu-id="12da8-114">Remarks</span></span>

<span data-ttu-id="12da8-115">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="12da8-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="12da8-116">針對以 Windows Media 為基礎的內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="12da8-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="12da8-117">使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目，然後使用以一為基礎的索引個別存取音訊語言。</span><span class="sxs-lookup"><span data-stu-id="12da8-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="12da8-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="12da8-118">Requirements</span></span>



| <span data-ttu-id="12da8-119">需求</span><span class="sxs-lookup"><span data-stu-id="12da8-119">Requirement</span></span> | <span data-ttu-id="12da8-120">值</span><span class="sxs-lookup"><span data-stu-id="12da8-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12da8-121">版本</span><span class="sxs-lookup"><span data-stu-id="12da8-121">Version</span></span><br/>   | <span data-ttu-id="12da8-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="12da8-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="12da8-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="12da8-123">Namespace</span></span><br/> | <span data-ttu-id="12da8-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="12da8-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="12da8-125">組件</span><span class="sxs-lookup"><span data-stu-id="12da8-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="12da8-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="12da8-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12da8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="12da8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12da8-128">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="12da8-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="12da8-129">**IWMPControls3. audioLanguageCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="12da8-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="12da8-130">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="12da8-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="12da8-131">**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="12da8-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="12da8-132">**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="12da8-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="12da8-133">**IWMPControls3. getLanguageName (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="12da8-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





