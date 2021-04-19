---
title: SourceURL
description: SourceURL 屬性會抓取媒體專案的 URL。
ms.assetid: 98ff6ed4-ad3d-44f8-893d-f016e5217ce5
keywords:
- SourceURL Windows Media Player
topic_type:
- apiref
api_name:
- Media.sourceURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c32d594cd1c3b590001eedfd09e9a8c8eb21240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984770"
---
# <a name="mediasourceurl"></a><span data-ttu-id="f45bc-104">SourceURL</span><span class="sxs-lookup"><span data-stu-id="f45bc-104">Media.sourceURL</span></span>

<span data-ttu-id="f45bc-105">**SourceURL** 屬性會抓取媒體專案的 URL。</span><span class="sxs-lookup"><span data-stu-id="f45bc-105">The **sourceURL** property retrieves the URL of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="f45bc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f45bc-106">Syntax</span></span>

<span data-ttu-id="f45bc-107">*玩家*。*currentMedia*. sourceURL</span><span class="sxs-lookup"><span data-stu-id="f45bc-107">*player*.*currentMedia*.sourceURL</span></span>

## <a name="possible-values"></a><span data-ttu-id="f45bc-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="f45bc-108">Possible Values</span></span>

<span data-ttu-id="f45bc-109">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="f45bc-109">This property is a read-only **String**.</span></span>

## <a name="examples"></a><span data-ttu-id="f45bc-110">範例</span><span class="sxs-lookup"><span data-stu-id="f45bc-110">Examples</span></span>

<span data-ttu-id="f45bc-111">下列 JScript 範例會使用 *媒體*。**sourceURL** 以取得範例播放清單中第一個媒體專案的 URL;媒體專案的 URL 接著會指派給 player 物件 **url** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f45bc-111">The following JScript example uses *Media*.**sourceURL** to retrieve the URL of the first media item in the sample playlist; the URL of the media item is then assigned to the player object **URL** property.</span></span> <span data-ttu-id="f45bc-112">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="f45bc-112">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the sample playlist object in a variable. 
var pl = Player.playlistCollection.getByName("Sample Playlist").item(0);

// Store the first media item from the sample playlist.
var media = pl.item(0);

// Change the URL property of the player to the URL of the media item.
Player.URL = media.sourceURL;

// Play the media item.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="f45bc-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f45bc-113">Requirements</span></span>



| <span data-ttu-id="f45bc-114">需求</span><span class="sxs-lookup"><span data-stu-id="f45bc-114">Requirement</span></span> | <span data-ttu-id="f45bc-115">值</span><span class="sxs-lookup"><span data-stu-id="f45bc-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f45bc-116">版本</span><span class="sxs-lookup"><span data-stu-id="f45bc-116">Version</span></span><br/> | <span data-ttu-id="f45bc-117">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f45bc-117">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f45bc-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f45bc-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f45bc-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f45bc-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f45bc-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f45bc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f45bc-121">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="f45bc-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





