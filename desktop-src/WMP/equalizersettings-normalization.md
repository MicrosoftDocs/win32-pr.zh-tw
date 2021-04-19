---
title: EQUALIZERSETTINGS 正規化
description: 正規化屬性會指定或抓取值，指出是否已啟用正規化。
ms.assetid: d0819624-7bc5-447a-b890-c8af94faa7b0
keywords:
- EQUALIZERSETTINGS 正規化 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.normalization
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9714359e5d5e2af0c82a0d687555f7cfcbf1cf70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990146"
---
# <a name="equalizersettingsnormalization"></a><span data-ttu-id="682c6-104">EQUALIZERSETTINGS 正規化</span><span class="sxs-lookup"><span data-stu-id="682c6-104">EQUALIZERSETTINGS.normalization</span></span>

<span data-ttu-id="682c6-105">正規化 **屬性會** 指定或抓取值，指出是否已啟用正規化。</span><span class="sxs-lookup"><span data-stu-id="682c6-105">The **normalization** attribute specifies or retrieves a value indicating whether normalization is enabled.</span></span>

``` syntax
        elementID.normalization
```

## <a name="possible-values"></a><span data-ttu-id="682c6-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="682c6-106">Possible Values</span></span>

<span data-ttu-id="682c6-107">此屬性是讀取/寫入 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="682c6-107">This attribute is a read/write **Boolean**.</span></span>



| <span data-ttu-id="682c6-108">值</span><span class="sxs-lookup"><span data-stu-id="682c6-108">Value</span></span> | <span data-ttu-id="682c6-109">描述</span><span class="sxs-lookup"><span data-stu-id="682c6-109">Description</span></span>                         |
|-------|-------------------------------------|
| <span data-ttu-id="682c6-110">true</span><span class="sxs-lookup"><span data-stu-id="682c6-110">true</span></span>  | <span data-ttu-id="682c6-111">已啟用正規化。</span><span class="sxs-lookup"><span data-stu-id="682c6-111">Normalization is enabled.</span></span>           |
| <span data-ttu-id="682c6-112">false</span><span class="sxs-lookup"><span data-stu-id="682c6-112">false</span></span> | <span data-ttu-id="682c6-113">預設值。</span><span class="sxs-lookup"><span data-stu-id="682c6-113">Default.</span></span> <span data-ttu-id="682c6-114">正規化已停用。</span><span class="sxs-lookup"><span data-stu-id="682c6-114">Normalization is disabled.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="682c6-115">備註</span><span class="sxs-lookup"><span data-stu-id="682c6-115">Remarks</span></span>

<span data-ttu-id="682c6-116">啟用正規化時，會將整個數位媒體檔案的音訊信號向上調整為最大值。</span><span class="sxs-lookup"><span data-stu-id="682c6-116">When normalization is enabled, the audio signal for an entire digital media file is scaled up to the maximum value.</span></span> <span data-ttu-id="682c6-117">這可讓多個檔案在大約相同的磁片區上播放，而不需要進行磁片區調整。</span><span class="sxs-lookup"><span data-stu-id="682c6-117">This allows multiple files to be played at approximately the same volume without requiring volume adjustments.</span></span>

## <a name="requirements"></a><span data-ttu-id="682c6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="682c6-118">Requirements</span></span>



| <span data-ttu-id="682c6-119">需求</span><span class="sxs-lookup"><span data-stu-id="682c6-119">Requirement</span></span> | <span data-ttu-id="682c6-120">值</span><span class="sxs-lookup"><span data-stu-id="682c6-120">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="682c6-121">版本</span><span class="sxs-lookup"><span data-stu-id="682c6-121">Version</span></span><br/> | <span data-ttu-id="682c6-122">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="682c6-122">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="682c6-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="682c6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="682c6-124">**EQUALIZERSETTINGS 元素**</span><span class="sxs-lookup"><span data-stu-id="682c6-124">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="682c6-125">**EQUALIZERSETTINGS.normalizationAverage**</span><span class="sxs-lookup"><span data-stu-id="682c6-125">**EQUALIZERSETTINGS.normalizationAverage**</span></span>](equalizersettings-normalizationaverage.md)
</dt> <dt>

[<span data-ttu-id="682c6-126">**EQUALIZERSETTINGS.normalizationPeak**</span><span class="sxs-lookup"><span data-stu-id="682c6-126">**EQUALIZERSETTINGS.normalizationPeak**</span></span>](equalizersettings-normalizationpeak.md)
</dt> </dl>

 

 





