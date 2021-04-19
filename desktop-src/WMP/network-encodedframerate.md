---
title: EncodedFrameRate
description: EncodedFrameRate 屬性會以每秒畫面格的畫面數來抓取內容作者所指定的影片畫面播放速率。
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- EncodedFrameRate Windows Media Player
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999618"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="fb6f6-104">EncodedFrameRate</span><span class="sxs-lookup"><span data-stu-id="fb6f6-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="fb6f6-105">**EncodedFrameRate** 屬性會以每秒畫面格的畫面數來抓取內容作者所指定的影片畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="fb6f6-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb6f6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb6f6-106">Syntax</span></span>

<span data-ttu-id="fb6f6-107">*玩家*。*網路*。**encodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="fb6f6-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="fb6f6-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="fb6f6-108">Possible Values</span></span>

<span data-ttu-id="fb6f6-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="fb6f6-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="fb6f6-110">範例</span><span class="sxs-lookup"><span data-stu-id="fb6f6-110">Examples</span></span>

<span data-ttu-id="fb6f6-111">下列 JScript 範例會使用 *網路*。**encodedFrameRate** 可顯示編碼檔案時所指定的畫面播放速率。</span><span class="sxs-lookup"><span data-stu-id="fb6f6-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="fb6f6-112">這項資訊會顯示在以 ID = "FR" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="fb6f6-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="fb6f6-113">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="fb6f6-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="fb6f6-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb6f6-114">Requirements</span></span>



| <span data-ttu-id="fb6f6-115">需求</span><span class="sxs-lookup"><span data-stu-id="fb6f6-115">Requirement</span></span> | <span data-ttu-id="fb6f6-116">值</span><span class="sxs-lookup"><span data-stu-id="fb6f6-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb6f6-117">版本</span><span class="sxs-lookup"><span data-stu-id="fb6f6-117">Version</span></span><br/> | <span data-ttu-id="fb6f6-118">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="fb6f6-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fb6f6-119">DLL</span><span class="sxs-lookup"><span data-stu-id="fb6f6-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="fb6f6-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb6f6-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb6f6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb6f6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb6f6-122">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="fb6f6-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="fb6f6-123">**Network. 幀**</span><span class="sxs-lookup"><span data-stu-id="fb6f6-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





