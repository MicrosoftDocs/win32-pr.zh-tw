---
title: 嵌套中繼檔
description: 嵌套中繼檔
ms.assetid: fa355c98-31e2-4bb9-ad67-fd9a727300c3
keywords:
- Windows Media 中繼檔，嵌套
- Windows Media 中繼檔，參考其他中繼檔
- 嵌套中繼檔
- 中繼檔，嵌套
- 中繼檔，參考其他中繼檔
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3cd5743424858c4bbcd6f66952f4275ea82d947e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300167"
---
# <a name="nesting-metafiles"></a><span data-ttu-id="bb8fc-108">嵌套中繼檔</span><span class="sxs-lookup"><span data-stu-id="bb8fc-108">Nesting Metafiles</span></span>

<span data-ttu-id="bb8fc-109">中繼檔可以參考另一個中繼檔。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-109">A metafile can reference another metafile.</span></span> <span data-ttu-id="bb8fc-110">若要參考另一個中繼檔，請使用 **ENTRYREF** 元素。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-110">To reference another metafile, use the **ENTRYREF** element.</span></span> <span data-ttu-id="bb8fc-111">主要中繼檔中的 **ENTRYREF** 元素會指向外部中繼檔。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-111">An **ENTRYREF** element in the primary metafile points to an external metafile.</span></span>

<span data-ttu-id="bb8fc-112">Windows Media Player 控制項會處理參考之中繼檔的 **專案專案** ，就如同它們是包含在 **ENTRYREF** 元素位置的主要中繼檔中一樣。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-112">The Windows Media Player control processes the **ENTRY** elements of the referenced metafile as if they were included in the primary metafile at the position of the **ENTRYREF** element.</span></span> <span data-ttu-id="bb8fc-113">但是，它會略過參考的中繼檔中，將 **SKIPIFREF** 屬性設定為 YES 的任何 **專案專案**。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-113">However, it skips any **ENTRY** elements in the referenced metafile that have the **SKIPIFREF** attribute set to YES.</span></span>

<span data-ttu-id="bb8fc-114">Windows XP 控制項的 Windows Media Player 7.0、7.1 和 Windows Media Player 會忽略參考的中繼檔中的任何 **ENTRYREF** 元素。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-114">The Windows Media Player 7.0, 7.1, and Windows Media Player for Windows XP controls ignore any **ENTRYREF** elements in the referenced metafile.</span></span> <span data-ttu-id="bb8fc-115">因此，您只能使用這些版本來將中繼檔的深度嵌套一層。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-115">Thus, metafiles can only be nested one level deep using these versions.</span></span> <span data-ttu-id="bb8fc-116">這些版本也會忽略所參考檔案中的 **ASX** 元素及其屬性。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-116">These versions also ignore the **ASX** element and its attributes in the referenced file.</span></span> <span data-ttu-id="bb8fc-117">Windows Media Player 9 系列或更新版本支援最多5個深度的嵌套中繼檔。</span><span class="sxs-lookup"><span data-stu-id="bb8fc-117">Windows Media Player 9 Series or later supports nesting metafiles up to 5 deep.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb8fc-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="bb8fc-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8fc-119">**建立中繼檔播放清單**</span><span class="sxs-lookup"><span data-stu-id="bb8fc-119">**Creating Metafile Playlists**</span></span>](creating-metafile-playlists.md)
</dt> </dl>

 

 




