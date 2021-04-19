---
title: Network. 幀
description: '[畫面播放速率] 屬性會以每數百秒的畫面格速率抓取目前的影片畫面速率。 例如，值2998表示每秒29.98 個畫面格。'
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- 網路. 幀 Windows Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989862"
---
# <a name="networkframerate"></a><span data-ttu-id="c7d85-105">Network. 幀</span><span class="sxs-lookup"><span data-stu-id="c7d85-105">Network.frameRate</span></span>

<span data-ttu-id="c7d85-106">[ **幀** 速率] 屬性會以每數百秒的畫面格速率抓取目前的影片畫面速率。</span><span class="sxs-lookup"><span data-stu-id="c7d85-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="c7d85-107">例如，值2998表示每秒29.98 個畫面格。</span><span class="sxs-lookup"><span data-stu-id="c7d85-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7d85-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7d85-108">Syntax</span></span>

<span data-ttu-id="c7d85-109">*玩家*。*網路*。**畫面播放速率**</span><span class="sxs-lookup"><span data-stu-id="c7d85-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c7d85-110">可能的值</span><span class="sxs-lookup"><span data-stu-id="c7d85-110">Possible Values</span></span>

<span data-ttu-id="c7d85-111">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="c7d85-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="c7d85-112">範例</span><span class="sxs-lookup"><span data-stu-id="c7d85-112">Examples</span></span>

<span data-ttu-id="c7d85-113">下列 JScript 範例會使用 *網路*。顯示目前畫面播放速率的 **幀** 速率。</span><span class="sxs-lookup"><span data-stu-id="c7d85-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="c7d85-114">這項資訊會顯示在以 ID = "FR" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="c7d85-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="c7d85-115">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c7d85-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c7d85-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7d85-116">Requirements</span></span>



| <span data-ttu-id="c7d85-117">需求</span><span class="sxs-lookup"><span data-stu-id="c7d85-117">Requirement</span></span> | <span data-ttu-id="c7d85-118">值</span><span class="sxs-lookup"><span data-stu-id="c7d85-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d85-119">版本</span><span class="sxs-lookup"><span data-stu-id="c7d85-119">Version</span></span><br/> | <span data-ttu-id="c7d85-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c7d85-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c7d85-121">DLL</span><span class="sxs-lookup"><span data-stu-id="c7d85-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="c7d85-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7d85-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d85-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7d85-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d85-124">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="c7d85-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c7d85-125">**EncodedFrameRate**</span><span class="sxs-lookup"><span data-stu-id="c7d85-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





