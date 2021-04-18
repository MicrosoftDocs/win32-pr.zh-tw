---
title: CurrentAudioLanguageIndex
description: CurrentAudioLanguageIndex 屬性會指定或抓取對應于播放音訊語言的單一索引。
ms.assetid: 9a1ae887-4e64-4758-a8a2-bf2e10a7a5c7
keywords:
- CurrentAudioLanguageIndex Windows Media Player
topic_type:
- apiref
api_name:
- Controls.currentAudioLanguageIndex
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1eb87873170c486782368f431f4fa8e3597b20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976151"
---
# <a name="controlscurrentaudiolanguageindex"></a><span data-ttu-id="f87fe-104">CurrentAudioLanguageIndex</span><span class="sxs-lookup"><span data-stu-id="f87fe-104">Controls.currentAudioLanguageIndex</span></span>

<span data-ttu-id="f87fe-105">**CurrentAudioLanguageIndex** 屬性會指定或抓取對應于播放音訊語言的單一索引。</span><span class="sxs-lookup"><span data-stu-id="f87fe-105">The **currentAudioLanguageIndex** property specifies or retrieves the one-based index that corresponds to the audio language for playback.</span></span>

``` syntax
player.controls.currentAudioLanguageIndex
      
```

## <a name="possible-values"></a><span data-ttu-id="f87fe-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="f87fe-106">Possible Values</span></span>

<span data-ttu-id="f87fe-107">這個屬性是 (**長**) 的讀取/寫入 **號碼**。</span><span class="sxs-lookup"><span data-stu-id="f87fe-107">This property is a read/write **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="f87fe-108">備註</span><span class="sxs-lookup"><span data-stu-id="f87fe-108">Remarks</span></span>

<span data-ttu-id="f87fe-109">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="f87fe-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="f87fe-110">使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目。</span><span class="sxs-lookup"><span data-stu-id="f87fe-110">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

<span data-ttu-id="f87fe-111">**Windows Media Player 10** 行動裝置版：這個屬性只接受或傳回0。</span><span class="sxs-lookup"><span data-stu-id="f87fe-111">**Windows Media Player 10 Mobile:** This property only accepts or returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="f87fe-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f87fe-112">Requirements</span></span>



| <span data-ttu-id="f87fe-113">需求</span><span class="sxs-lookup"><span data-stu-id="f87fe-113">Requirement</span></span> | <span data-ttu-id="f87fe-114">值</span><span class="sxs-lookup"><span data-stu-id="f87fe-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f87fe-115">版本</span><span class="sxs-lookup"><span data-stu-id="f87fe-115">Version</span></span><br/> | <span data-ttu-id="f87fe-116">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="f87fe-116">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="f87fe-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f87fe-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="f87fe-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f87fe-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f87fe-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f87fe-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f87fe-120">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="f87fe-120">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="f87fe-121">**AudioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="f87fe-121">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="f87fe-122">**CurrentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="f87fe-122">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="f87fe-123">**GetAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="f87fe-123">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="f87fe-124">**GetAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="f87fe-124">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="f87fe-125">**GetLanguageName**</span><span class="sxs-lookup"><span data-stu-id="f87fe-125">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





