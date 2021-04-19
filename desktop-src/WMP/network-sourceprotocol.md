---
title: SourceProtocol
description: SourceProtocol 屬性會抓取用來接收資料的來源通訊協定。
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- SourceProtocol Windows Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998756"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="d0578-104">SourceProtocol</span><span class="sxs-lookup"><span data-stu-id="d0578-104">Network.sourceProtocol</span></span>

<span data-ttu-id="d0578-105">**SourceProtocol** 屬性會抓取用來接收資料的來源通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d0578-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0578-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d0578-106">Syntax</span></span>

<span data-ttu-id="d0578-107">*玩家*。*網路*。**sourceProtocol**</span><span class="sxs-lookup"><span data-stu-id="d0578-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d0578-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="d0578-108">Possible Values</span></span>

<span data-ttu-id="d0578-109">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="d0578-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0578-110">備註</span><span class="sxs-lookup"><span data-stu-id="d0578-110">Remarks</span></span>

<span data-ttu-id="d0578-111">從 CD 或 DVD 播放媒體時，這個屬性會設定為 "" (空白字串) 。</span><span class="sxs-lookup"><span data-stu-id="d0578-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="d0578-112">範例</span><span class="sxs-lookup"><span data-stu-id="d0578-112">Examples</span></span>

<span data-ttu-id="d0578-113">下列 JScript 範例會使用 *網路*。**sourceProtocol** ，以顯示用來接收資料的來源通訊協定。</span><span class="sxs-lookup"><span data-stu-id="d0578-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="d0578-114">這項資訊會顯示在以 ID = "SP" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="d0578-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="d0578-115">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="d0578-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="d0578-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0578-116">Requirements</span></span>



| <span data-ttu-id="d0578-117">需求</span><span class="sxs-lookup"><span data-stu-id="d0578-117">Requirement</span></span> | <span data-ttu-id="d0578-118">值</span><span class="sxs-lookup"><span data-stu-id="d0578-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d0578-119">版本</span><span class="sxs-lookup"><span data-stu-id="d0578-119">Version</span></span><br/> | <span data-ttu-id="d0578-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="d0578-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d0578-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d0578-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d0578-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0578-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0578-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0578-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0578-124">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="d0578-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





