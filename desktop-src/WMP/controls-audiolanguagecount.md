---
title: AudioLanguageCount
description: AudioLanguageCount 屬性會捕獲支援的音訊語言計數。
ms.assetid: a6dda8bf-db8c-4e97-9277-5a23dfa93156
keywords:
- AudioLanguageCount Windows Media Player
topic_type:
- apiref
api_name:
- Controls.audioLanguageCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09193eb19580d9456f25ea336fe68b8d21e06bae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983110"
---
# <a name="controlsaudiolanguagecount"></a><span data-ttu-id="2701b-104">AudioLanguageCount</span><span class="sxs-lookup"><span data-stu-id="2701b-104">Controls.audioLanguageCount</span></span>

<span data-ttu-id="2701b-105">**AudioLanguageCount** 屬性會捕獲支援的音訊語言計數。</span><span class="sxs-lookup"><span data-stu-id="2701b-105">The **audioLanguageCount** property retrieves the count of supported audio languages.</span></span>

``` syntax
player.controls.audioLanguageCount
      
```

## <a name="possible-values"></a><span data-ttu-id="2701b-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="2701b-106">Possible Values</span></span>

<span data-ttu-id="2701b-107">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="2701b-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2701b-108">備註</span><span class="sxs-lookup"><span data-stu-id="2701b-108">Remarks</span></span>

<span data-ttu-id="2701b-109">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="2701b-109">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="2701b-110">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回1。</span><span class="sxs-lookup"><span data-stu-id="2701b-110">**Windows Media Player 10 Mobile:** This property always returns 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="2701b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="2701b-111">Requirements</span></span>



| <span data-ttu-id="2701b-112">需求</span><span class="sxs-lookup"><span data-stu-id="2701b-112">Requirement</span></span> | <span data-ttu-id="2701b-113">值</span><span class="sxs-lookup"><span data-stu-id="2701b-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2701b-114">版本</span><span class="sxs-lookup"><span data-stu-id="2701b-114">Version</span></span><br/> | <span data-ttu-id="2701b-115">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="2701b-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="2701b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="2701b-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="2701b-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2701b-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2701b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2701b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2701b-119">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="2701b-119">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="2701b-120">**CurrentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="2701b-120">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="2701b-121">**CurrentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="2701b-121">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="2701b-122">**GetAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="2701b-122">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="2701b-123">**GetAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="2701b-123">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="2701b-124">**GetLanguageName**</span><span class="sxs-lookup"><span data-stu-id="2701b-124">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





