---
title: FramesSkipped
description: FramesSkipped 屬性會抓取播放期間略過的總畫面格數。
ms.assetid: fc7561a4-1e52-4192-b8df-ed2fb407fb78
keywords:
- FramesSkipped Windows Media Player
topic_type:
- apiref
api_name:
- Network.framesSkipped
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f33b778fffce071c47cb455f09e468243abab6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989861"
---
# <a name="networkframesskipped"></a><span data-ttu-id="6953c-104">FramesSkipped</span><span class="sxs-lookup"><span data-stu-id="6953c-104">Network.framesSkipped</span></span>

<span data-ttu-id="6953c-105">**FramesSkipped** 屬性會抓取播放期間略過的總畫面格數。</span><span class="sxs-lookup"><span data-stu-id="6953c-105">The **framesSkipped** property retrieves the total number of frames skipped during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="6953c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6953c-106">Syntax</span></span>

<span data-ttu-id="6953c-107">*玩家*。*網路*。**framesSkipped**</span><span class="sxs-lookup"><span data-stu-id="6953c-107">*player*.*network*.**framesSkipped**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6953c-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="6953c-108">Possible Values</span></span>

<span data-ttu-id="6953c-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="6953c-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="6953c-110">範例</span><span class="sxs-lookup"><span data-stu-id="6953c-110">Examples</span></span>

<span data-ttu-id="6953c-111">下列 JScript 範例會使用 *網路*。**framesSkipped** 可顯示當使用者按一下按鈕時，播放期間略過的框架總數。</span><span class="sxs-lookup"><span data-stu-id="6953c-111">The following JScript example uses *Network*.**framesSkipped** to display the total number of frames skipped during playback when the user clicks a button.</span></span> <span data-ttu-id="6953c-112">這項資訊會顯示在以 ID = "FS" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="6953c-112">The information is displayed in an HTML DIV created with ID = "FS".</span></span> <span data-ttu-id="6953c-113">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="6953c-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "skipped" NAME = "skipped"
       VALUE = "Count frames skipped" 
       onClick = "FS.innerHTML = 'Frames skipped: ' + Player.network.framesSkipped;">

```



## <a name="requirements"></a><span data-ttu-id="6953c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6953c-114">Requirements</span></span>



| <span data-ttu-id="6953c-115">需求</span><span class="sxs-lookup"><span data-stu-id="6953c-115">Requirement</span></span> | <span data-ttu-id="6953c-116">值</span><span class="sxs-lookup"><span data-stu-id="6953c-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6953c-117">版本</span><span class="sxs-lookup"><span data-stu-id="6953c-117">Version</span></span><br/> | <span data-ttu-id="6953c-118">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6953c-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6953c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6953c-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="6953c-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6953c-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6953c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6953c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6953c-122">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="6953c-122">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





