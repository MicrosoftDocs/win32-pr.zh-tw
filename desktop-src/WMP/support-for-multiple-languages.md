---
title: 支援多種語言
description: 支援多種語言
ms.assetid: f46efb7f-73d1-4f64-aa44-cb50170a2245
keywords:
- Windows Media 中繼檔播放清單，支援多種語言
- 中繼檔播放清單，支援多種語言
- 播放清單、支援多種語言
- Windows Media 中繼檔播放清單，支援多種語言
- 中繼檔播放清單，支援多種語言
- 播放清單、多重語言支援
- Windows Media 中繼檔播放清單，語言支援
- 中繼檔播放清單，語言支援
- 播放清單、語言支援
- 支援多種語言
- 多重語言支援
- 語言支援
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d8855aeb798e4243182a6f82479289ccccbd97d8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021929"
---
# <a name="support-for-multiple-languages"></a><span data-ttu-id="39fee-115">支援多種語言</span><span class="sxs-lookup"><span data-stu-id="39fee-115">Support for Multiple Languages</span></span>

<span data-ttu-id="39fee-116">Windows Media Player 9 系列或更新版本支援使用 Unicode 字元集建立的 Windows Media 中繼檔。</span><span class="sxs-lookup"><span data-stu-id="39fee-116">Windows Media Player 9 Series or later supports Windows Media metafiles created using the Unicode character set.</span></span> <span data-ttu-id="39fee-117">這可讓您在中繼檔播放清單中包含多語系中繼資料。</span><span class="sxs-lookup"><span data-stu-id="39fee-117">This allows you to include multilingual metadata in your metafile playlist.</span></span> <span data-ttu-id="39fee-118">下列規則會管理在 Windows Media 中繼檔中使用多語系中繼資料的方式：</span><span class="sxs-lookup"><span data-stu-id="39fee-118">The following rules govern the use of multilingual metadata in Windows Media metafiles:</span></span>

-   <span data-ttu-id="39fee-119">字元必須使用 UTF-8 編碼配置進行編碼。</span><span class="sxs-lookup"><span data-stu-id="39fee-119">Characters must be encoded using the UTF-8 encoding scheme.</span></span>
-   <span data-ttu-id="39fee-120">中繼檔播放清單必須在播放清單層級包含下列 **參數** ：</span><span class="sxs-lookup"><span data-stu-id="39fee-120">The metafile playlist must include the following **PARAM** at the playlist level:</span></span>
    ```XML
    <PARAM  NAME = "Encoding"  VALUE = "utf-8">
    
    ```

    

-   <span data-ttu-id="39fee-121">只有 Windows Media Player 9 系列或更新版本才支援此功能。</span><span class="sxs-lookup"><span data-stu-id="39fee-121">Only Windows Media Player 9 Series or later supports this functionality.</span></span>
-   <span data-ttu-id="39fee-122">如果未使用 UTF-8 編碼和正確的 **PARAM** 專案儲存中繼檔播放清單，則會使用使用者電腦的預設系統地區設定字碼頁面來剖析中繼檔播放清單。</span><span class="sxs-lookup"><span data-stu-id="39fee-122">If the metafile playlist is not saved with UTF-8 encoding and the correct **PARAM** element, it will be parsed using the default system locale code page of the user's computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39fee-123">相關主題</span><span class="sxs-lookup"><span data-stu-id="39fee-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39fee-124">**PARAM 元素**</span><span class="sxs-lookup"><span data-stu-id="39fee-124">**PARAM Element**</span></span>](param-element.md)
</dt> <dt>

[<span data-ttu-id="39fee-125">**Windows Media 中繼檔總覽**</span><span class="sxs-lookup"><span data-stu-id="39fee-125">**Windows Media Metafiles Overview**</span></span>](windows-media-metafiles-overview.md)
</dt> </dl>

 

 




