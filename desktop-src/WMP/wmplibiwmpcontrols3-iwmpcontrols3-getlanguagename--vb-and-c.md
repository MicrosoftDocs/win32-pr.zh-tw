---
title: IWMPControls3 getLanguageName 方法
description: GetLanguageName 方法會傳回具有指定地區設定識別碼 (LCID) 的音訊語言名稱。
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- getLanguageName 方法 Windows Media Player
- getLanguageName 方法 Windows Media Player，IWMPControls3 介面
- IWMPControls3 介面 Windows Media Player，getLanguageName 方法
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980202"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="8378a-106">IWMPControls3：： getLanguageName 方法</span><span class="sxs-lookup"><span data-stu-id="8378a-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="8378a-107">**GetLanguageName** 方法會傳回具有指定地區設定識別碼 (LCID) 的音訊語言名稱。</span><span class="sxs-lookup"><span data-stu-id="8378a-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="8378a-108">語法</span><span class="sxs-lookup"><span data-stu-id="8378a-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="8378a-109">參數</span><span class="sxs-lookup"><span data-stu-id="8378a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8378a-110">*lLangID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8378a-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8378a-111">為 LCID 的 **system.object** 。</span><span class="sxs-lookup"><span data-stu-id="8378a-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8378a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8378a-112">Return value</span></span>

<span data-ttu-id="8378a-113">**System.string** ，這是音訊語言的名稱。</span><span class="sxs-lookup"><span data-stu-id="8378a-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="8378a-114">備註</span><span class="sxs-lookup"><span data-stu-id="8378a-114">Remarks</span></span>

<span data-ttu-id="8378a-115">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="8378a-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="8378a-116">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="8378a-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="8378a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8378a-117">Requirements</span></span>



| <span data-ttu-id="8378a-118">需求</span><span class="sxs-lookup"><span data-stu-id="8378a-118">Requirement</span></span> | <span data-ttu-id="8378a-119">值</span><span class="sxs-lookup"><span data-stu-id="8378a-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8378a-120">版本</span><span class="sxs-lookup"><span data-stu-id="8378a-120">Version</span></span><br/>   | <span data-ttu-id="8378a-121">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="8378a-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="8378a-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="8378a-122">Namespace</span></span><br/> | <span data-ttu-id="8378a-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="8378a-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="8378a-124">組件</span><span class="sxs-lookup"><span data-stu-id="8378a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="8378a-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="8378a-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8378a-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8378a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8378a-127">**IWMPControls3 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8378a-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8378a-128">**IWMPControls3. audioLanguageCount (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8378a-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8378a-129">**IWMPControls3. currentAudioLanguage (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8378a-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8378a-130">**IWMPControls3. currentAudioLanguageIndex (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8378a-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8378a-131">**IWMPControls3. getAudioLanguageDescription (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8378a-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="8378a-132">**IWMPControls3. getAudioLanguageID (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="8378a-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





