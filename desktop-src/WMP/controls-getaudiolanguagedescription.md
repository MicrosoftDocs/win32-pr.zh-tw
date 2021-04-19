---
title: GetAudioLanguageDescription 方法
description: GetAudioLanguageDescription 方法會抓取對應于指定之以一為基礎之索引的音訊語言描述。
ms.assetid: 995a2568-f15f-4b92-9782-92ba5273f444
keywords:
- getAudioLanguageDescription 方法 Windows Media Player
- getAudioLanguageDescription 方法 Windows Media Player、Controls 類別
- Controls 類別 Windows Media Player，getAudioLanguageDescription 方法
topic_type:
- apiref
api_name:
- Controls.getAudioLanguageDescription
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d28e82648a1047252402694f4948d2a2734f344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984002"
---
# <a name="controlsgetaudiolanguagedescription-method"></a><span data-ttu-id="19b11-106">GetAudioLanguageDescription 方法</span><span class="sxs-lookup"><span data-stu-id="19b11-106">Controls.getAudioLanguageDescription method</span></span>

<span data-ttu-id="19b11-107">**GetAudioLanguageDescription** 方法會抓取對應于指定之以一為基礎之索引的音訊語言描述。</span><span class="sxs-lookup"><span data-stu-id="19b11-107">The **getAudioLanguageDescription** method retrieves the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="19b11-108">語法</span><span class="sxs-lookup"><span data-stu-id="19b11-108">Syntax</span></span>


```JScript
strRetVal = Controls.getAudioLanguageDescription(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="19b11-109">參數</span><span class="sxs-lookup"><span data-stu-id="19b11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19b11-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19b11-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19b11-111">指定以一為基礎之音訊語言索引的 (**long**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="19b11-111">**Number** (**long**) specifying the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19b11-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="19b11-112">Return value</span></span>

<span data-ttu-id="19b11-113">這個方法會傳回 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="19b11-113">This method returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19b11-114">備註</span><span class="sxs-lookup"><span data-stu-id="19b11-114">Remarks</span></span>

<span data-ttu-id="19b11-115">針對 Windows Media 內容，與語言選取相關的屬性和方法只支援單一輸出。</span><span class="sxs-lookup"><span data-stu-id="19b11-115">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

<span data-ttu-id="19b11-116">使用 **audioLanguageCount** 屬性來取得支援的音訊語言數目，然後使用以一為基礎的索引個別存取音訊語言。</span><span class="sxs-lookup"><span data-stu-id="19b11-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

<span data-ttu-id="19b11-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="19b11-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="19b11-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="19b11-118">Requirements</span></span>



| <span data-ttu-id="19b11-119">需求</span><span class="sxs-lookup"><span data-stu-id="19b11-119">Requirement</span></span> | <span data-ttu-id="19b11-120">值</span><span class="sxs-lookup"><span data-stu-id="19b11-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="19b11-121">版本</span><span class="sxs-lookup"><span data-stu-id="19b11-121">Version</span></span><br/> | <span data-ttu-id="19b11-122">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="19b11-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="19b11-123">DLL</span><span class="sxs-lookup"><span data-stu-id="19b11-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="19b11-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19b11-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19b11-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19b11-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19b11-126">**Controls 物件**</span><span class="sxs-lookup"><span data-stu-id="19b11-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="19b11-127">**AudioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="19b11-127">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="19b11-128">**CurrentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="19b11-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="19b11-129">**CurrentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="19b11-129">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="19b11-130">**GetAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="19b11-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> <dt>

[<span data-ttu-id="19b11-131">**GetLanguageName**</span><span class="sxs-lookup"><span data-stu-id="19b11-131">**Controls.getLanguageName**</span></span>](controls-getlanguagename.md)
</dt> </dl>

 

 





