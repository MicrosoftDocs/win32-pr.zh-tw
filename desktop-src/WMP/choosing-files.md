---
title: 選擇檔案
description: 選擇檔案
ms.assetid: dfa44a32-7d72-47f7-a872-33b823a34798
keywords:
- 建立外觀，選擇檔案
- Windows Media Player 的外觀，選擇檔案
- 外觀，選擇檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0098a37635c52ba3e48fb77f07a5868ceb957239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183951"
---
# <a name="choosing-files"></a><span data-ttu-id="e0e32-106">選擇檔案</span><span class="sxs-lookup"><span data-stu-id="e0e32-106">Choosing Files</span></span>

<span data-ttu-id="e0e32-107">如果您想要選擇檔案，您可以使用類似播放清單範例的程式碼，但請將下列內容取代為 PLAYELEMENT 區段：</span><span class="sxs-lookup"><span data-stu-id="e0e32-107">If you want to choose a file, you can use code similar to the Playlist example, but substitute the following for the PLAYELEMENT section:</span></span>


```C++
<PLAYELEMENT
  mappingColor = "#00FF00"
  onClick = "JScript:player.URL=theme.openDialog('FILE_OPEN','FILES_ALL');"
  />

```



<span data-ttu-id="e0e32-108">這一行會使用 **主題** 的 **openDialog** 方法來定義播放程式的 **URL** 。</span><span class="sxs-lookup"><span data-stu-id="e0e32-108">This line will use the **openDialog** method of **THEME** to define a **URL** for the player.</span></span> <span data-ttu-id="e0e32-109">您可以使用這個來選擇不在播放清單中的檔案。</span><span class="sxs-lookup"><span data-stu-id="e0e32-109">You can use this to choose files that are not in playlists.</span></span>

<span data-ttu-id="e0e32-110">您可以在 SDK 的範例區段中看到類似的工作 **openDialog** 範例。</span><span class="sxs-lookup"><span data-stu-id="e0e32-110">You can see a similar working **openDialog** example in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0e32-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e0e32-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0e32-112">**外觀建立指南**</span><span class="sxs-lookup"><span data-stu-id="e0e32-112">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




