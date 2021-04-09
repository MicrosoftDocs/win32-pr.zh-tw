---
title: 標記
description: 標記
ms.assetid: ba9bc93e-76a9-4a49-951f-c38dbcceef8c
keywords:
- Windows Media Format SDK，標記
- Advanced Systems Format (ASF) ，標記
- ASF (Advanced Systems Format) ，標記
- 標記，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d314b4e74aa05a08dfd4a297687662e10f045abc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840776"
---
# <a name="markers"></a><span data-ttu-id="3f198-107">標記</span><span class="sxs-lookup"><span data-stu-id="3f198-107">Markers</span></span>

<span data-ttu-id="3f198-108">標記是在 ASF 檔案的時間軸上命名的位置。</span><span class="sxs-lookup"><span data-stu-id="3f198-108">Markers are named places on the timeline of an ASF file.</span></span> <span data-ttu-id="3f198-109">每個標記都有您指派的名稱和呈現時間。</span><span class="sxs-lookup"><span data-stu-id="3f198-109">Each marker has a name and a presentation time that you assign.</span></span> <span data-ttu-id="3f198-110">您可以指定檔案所需數量的標記。</span><span class="sxs-lookup"><span data-stu-id="3f198-110">You can specify as many markers as you need for a file.</span></span>

<span data-ttu-id="3f198-111">標記適用于將大型 ASF 檔案分割為邏輯片段。</span><span class="sxs-lookup"><span data-stu-id="3f198-111">Markers are useful for breaking up large ASF files in to logical pieces.</span></span> <span data-ttu-id="3f198-112">使用 reader 物件播放 ASF 檔案的應用程式，可以讓使用者選擇從標記跳至標記，以簡化數位媒體的導覽。</span><span class="sxs-lookup"><span data-stu-id="3f198-112">An application that uses the reader object to play ASF files can provide the user with the option to skip from marker to marker, simplifying navigation of digital media.</span></span> <span data-ttu-id="3f198-113">例如，如果您要將 ASF 檔案從簡報中移出，您可以在時間軸中，為每個討論的主要主題放入標記。</span><span class="sxs-lookup"><span data-stu-id="3f198-113">For example, if you are making an ASF file out of a presentation, you can put markers in the timeline for each major topic that is discussed.</span></span> <span data-ttu-id="3f198-114">在播放時，使用者可以直接從清單中挑選主題，並直接移至檔案的相關部分，而不是取得一長時間的時間軸，而且必須在要搜尋的位置上猜測。</span><span class="sxs-lookup"><span data-stu-id="3f198-114">On playback, instead of getting one long timeline and having to guess at the location to seek to, a user can simply pick a topic from a list and go right to the pertinent portion of the file.</span></span>

<span data-ttu-id="3f198-115">標記是由中繼資料編輯器物件操作。</span><span class="sxs-lookup"><span data-stu-id="3f198-115">Markers are manipulated by the metadata editor object.</span></span> <span data-ttu-id="3f198-116">寫入檔案之後，您隨時都可以新增、移除和查看檔案中的標記。</span><span class="sxs-lookup"><span data-stu-id="3f198-116">You can add, remove, and view the markers in a file at any time after the file has been written.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3f198-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="3f198-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f198-118">**ASF 檔案功能**</span><span class="sxs-lookup"><span data-stu-id="3f198-118">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="3f198-119">**搜尋標記**</span><span class="sxs-lookup"><span data-stu-id="3f198-119">**To Seek to Markers**</span></span>](to-seek-to-markers.md)
</dt> <dt>

[<span data-ttu-id="3f198-120">**使用標記**</span><span class="sxs-lookup"><span data-stu-id="3f198-120">**Using Markers**</span></span>](using-markers.md)
</dt> </dl>

 

 




