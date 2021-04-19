---
title: Network. 位元速率
description: 位元速率屬性會抓取目前接收的位速率。
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- 網路位元速率 Windows Media Player
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990145"
---
# <a name="networkbitrate"></a><span data-ttu-id="a1f80-104">Network. 位元速率</span><span class="sxs-lookup"><span data-stu-id="a1f80-104">Network.bitRate</span></span>

<span data-ttu-id="a1f80-105">**位元速率** 屬性會抓取目前接收的位速率。</span><span class="sxs-lookup"><span data-stu-id="a1f80-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1f80-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1f80-106">Syntax</span></span>

<span data-ttu-id="a1f80-107">*玩家*。*網路*。**位元速率**</span><span class="sxs-lookup"><span data-stu-id="a1f80-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a1f80-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="a1f80-108">Possible Values</span></span>

<span data-ttu-id="a1f80-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="a1f80-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a1f80-110">備註</span><span class="sxs-lookup"><span data-stu-id="a1f80-110">Remarks</span></span>

<span data-ttu-id="a1f80-111">此值是目前影片和音訊串流的位元速率組合。</span><span class="sxs-lookup"><span data-stu-id="a1f80-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="a1f80-112">範例</span><span class="sxs-lookup"><span data-stu-id="a1f80-112">Examples</span></span>

<span data-ttu-id="a1f80-113">下列 JScript 範例會使用 *網路*。**位元速率** 顯示目前的媒體位元速率。</span><span class="sxs-lookup"><span data-stu-id="a1f80-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="a1f80-114">這項資訊會顯示在以 ID = "BR" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="a1f80-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="a1f80-115">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="a1f80-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a1f80-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1f80-116">Requirements</span></span>



| <span data-ttu-id="a1f80-117">需求</span><span class="sxs-lookup"><span data-stu-id="a1f80-117">Requirement</span></span> | <span data-ttu-id="a1f80-118">值</span><span class="sxs-lookup"><span data-stu-id="a1f80-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a1f80-119">版本</span><span class="sxs-lookup"><span data-stu-id="a1f80-119">Version</span></span><br/> | <span data-ttu-id="a1f80-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a1f80-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a1f80-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a1f80-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1f80-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1f80-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1f80-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a1f80-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1f80-124">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="a1f80-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





