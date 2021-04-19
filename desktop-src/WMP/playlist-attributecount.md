---
title: 播放清單。 attributeCount
description: AttributeCount 屬性會捕獲與播放清單相關聯的屬性數目。
ms.assetid: 92063131-0118-4458-9122-0539628a9821
keywords:
- 播放清單. attributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Playlist.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e42d72e029f232bb6dabc074b412406a1bb64c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000414"
---
# <a name="playlistattributecount"></a><span data-ttu-id="5286b-104">播放清單。 attributeCount</span><span class="sxs-lookup"><span data-stu-id="5286b-104">Playlist.attributeCount</span></span>

<span data-ttu-id="5286b-105">**AttributeCount** 屬性會捕獲與播放清單相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="5286b-105">The **attributeCount** property retrieves the number of attributes associated with the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="5286b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5286b-106">Syntax</span></span>

<span data-ttu-id="5286b-107">*玩家*。*currentPlaylist*。**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="5286b-107">*player*.*currentPlaylist*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5286b-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="5286b-108">Possible Values</span></span>

<span data-ttu-id="5286b-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="5286b-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5286b-110">備註</span><span class="sxs-lookup"><span data-stu-id="5286b-110">Remarks</span></span>

<span data-ttu-id="5286b-111">由於播放清單可以來自許多不同的來源，因此可以有數個不同的屬性集。</span><span class="sxs-lookup"><span data-stu-id="5286b-111">Because playlists can come from many different sources, they can have several different sets of properties.</span></span> <span data-ttu-id="5286b-112">這個方法會抓取可用屬性的總數，讓 **播放清單** 物件的其他方法可以存取它們。</span><span class="sxs-lookup"><span data-stu-id="5286b-112">This method retrieves the total number of properties available so that the other methods of the **Playlist** object can access them.</span></span>

<span data-ttu-id="5286b-113">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="5286b-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5286b-114">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="5286b-114">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="5286b-115">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="5286b-115">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5286b-116">範例</span><span class="sxs-lookup"><span data-stu-id="5286b-116">Examples</span></span>

<span data-ttu-id="5286b-117">下列 JScript 範例說明如何使用 **播放清單** 和 **媒體** 物件的各種屬性和方法。</span><span class="sxs-lookup"><span data-stu-id="5286b-117">The following JScript example illustrates how various properties and methods of the **Playlist** and **Media** objects are used.</span></span>


```JScript
function onLoad() {
    var display;
    var pl = player.currentPlaylist;

    pl.setItemInfo("custom playlist attribute", "changed");
    pl.item(0).setItemInfo("new custom attribute", "5");

    display = pl.attributeCount + " Playlist Attributes:\r\r";

    for (var i = 0; i < pl.attributeCount; ++i) {
        display = display + pl.attributeName(i) + ": ";
        display = display + pl.getItemInfo(pl.attributeName(i)) + "\r";
    }

    for (var j = 0; j < pl.count; ++j) {
        display = display + "\rTrack " + j + "\r"
        display = display + pl.item(j).attributeCount + " Attributes:\r\r";

        for (var k = 0; k < pl.item(j).attributeCount; ++k) {
            var it = pl.item(j);  // Media object
            display = display + it.getAttributeName(k) + ": ";
            display = display + it.getItemInfo(it.getAttributeName(k)) + "\r";
        }
    }

    myText.value = display;
}

```



## <a name="requirements"></a><span data-ttu-id="5286b-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="5286b-118">Requirements</span></span>



| <span data-ttu-id="5286b-119">需求</span><span class="sxs-lookup"><span data-stu-id="5286b-119">Requirement</span></span> | <span data-ttu-id="5286b-120">值</span><span class="sxs-lookup"><span data-stu-id="5286b-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5286b-121">版本</span><span class="sxs-lookup"><span data-stu-id="5286b-121">Version</span></span><br/> | <span data-ttu-id="5286b-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5286b-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5286b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5286b-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="5286b-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5286b-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5286b-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5286b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5286b-126">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="5286b-126">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5286b-127">**播放清單。 attributeName**</span><span class="sxs-lookup"><span data-stu-id="5286b-127">**Playlist.attributeName**</span></span>](playlist-attributename.md)
</dt> <dt>

[<span data-ttu-id="5286b-128">**播放清單。 getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="5286b-128">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="5286b-129">**播放清單。 setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="5286b-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="5286b-130">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5286b-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5286b-131">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5286b-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





