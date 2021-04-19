---
title: LostPackets
description: LostPackets 屬性會捕獲遺失的封包數目。
ms.assetid: b90faaaf-656a-4b9b-abfe-370e6f7c7c4b
keywords:
- LostPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.lostPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a780afaea1ba46c5e2d5c7eb55b9476f68c9570
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997697"
---
# <a name="networklostpackets"></a><span data-ttu-id="d3f8a-104">LostPackets</span><span class="sxs-lookup"><span data-stu-id="d3f8a-104">Network.lostPackets</span></span>

<span data-ttu-id="d3f8a-105">**LostPackets** 屬性會捕獲遺失的封包數目。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-105">The **lostPackets** property retrieves the number of packets lost.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3f8a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3f8a-106">Syntax</span></span>

<span data-ttu-id="d3f8a-107">*玩家*。*網路*。**lostPackets**</span><span class="sxs-lookup"><span data-stu-id="d3f8a-107">*player*.*network*.**lostPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d3f8a-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="d3f8a-108">Possible Values</span></span>

<span data-ttu-id="d3f8a-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="d3f8a-110">備註</span><span class="sxs-lookup"><span data-stu-id="d3f8a-110">Remarks</span></span>

<span data-ttu-id="d3f8a-111">這個屬性僅適用于串流媒體，而且在使用 HTTP 通訊協定（不失真）時，將會等於零。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-111">This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless.</span></span>

<span data-ttu-id="d3f8a-112">封包可能因為許多原因而遺失，例如網路連線的類型和品質。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-112">Packets may be lost for a number of reasons, such as the type and quality of the network connection.</span></span>

<span data-ttu-id="d3f8a-113">每次播放都會停止並重新啟動，這個屬性會設定為零。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="d3f8a-114">如果播放暫停並重新啟動，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-114">It is not reset if playback is paused and restarted.</span></span> <span data-ttu-id="d3f8a-115">這個屬性只有在執行時間才會傳回有效的資訊，而且只有在 *播放玩家* 時才會傳回。已設定 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-115">This property returns valid information only during run time, and only if the *Player*.**URL** property is set.</span></span>

## <a name="examples"></a><span data-ttu-id="d3f8a-116">範例</span><span class="sxs-lookup"><span data-stu-id="d3f8a-116">Examples</span></span>

<span data-ttu-id="d3f8a-117">下列 JScript 範例會使用 *網路*。**lostPackets** 可顯示當使用者按一下按鈕時，播放時遺失的封包總數。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-117">The following JScript example uses *Network*.**lostPackets** to display the total number of packets lost during playback when the user clicks a button.</span></span> <span data-ttu-id="d3f8a-118">這項資訊會顯示在以 ID = "LP" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-118">The information is displayed in an HTML DIV created with ID = "LP".</span></span> <span data-ttu-id="d3f8a-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an HTML BUTTON element. -->
<INPUT TYPE = "BUTTON" ID = "lostpkts" NAME = "lostpkts"
       VALUE = "Count lost packets" 
       onClick = "LP.innerHTML = 'Packets lost: ' + Player.network.lostPackets;">

```



## <a name="requirements"></a><span data-ttu-id="d3f8a-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3f8a-120">Requirements</span></span>



| <span data-ttu-id="d3f8a-121">需求</span><span class="sxs-lookup"><span data-stu-id="d3f8a-121">Requirement</span></span> | <span data-ttu-id="d3f8a-122">值</span><span class="sxs-lookup"><span data-stu-id="d3f8a-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3f8a-123">版本</span><span class="sxs-lookup"><span data-stu-id="d3f8a-123">Version</span></span><br/> | <span data-ttu-id="d3f8a-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d3f8a-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d3f8a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d3f8a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d3f8a-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3f8a-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3f8a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3f8a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3f8a-128">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="d3f8a-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="d3f8a-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="d3f8a-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





