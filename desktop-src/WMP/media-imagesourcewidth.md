---
title: ImageSourceWidth
description: ImageSourceWidth 屬性會抓取目前媒體專案的寬度（以圖元為單位）。
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- ImageSourceWidth Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989882"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="345e2-104">ImageSourceWidth</span><span class="sxs-lookup"><span data-stu-id="345e2-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="345e2-105">**ImageSourceWidth** 屬性會抓取目前媒體專案的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="345e2-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="345e2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="345e2-106">Syntax</span></span>

<span data-ttu-id="345e2-107">*玩家*。*currentMedia*。**imageSourceWidth**</span><span class="sxs-lookup"><span data-stu-id="345e2-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="345e2-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="345e2-108">Possible Values</span></span>

<span data-ttu-id="345e2-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="345e2-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="345e2-110">備註</span><span class="sxs-lookup"><span data-stu-id="345e2-110">Remarks</span></span>

<span data-ttu-id="345e2-111">如果媒體專案不是目前的，則這個屬性會傳回零。</span><span class="sxs-lookup"><span data-stu-id="345e2-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="345e2-112">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="345e2-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="345e2-113">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="345e2-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="345e2-114">範例</span><span class="sxs-lookup"><span data-stu-id="345e2-114">Examples</span></span>

<span data-ttu-id="345e2-115">下列 JScript 範例會使用 *媒體*。**imageSourceWidth** ：顯示目前媒體專案的影像大小（以圖元為單位） **。這項資訊會列印到名為 VideoSize 的 HTML TEXTAREA 元素。** 使用 ID = "player" 建立 player 物件。</span><span class="sxs-lookup"><span data-stu-id="345e2-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="345e2-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="345e2-116">Requirements</span></span>



| <span data-ttu-id="345e2-117">需求</span><span class="sxs-lookup"><span data-stu-id="345e2-117">Requirement</span></span> | <span data-ttu-id="345e2-118">值</span><span class="sxs-lookup"><span data-stu-id="345e2-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="345e2-119">版本</span><span class="sxs-lookup"><span data-stu-id="345e2-119">Version</span></span><br/> | <span data-ttu-id="345e2-120">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="345e2-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="345e2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="345e2-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="345e2-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="345e2-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="345e2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="345e2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="345e2-124">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="345e2-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="345e2-125">**CurrentMedia**</span><span class="sxs-lookup"><span data-stu-id="345e2-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="345e2-126">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="345e2-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="345e2-127">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="345e2-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





