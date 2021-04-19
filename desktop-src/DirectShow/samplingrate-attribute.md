---
description: Samplingrate 屬性會指定輸出音訊的取樣率，以 Hz 為限。
ms.assetid: d053285c-bf94-465a-99d3-bed7c2d09b1a
title: samplingrate 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2daa2751b0c41f5bf2eb030841dad638d8672a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972929"
---
# <a name="samplingrate-attribute"></a><span data-ttu-id="99ef4-103">samplingrate 屬性</span><span class="sxs-lookup"><span data-stu-id="99ef4-103">samplingrate Attribute</span></span>

> [!Note]  
> <span data-ttu-id="99ef4-104">\[廢棄。</span><span class="sxs-lookup"><span data-stu-id="99ef4-104">\[Deprecated.</span></span> <span data-ttu-id="99ef4-105">此 API 可能會從 Windows 的未來版本中移除。\]</span><span class="sxs-lookup"><span data-stu-id="99ef4-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="99ef4-106">`samplingrate`屬性指定輸出音訊的取樣率，以 Hz 為限。</span><span class="sxs-lookup"><span data-stu-id="99ef4-106">The `samplingrate` attribute specifies the sampling rate of the output audio, in Hz.</span></span>

## <a name="possible-values"></a><span data-ttu-id="99ef4-107">可能的值</span><span class="sxs-lookup"><span data-stu-id="99ef4-107">Possible Values</span></span>

<span data-ttu-id="99ef4-108">此值必須是8000、11025、22050、32000、44100或48000。</span><span class="sxs-lookup"><span data-stu-id="99ef4-108">The value must be 8000, 11025, 22050, 32000, 44100, or 48000.</span></span> <span data-ttu-id="99ef4-109">預設值為44100。</span><span class="sxs-lookup"><span data-stu-id="99ef4-109">The default value is 44100.</span></span>

## <a name="applies-to"></a><span data-ttu-id="99ef4-110">套用至</span><span class="sxs-lookup"><span data-stu-id="99ef4-110">Applies To</span></span>

[<span data-ttu-id="99ef4-111">**組**</span><span class="sxs-lookup"><span data-stu-id="99ef4-111">**group**</span></span>](group-element.md)

## <a name="remarks"></a><span data-ttu-id="99ef4-112">備註</span><span class="sxs-lookup"><span data-stu-id="99ef4-112">Remarks</span></span>

<span data-ttu-id="99ef4-113">只有當 **type** 屬性為時，才設定這個屬性 `audio` 。</span><span class="sxs-lookup"><span data-stu-id="99ef4-113">Set this attribute only if the **type** attribute is `audio`.</span></span>

## <a name="see-also"></a><span data-ttu-id="99ef4-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99ef4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99ef4-115">XTL 屬性</span><span class="sxs-lookup"><span data-stu-id="99ef4-115">XTL Attributes</span></span>](xtl-attributes.md)
</dt> </dl>

 

 



