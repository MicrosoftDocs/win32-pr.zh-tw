---
title: Windows Media 中繼檔參考
description: Windows Media 中繼檔參考
ms.assetid: 03dadba3-0143-46f0-990a-108196eb58ab
keywords:
- Windows Media 中繼檔，參考
- 中繼檔，參考
- Windows Media 中繼檔的參考
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 31d2c8d20d64e9a363fb37594519253206d30483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021412"
---
# <a name="windows-media-metafile-reference"></a><span data-ttu-id="6661a-106">Windows Media 中繼檔參考</span><span class="sxs-lookup"><span data-stu-id="6661a-106">Windows Media Metafile Reference</span></span>

<span data-ttu-id="6661a-107">本參考檔是 Windows Media 中繼檔的元素和副檔名。</span><span class="sxs-lookup"><span data-stu-id="6661a-107">This reference documents elements and file name extensions for Windows Media metafiles.</span></span> <span data-ttu-id="6661a-108">參考分成下列各節。</span><span class="sxs-lookup"><span data-stu-id="6661a-108">The reference is divided into the following sections.</span></span>



| <span data-ttu-id="6661a-109">區段</span><span class="sxs-lookup"><span data-stu-id="6661a-109">Section</span></span>                                                                                    | <span data-ttu-id="6661a-110">描述</span><span class="sxs-lookup"><span data-stu-id="6661a-110">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6661a-111">Windows Media 中繼檔元素參考</span><span class="sxs-lookup"><span data-stu-id="6661a-111">Windows Media Metafile Elements Reference</span></span>](windows-media-metafile-elements-reference.md) | <span data-ttu-id="6661a-112">記載中繼檔元素，包括定義、屬性和其值，以及與每個專案相關的特殊條件。</span><span class="sxs-lookup"><span data-stu-id="6661a-112">Documents metafile elements, including definitions, attributes and their values, and special conditions related to each element.</span></span> |
| [<span data-ttu-id="6661a-113">副檔名</span><span class="sxs-lookup"><span data-stu-id="6661a-113">File Name Extensions</span></span>](file-name-extensions.md)                                           | <span data-ttu-id="6661a-114">檔中繼檔副檔名，以及其使用規則和指導方針。</span><span class="sxs-lookup"><span data-stu-id="6661a-114">Documents metafile file name extensions with rules and guidelines on their use.</span></span>                                                  |



 

<span data-ttu-id="6661a-115">Windows Media 中繼檔是提供檔案資料流程及其簡報相關資訊的文字檔。</span><span class="sxs-lookup"><span data-stu-id="6661a-115">Windows Media metafiles are text files that provide information about a file stream and its presentation.</span></span> <span data-ttu-id="6661a-116">中繼檔是以可延伸標記語言 (XML)  (XML) 語法為基礎，而且是由各種類似 XML 的元素所組成，以及它們的標記和屬性。</span><span class="sxs-lookup"><span data-stu-id="6661a-116">The metafiles are based on the Extensible Markup Language (XML) syntax, and are made up of various XML-like elements with their tags and attributes.</span></span> <span data-ttu-id="6661a-117">每個元素都會定義串流媒體的設定或動作。</span><span class="sxs-lookup"><span data-stu-id="6661a-117">Each element defines a setting or action for streaming media.</span></span>

<span data-ttu-id="6661a-118">有兩組元素標記可供中繼檔使用。</span><span class="sxs-lookup"><span data-stu-id="6661a-118">There are two sets of element tags available for metafiles.</span></span> <span data-ttu-id="6661a-119">用戶端中繼檔有一組專案，而伺服器端中繼檔則有另一組元素。</span><span class="sxs-lookup"><span data-stu-id="6661a-119">Client-side metafiles have one set of elements, and server-side metafiles have another set of elements.</span></span>

<span data-ttu-id="6661a-120">如果專案標記沒有任何子項目 (修改或包含在另一個專案) 中的專案，就可以在開頭標記的結尾處使用單一斜線字元 (/) 來取代結束記號。</span><span class="sxs-lookup"><span data-stu-id="6661a-120">If an element tag does not have any child elements (those that modify or are contained within another element), a single slash character (/) can be used at the end of the opening tag in place of a closing tag.</span></span> <span data-ttu-id="6661a-121">如果專案的開頭和結束記號之間沒有子項目，則它們不是該專案的子專案，而且會被忽略，或在中繼檔的語法中造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="6661a-121">If child elements do not appear between the opening and closing tag for an element, they are not child elements for that element, and are ignored or cause an error in the syntax of the metafile.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6661a-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="6661a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6661a-123">**關於 Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="6661a-123">**About Windows Media Metafiles**</span></span>](about-windows-media-metafiles.md)
</dt> <dt>

[<span data-ttu-id="6661a-124">**Windows Media 中繼檔指南**</span><span class="sxs-lookup"><span data-stu-id="6661a-124">**Windows Media Metafile Guide**</span></span>](windows-media-metafile-guide.md)
</dt> <dt>

[<span data-ttu-id="6661a-125">**Windows Media 中繼檔**</span><span class="sxs-lookup"><span data-stu-id="6661a-125">**Windows Media Metafiles**</span></span>](windows-media-metafiles.md)
</dt> </dl>

 

 




