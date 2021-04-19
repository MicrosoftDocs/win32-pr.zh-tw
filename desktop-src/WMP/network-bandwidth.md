---
title: 網路。頻寬
description: 頻寬屬性會抓取剪輯目前的頻寬。
ms.assetid: 2ef86f2a-98e9-4544-a740-c2237f06c135
keywords:
- Network. 頻寬 Windows Media Player
topic_type:
- apiref
api_name:
- Network.bandWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4783d86160070fc61202f97b4cf3882f2cebcfb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993271"
---
# <a name="networkbandwidth"></a><span data-ttu-id="867ab-104">網路。頻寬</span><span class="sxs-lookup"><span data-stu-id="867ab-104">Network.bandWidth</span></span>

<span data-ttu-id="867ab-105">**頻寬** 屬性會抓取剪輯目前的頻寬。</span><span class="sxs-lookup"><span data-stu-id="867ab-105">The **bandWidth** property retrieves the current bandwidth of the clip.</span></span>

## <a name="syntax"></a><span data-ttu-id="867ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="867ab-106">Syntax</span></span>

<span data-ttu-id="867ab-107">*玩家*。*網路*。**頻寬**</span><span class="sxs-lookup"><span data-stu-id="867ab-107">*player*.*network*.**bandWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="867ab-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="867ab-108">Possible Values</span></span>

<span data-ttu-id="867ab-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="867ab-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="867ab-110">備註</span><span class="sxs-lookup"><span data-stu-id="867ab-110">Remarks</span></span>

<span data-ttu-id="867ab-111">如果 *播放玩家*，這個屬性會傳回零。未設定 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="867ab-111">This property returns zero if the *Player*.**URL** property is not set.</span></span> <span data-ttu-id="867ab-112">這個屬性只對串流媒體有效。</span><span class="sxs-lookup"><span data-stu-id="867ab-112">This property is only valid for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="867ab-113">範例</span><span class="sxs-lookup"><span data-stu-id="867ab-113">Examples</span></span>

<span data-ttu-id="867ab-114">下列 Microsoft JScript 範例使用 *網路*。顯示目前媒體頻寬的 **頻寬** 。</span><span class="sxs-lookup"><span data-stu-id="867ab-114">The following Microsoft JScript example uses *Network*.**bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="867ab-115">這項資訊會顯示在以 ID = "BW" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="867ab-115">The information is displayed in an HTML DIV created with ID = "BW".</span></span> <span data-ttu-id="867ab-116">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="867ab-116">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state.-->
<SCRIPT FOR = Player EVENT = PlayStateChange()>

   switch (Player.playState){

      case 3:

         if (Player.network.bandwidth != 0){
  
            BW.innerHTML = "Current Bandwidth: " + Player.network.bandWidth;
            BW.innerHTML += " K bits/second";
         }

         else
            BW.innerHTML = "Bandwidth is only available for streaming media.";

            break;

      default:
}
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="867ab-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="867ab-117">Requirements</span></span>



| <span data-ttu-id="867ab-118">需求</span><span class="sxs-lookup"><span data-stu-id="867ab-118">Requirement</span></span> | <span data-ttu-id="867ab-119">值</span><span class="sxs-lookup"><span data-stu-id="867ab-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="867ab-120">版本</span><span class="sxs-lookup"><span data-stu-id="867ab-120">Version</span></span><br/> | <span data-ttu-id="867ab-121">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="867ab-121">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="867ab-122">DLL</span><span class="sxs-lookup"><span data-stu-id="867ab-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="867ab-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="867ab-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="867ab-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="867ab-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="867ab-125">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="867ab-125">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="867ab-126">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="867ab-126">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





