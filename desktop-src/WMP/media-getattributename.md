---
title: GetAttributeName 方法
description: GetAttributeName 方法會抓取對應于指定索引之屬性的名稱。
ms.assetid: f74d81c6-49f8-4b1e-a367-acb4a0914c5a
keywords:
- getAttributeName 方法 Windows Media Player
- getAttributeName 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getAttributeName 方法
topic_type:
- apiref
api_name:
- Media.getAttributeName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7134b68837a7a5d1b765c64320ae68c56c6fc56
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992152"
---
# <a name="mediagetattributename-method"></a><span data-ttu-id="b4380-106">GetAttributeName 方法</span><span class="sxs-lookup"><span data-stu-id="b4380-106">Media.getAttributeName method</span></span>

<span data-ttu-id="b4380-107">**GetAttributeName** 方法會抓取對應于指定索引之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="b4380-107">The **getAttributeName** method retrieves the name of the attribute corresponding to the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4380-108">語法</span><span class="sxs-lookup"><span data-stu-id="b4380-108">Syntax</span></span>


```JScript
strRetVal = Media.getAttributeName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="b4380-109">參數</span><span class="sxs-lookup"><span data-stu-id="b4380-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4380-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b4380-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4380-111">包含屬性索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="b4380-111">**Number** (**long**) containing the index of the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4380-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b4380-112">Return value</span></span>

<span data-ttu-id="b4380-113">這個方法會傳回指定屬性名稱的 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="b4380-113">This method returns a **String** specifying the name of the attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4380-114">備註</span><span class="sxs-lookup"><span data-stu-id="b4380-114">Remarks</span></span>

<span data-ttu-id="b4380-115">傳回的屬性名稱可以與 **getItemInfo** 搭配使用，以抓取特定命名屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b4380-115">The attribute name returned can be used in conjunction with **getItemInfo** to retrieve the value for a specific named attribute.</span></span>

<span data-ttu-id="b4380-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b4380-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b4380-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b4380-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b4380-118">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b4380-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="b4380-119">**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。</span><span class="sxs-lookup"><span data-stu-id="b4380-119">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="examples"></a><span data-ttu-id="b4380-120">範例</span><span class="sxs-lookup"><span data-stu-id="b4380-120">Examples</span></span>

<span data-ttu-id="b4380-121">下列 JScript 範例會使用 *媒體*。**getAttributeName** 使用目前媒體專案的每個屬性的索引和名稱，填滿名為 MYTEXT 的 HTML 文字區域。</span><span class="sxs-lookup"><span data-stu-id="b4380-121">The following JScript example uses *Media*.**getAttributeName** to fill an HTML text area named myText with the index and name of each attribute for the current media item.</span></span> <span data-ttu-id="b4380-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="b4380-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media object.
var cm = Player.currentMedia;

// Get the number of attributes for the current media. 
var atCount = cm.attributeCount;

// Loop through the attribute list.
for(var i=0; i < atCount; i++){
   
   // Print each attribute index and name.   
   myText.value += "Attribute " + i +": ";
   myText.value += cm.getAttributeName(i);
   myText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="b4380-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4380-123">Requirements</span></span>



| <span data-ttu-id="b4380-124">需求</span><span class="sxs-lookup"><span data-stu-id="b4380-124">Requirement</span></span> | <span data-ttu-id="b4380-125">值</span><span class="sxs-lookup"><span data-stu-id="b4380-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4380-126">版本</span><span class="sxs-lookup"><span data-stu-id="b4380-126">Version</span></span><br/> | <span data-ttu-id="b4380-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b4380-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b4380-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b4380-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="b4380-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4380-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4380-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4380-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4380-131">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="b4380-131">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b4380-132">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="b4380-132">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b4380-133">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b4380-133">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b4380-134">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b4380-134">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b4380-135">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b4380-135">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





