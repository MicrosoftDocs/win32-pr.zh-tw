---
title: 新增播放清單
description: 新增播放清單
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- 建立外觀、播放清單
- Windows Media Player 的外觀、播放清單
- 外觀，播放清單
- 播放清單、外觀
- 中繼檔播放清單，外觀
- Windows Media 中繼檔播放清單，外觀
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968648"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="31d27-109">新增播放清單</span><span class="sxs-lookup"><span data-stu-id="31d27-109">Adding a Playlist</span></span>

<span data-ttu-id="31d27-110">您可以使用播放清單從音訊和影片的集合中選擇。</span><span class="sxs-lookup"><span data-stu-id="31d27-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="31d27-111">您可以使用第一個面板中的圖稿，對外觀定義檔進行一些變更。</span><span class="sxs-lookup"><span data-stu-id="31d27-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="31d27-112">第一個步驟是使用您將用於大部分外觀的 shell：</span><span class="sxs-lookup"><span data-stu-id="31d27-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="31d27-113">現在新增包含播放清單的第二個 **視圖**。</span><span class="sxs-lookup"><span data-stu-id="31d27-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="31d27-114">將下列程式碼放在 </VIEW> shell 程式碼的後面。</span><span class="sxs-lookup"><span data-stu-id="31d27-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="31d27-115">您將需要提供第二個 view 的識別碼，讓您稍後可以參考它。</span><span class="sxs-lookup"><span data-stu-id="31d27-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="31d27-116">新增 PLAYELEMENT 和 STOPELEMENT。</span><span class="sxs-lookup"><span data-stu-id="31d27-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="31d27-117">這些預先定義的按鈕可讓您更輕鬆地使用。</span><span class="sxs-lookup"><span data-stu-id="31d27-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="31d27-118">最後，將 onClick 事件新增至 PLAYELEMENT，以在第二個視圖中顯示播放清單：</span><span class="sxs-lookup"><span data-stu-id="31d27-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="31d27-119">您可以在 SDK 的 [範例] 區段中看到類似的工作播放清單面板。</span><span class="sxs-lookup"><span data-stu-id="31d27-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31d27-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="31d27-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31d27-121">**外觀建立指南**</span><span class="sxs-lookup"><span data-stu-id="31d27-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




