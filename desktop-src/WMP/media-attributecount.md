---
title: AttributeCount
description: AttributeCount 屬性會抓取可針對媒體專案查詢及/或設定的屬性數目。
ms.assetid: d2a5286f-dde1-48b5-b486-6cee1be463f9
keywords:
- AttributeCount Windows Media Player
topic_type:
- apiref
api_name:
- Media.attributeCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df4979f670cdd6a79b1b309bc3eceff5a2798223
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999458"
---
# <a name="mediaattributecount"></a><span data-ttu-id="3116b-104">AttributeCount</span><span class="sxs-lookup"><span data-stu-id="3116b-104">Media.attributeCount</span></span>

<span data-ttu-id="3116b-105">**AttributeCount** 屬性會抓取可針對媒體專案查詢及/或設定的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="3116b-105">The **attributeCount** property retrieves the number of attributes that can be queried and/or set for the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="3116b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="3116b-106">Syntax</span></span>

<span data-ttu-id="3116b-107">*玩家*。*currentMedia*。**attributeCount**</span><span class="sxs-lookup"><span data-stu-id="3116b-107">*player*.*currentMedia*.**attributeCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="3116b-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="3116b-108">Possible Values</span></span>

<span data-ttu-id="3116b-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="3116b-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="3116b-110">備註</span><span class="sxs-lookup"><span data-stu-id="3116b-110">Remarks</span></span>

<span data-ttu-id="3116b-111">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="3116b-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="3116b-112">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="3116b-112">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3116b-113">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="3116b-113">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="3116b-114">**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。</span><span class="sxs-lookup"><span data-stu-id="3116b-114">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="3116b-115">範例</span><span class="sxs-lookup"><span data-stu-id="3116b-115">Examples</span></span>

<span data-ttu-id="3116b-116">下列 JScript 範例會使用 *媒體*。**attributeCount** ，判斷目前媒體專案中可用的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="3116b-116">The following JScript example uses *Media*.**attributeCount** to determine the number of attributes available in the current media item.</span></span> <span data-ttu-id="3116b-117">程式碼會使用該值來列印 HTML 文字區域中的屬性名稱和值清單，名稱為 myText。</span><span class="sxs-lookup"><span data-stu-id="3116b-117">The code uses that value to print a list of attribute names and values in an HTML text area, named myText.</span></span> <span data-ttu-id="3116b-118">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="3116b-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Create arrays to hold each attribute name and value.
var atNames = new Array();
var atValues = new Array();

// Loop through the attribute list.   
for(var i = 0; i < cm.attributeCount; i++){

   // Fill the arrays with the attribute info.
   atNames[i] = cm.getAttributeName(i);
   atValues[i] = cm.getItemInfo(atNames[i]);

   // Print the attribute information to the text area.
   myText.value += atNames[i] + ": " + atValues[i];
   myText.value += "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3116b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="3116b-119">Requirements</span></span>



| <span data-ttu-id="3116b-120">需求</span><span class="sxs-lookup"><span data-stu-id="3116b-120">Requirement</span></span> | <span data-ttu-id="3116b-121">值</span><span class="sxs-lookup"><span data-stu-id="3116b-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3116b-122">版本</span><span class="sxs-lookup"><span data-stu-id="3116b-122">Version</span></span><br/> | <span data-ttu-id="3116b-123">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="3116b-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="3116b-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3116b-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="3116b-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3116b-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3116b-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3116b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3116b-127">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="3116b-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="3116b-128">**GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="3116b-128">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="3116b-129">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="3116b-129">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="3116b-130">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3116b-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="3116b-131">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="3116b-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





