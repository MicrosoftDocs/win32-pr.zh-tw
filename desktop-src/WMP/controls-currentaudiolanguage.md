---
title: CurrentAudioLanguage
description: CurrentAudioLanguage 屬性會指定或抓取用來播放之音訊語言 (LCID) 的地區設定識別碼。
ms.assetid: 628845df-add3-4068-9c3d-b4a9b818808c
keywords:
- CurrentAudioLanguage Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguage
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bc84c7d4c14bb742a6db37feca59fb9d0db0e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979450"
---
# <a name="controlscurrentaudiolanguage"></a><span data-ttu-id="5356d-104">CurrentAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="5356d-104">Controls.currentAudioLanguage</span></span>

<span data-ttu-id="5356d-105">**CurrentAudioLanguage** 屬性會指定或抓取用來播放之音訊語言 (LCID) 的地區設定識別碼。</span><span class="sxs-lookup"><span data-stu-id="5356d-105">The **currentAudioLanguage** property specifies or retrieves the locale identifier (LCID) of the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguage
      
```

## <a name="possible-values"></a><span data-ttu-id="5356d-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="5356d-106">Possible Values</span></span>

<span data-ttu-id="5356d-107">這個屬性是 (**長**) 的讀取/寫入 **號碼**。</span><span class="sxs-lookup"><span data-stu-id="5356d-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5356d-108">備註</span><span class="sxs-lookup"><span data-stu-id="5356d-108">Remarks</span></span>

<span data-ttu-id="5356d-109">LCID 可唯一識別特定語言方言，稱為地區設定。</span><span class="sxs-lookup"><span data-stu-id="5356d-109">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="5356d-110">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="5356d-110">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="5356d-111">使用 DVD 內容時，指定 LCID 將會導致第一個可用的音訊播放軌選取指定的語言識別項。</span><span class="sxs-lookup"><span data-stu-id="5356d-111">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

<span data-ttu-id="5356d-112">**Windows Media Player 10** 行動裝置版：這個屬性只會接受或傳回語言中立的 LCID (0) 。</span><span class="sxs-lookup"><span data-stu-id="5356d-112">**Windows Media Player 10 Mobile:** This property only accepts or returns the language-neutral LCID (0).</span></span>

## <a name="requirements"></a><span data-ttu-id="5356d-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5356d-113">Requirements</span></span>



| <span data-ttu-id="5356d-114">需求</span><span class="sxs-lookup"><span data-stu-id="5356d-114">Requirement</span></span> | <span data-ttu-id="5356d-115">值</span><span class="sxs-lookup"><span data-stu-id="5356d-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5356d-116">版本</span><span class="sxs-lookup"><span data-stu-id="5356d-116">Version</span></span><br/> | <span data-ttu-id="5356d-117">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="5356d-117">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="5356d-118">DLL</span><span class="sxs-lookup"><span data-stu-id="5356d-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="5356d-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5356d-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5356d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5356d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5356d-121">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="5356d-121">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="5356d-122">**AudioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="5356d-122">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="5356d-123">**CurrentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="5356d-123">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="5356d-124">**GetAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="5356d-124">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="5356d-125">**GetAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="5356d-125">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="5356d-126">**GetLanguageName**</span><span class="sxs-lookup"><span data-stu-id="5356d-126">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





