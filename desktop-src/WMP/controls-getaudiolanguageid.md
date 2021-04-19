---
title: GetAudioLanguageID 方法
description: GetAudioLanguageID 方法會針對指定的音訊語言索引，抓取 (LCID) 的地區設定識別碼。
ms.assetid: 8134a7ce-bdc7-46b2-b10e-2bf1215b0de1
keywords:
- getAudioLanguageID 方法 Windows Media Player
- getAudioLanguageID 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，getAudioLanguageID 方法
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab27e95edfc74fa7a9f57d2010bf86299c55dd4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994232"
---
# <a name="controlsgetaudiolanguageid-method"></a><span data-ttu-id="dbb34-106">GetAudioLanguageID 方法</span><span class="sxs-lookup"><span data-stu-id="dbb34-106">Controls.getAudioLanguageID method</span></span>

<span data-ttu-id="dbb34-107">**GetAudioLanguageID** 方法會針對指定的音訊語言索引，抓取 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="dbb34-107">The **getAudioLanguageID** method retrieves the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="dbb34-108">語法</span><span class="sxs-lookup"><span data-stu-id="dbb34-108">Syntax</span></span>


```JScript
retVal = Controls.getAudioLanguageID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="dbb34-109">參數</span><span class="sxs-lookup"><span data-stu-id="dbb34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dbb34-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dbb34-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dbb34-111">指定音訊語言索引的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="dbb34-111">**Number** (**long**) specifying the audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dbb34-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dbb34-112">Return value</span></span>

<span data-ttu-id="dbb34-113">這個方法會傳回 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="dbb34-113">This method returns a **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="dbb34-114">備註</span><span class="sxs-lookup"><span data-stu-id="dbb34-114">Remarks</span></span>

<span data-ttu-id="dbb34-115">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="dbb34-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="dbb34-116">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="dbb34-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="dbb34-117">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回語言中立的 LCID (0) 。</span><span class="sxs-lookup"><span data-stu-id="dbb34-117">**Windows Media Player 10 Mobile:** This property always returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="dbb34-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dbb34-118">Requirements</span></span>



| <span data-ttu-id="dbb34-119">需求</span><span class="sxs-lookup"><span data-stu-id="dbb34-119">Requirement</span></span> | <span data-ttu-id="dbb34-120">值</span><span class="sxs-lookup"><span data-stu-id="dbb34-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dbb34-121">版本</span><span class="sxs-lookup"><span data-stu-id="dbb34-121">Version</span></span><br/> | <span data-ttu-id="dbb34-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="dbb34-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="dbb34-123">DLL</span><span class="sxs-lookup"><span data-stu-id="dbb34-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="dbb34-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dbb34-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dbb34-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dbb34-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbb34-126">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="dbb34-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="dbb34-127">**AudioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="dbb34-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="dbb34-128">**CurrentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="dbb34-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="dbb34-129">**CurrentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="dbb34-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="dbb34-130">**GetAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="dbb34-130">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="dbb34-131">**GetLanguageName**</span><span class="sxs-lookup"><span data-stu-id="dbb34-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





