---
description: 本節說明 Windows Shell 色彩調色板處理函式。 本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。
title: Shell 色彩調色板處理函式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 93848cb3-60c6-4b2f-82d9-abfee97e372a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba92dcf280b8d54b8778e276bb603d888f5991c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193160"
---
# <a name="shell-color-palette-handling-functions"></a><span data-ttu-id="5489f-104">Shell 色彩調色板處理函式</span><span class="sxs-lookup"><span data-stu-id="5489f-104">Shell Color Palette Handling Functions</span></span>

<span data-ttu-id="5489f-105">本節說明 Windows Shell 色彩調色板處理函式。</span><span class="sxs-lookup"><span data-stu-id="5489f-105">This section describes the Windows Shell color palette handling functions.</span></span> <span data-ttu-id="5489f-106">本檔中所述的程式設計項目是由 Shlwapi.dll 匯出，並定義于 Shlwapi 和 Shlwapi 中。</span><span class="sxs-lookup"><span data-stu-id="5489f-106">The programming elements explained in this documentation are exported by Shlwapi.dll and defined in Shlwapi.h and Shlwapi.lib.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5489f-107">本節內容</span><span class="sxs-lookup"><span data-stu-id="5489f-107">In this section</span></span>



| <span data-ttu-id="5489f-108">主題</span><span class="sxs-lookup"><span data-stu-id="5489f-108">Topic</span></span>                                                           | <span data-ttu-id="5489f-109">描述</span><span class="sxs-lookup"><span data-stu-id="5489f-109">Description</span></span>                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="5489f-110">**ColorAdjustLuma**</span><span class="sxs-lookup"><span data-stu-id="5489f-110">**ColorAdjustLuma**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-coloradjustluma)<br/>           | <span data-ttu-id="5489f-111">變更 RGB 值的亮度。</span><span class="sxs-lookup"><span data-stu-id="5489f-111">Changes the luminance of a RGB value.</span></span> <span data-ttu-id="5489f-112">色調和飽和度不會受到影響。</span><span class="sxs-lookup"><span data-stu-id="5489f-112">Hue and saturation are not affected.</span></span><br/> |
| [<span data-ttu-id="5489f-113">**ColorHLSToRGB**</span><span class="sxs-lookup"><span data-stu-id="5489f-113">**ColorHLSToRGB**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorhlstorgb)<br/>               | <span data-ttu-id="5489f-114">將色彩從色調-亮度-飽和度 (HLS) 轉換為 RGB 格式。</span><span class="sxs-lookup"><span data-stu-id="5489f-114">Converts colors from hue-luminance-saturation (HLS) to RGB format.</span></span><br/>         |
| [<span data-ttu-id="5489f-115">**ColorRGBToHLS**</span><span class="sxs-lookup"><span data-stu-id="5489f-115">**ColorRGBToHLS**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-colorrgbtohls)<br/>               | <span data-ttu-id="5489f-116">將色彩從 RGB 轉換為色調-亮度-飽和度 (HLS) 格式。</span><span class="sxs-lookup"><span data-stu-id="5489f-116">Converts colors from RGB to hue-luminance-saturation (HLS) format.</span></span><br/>         |
| [<span data-ttu-id="5489f-117">**SHCreateShellPalette**</span><span class="sxs-lookup"><span data-stu-id="5489f-117">**SHCreateShellPalette**</span></span>](/windows/desktop/api/Shlwapi/nf-shlwapi-shcreateshellpalette)<br/> | <span data-ttu-id="5489f-118">建立指定之裝置內容的半色調調色板。</span><span class="sxs-lookup"><span data-stu-id="5489f-118">Creates a halftone palette for the specified device context.</span></span><br/>               |



 

 

 




