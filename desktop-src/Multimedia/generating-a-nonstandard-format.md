---
title: 產生非標準格式
description: 產生非標準格式
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- 音訊壓縮管理員 (的) 、非標準格式
- " (的音效壓縮管理員) 、非標準格式"
- 未通過範例，非標準格式
- acmFormatSuggest 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839932"
---
# <a name="generating-a-nonstandard-format"></a><span data-ttu-id="ee10c-107">產生非標準格式</span><span class="sxs-lookup"><span data-stu-id="ee10c-107">Generating a Nonstandard Format</span></span>

<span data-ttu-id="ee10c-108">有時候應用程式需要非標準的格式。</span><span class="sxs-lookup"><span data-stu-id="ee10c-108">Sometimes an application needs a nonstandard format.</span></span> <span data-ttu-id="ee10c-109">例如，應用程式可能需要 16 kHz 的 ADPCM 格式檔案。</span><span class="sxs-lookup"><span data-stu-id="ee10c-109">For example, an application might need a 16-kHz ADPCM-format file.</span></span> <span data-ttu-id="ee10c-110">因為 16 kHz 並非標準的，所以列舉函數不會產生此格式。</span><span class="sxs-lookup"><span data-stu-id="ee10c-110">Because 16 kHz is nonstandard, the enumeration functions will not generate this format.</span></span> <span data-ttu-id="ee10c-111">事實上，在應用程式中撰寫格式演算法的自訂程式碼很簡單，沒有可靠的方式可以產生非標準格式。</span><span class="sxs-lookup"><span data-stu-id="ee10c-111">In fact, short of custom coding the format algorithms into the application, there is no reliable way to generate a nonstandard format.</span></span> <span data-ttu-id="ee10c-112">不過，有時可能會藉由使用所有必要的資訊設定有效的 PCM 格式，然後使用 [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) 函式，來產生類似的格式。</span><span class="sxs-lookup"><span data-stu-id="ee10c-112">It is sometimes possible, however, to generate an analogous format by setting up a valid PCM format with all the required information and then using the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function.</span></span> <span data-ttu-id="ee10c-113">因為壓縮機和 decompressors 會嘗試建議最接近所需格式的格式，所以通常會保留通道數目和頻率。</span><span class="sxs-lookup"><span data-stu-id="ee10c-113">Because compressors and decompressors try to suggest a format that is closest to the desired format, the number of channels and frequency are usually preserved.</span></span>

 

 




