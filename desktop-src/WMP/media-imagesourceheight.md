---
title: ImageSourceHeight
description: ImageSourceHeight 屬性會抓取目前媒體專案的高度（以圖元為單位）。
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- ImageSourceHeight Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978404"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="6b426-104">ImageSourceHeight</span><span class="sxs-lookup"><span data-stu-id="6b426-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="6b426-105">**ImageSourceHeight** 屬性會抓取目前媒體專案的高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6b426-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b426-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b426-106">Syntax</span></span>

<span data-ttu-id="6b426-107">*玩家*。*currentMedia*。**imageSourceHeight**</span><span class="sxs-lookup"><span data-stu-id="6b426-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="6b426-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="6b426-108">Possible Values</span></span>

<span data-ttu-id="6b426-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="6b426-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="6b426-110">備註</span><span class="sxs-lookup"><span data-stu-id="6b426-110">Remarks</span></span>

<span data-ttu-id="6b426-111">如果媒體專案不是目前的，則這個屬性會傳回零。</span><span class="sxs-lookup"><span data-stu-id="6b426-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="6b426-112">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="6b426-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="6b426-113">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="6b426-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6b426-114">範例</span><span class="sxs-lookup"><span data-stu-id="6b426-114">Examples</span></span>

<span data-ttu-id="6b426-115">下列 JScript 範例 *會使用 imageSourceHeight* 來顯示目前媒體專案的影像大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="6b426-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="6b426-116">這項資訊會列印到名為 VideoSize 的 HTML TEXTAREA 元素。</span><span class="sxs-lookup"><span data-stu-id="6b426-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="6b426-117">使用 ID = "player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="6b426-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="6b426-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b426-118">Requirements</span></span>



| <span data-ttu-id="6b426-119">需求</span><span class="sxs-lookup"><span data-stu-id="6b426-119">Requirement</span></span> | <span data-ttu-id="6b426-120">值</span><span class="sxs-lookup"><span data-stu-id="6b426-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6b426-121">版本</span><span class="sxs-lookup"><span data-stu-id="6b426-121">Version</span></span><br/> | <span data-ttu-id="6b426-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6b426-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6b426-123">DLL</span><span class="sxs-lookup"><span data-stu-id="6b426-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="6b426-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b426-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b426-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b426-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b426-126">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="6b426-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="6b426-127">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="6b426-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="6b426-128">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6b426-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="6b426-129">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6b426-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





