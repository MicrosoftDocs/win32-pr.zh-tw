---
title: MediaCollection. getAttributeStringCollection 方法
description: GetAttributeStringCollection 方法會抓取 StringCollection 物件，代表指定之媒體類型內指定之屬性的所有值集。
ms.assetid: 75563a75-88f5-419e-983b-d105bce02511
keywords:
- getAttributeStringCollection 方法 Windows Media Player
- getAttributeStringCollection 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getAttributeStringCollection 方法
topic_type:
- apiref
api_name:
- MediaCollection.getAttributeStringCollection
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d50d25488a05e6076c99802ce738edf02298ade
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984343"
---
# <a name="mediacollectiongetattributestringcollection-method"></a><span data-ttu-id="7dd99-106">MediaCollection. getAttributeStringCollection 方法</span><span class="sxs-lookup"><span data-stu-id="7dd99-106">MediaCollection.getAttributeStringCollection method</span></span>

<span data-ttu-id="7dd99-107">**GetAttributeStringCollection** 方法會抓取 **StringCollection** 物件，代表指定之媒體類型內指定之屬性的所有值集。</span><span class="sxs-lookup"><span data-stu-id="7dd99-107">The **getAttributeStringCollection** method retrieves a **StringCollection** object representing the set of all values for a specified attribute within a specified media type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dd99-108">語法</span><span class="sxs-lookup"><span data-stu-id="7dd99-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getAttributeStringCollection(
  attribute,
  mediaType
)
```



## <a name="parameters"></a><span data-ttu-id="7dd99-109">參數</span><span class="sxs-lookup"><span data-stu-id="7dd99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dd99-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7dd99-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd99-111">指定屬性的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="7dd99-111">**String** specifying the attribute.</span></span>

</dd> <dt>

<span data-ttu-id="7dd99-112">*媒體媒體* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7dd99-112">*mediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dd99-113">代表媒體類型的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="7dd99-113">**String** representing the media type.</span></span> <span data-ttu-id="7dd99-114">包含下列其中一個值：「音訊」、「影片」、「播放清單」或「其他」。</span><span class="sxs-lookup"><span data-stu-id="7dd99-114">Contains one of the following values: "Audio", "Video", "Playlist", or "Other".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dd99-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="7dd99-115">Return value</span></span>

<span data-ttu-id="7dd99-116">這個方法會傳回 **StringCollection** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dd99-116">This method returns a **StringCollection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dd99-117">備註</span><span class="sxs-lookup"><span data-stu-id="7dd99-117">Remarks</span></span>

<span data-ttu-id="7dd99-118">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="7dd99-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7dd99-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="7dd99-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7dd99-120">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 [屬性參考](attribute-reference.md) 一節。</span><span class="sxs-lookup"><span data-stu-id="7dd99-120">For information about the attributes supported by Windows Media Player, see the [Attribute Reference](attribute-reference.md) section.</span></span>

## <a name="examples"></a><span data-ttu-id="7dd99-121">範例</span><span class="sxs-lookup"><span data-stu-id="7dd99-121">Examples</span></span>

<span data-ttu-id="7dd99-122">下列 JScript 範例會使用 *MediaCollection*。**getAttributeStringCollection** 顯示的值清單，會對應至媒體集合中音訊專案的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="7dd99-122">The following JScript example uses *MediaCollection*.**getAttributeStringCollection** to display a list of values that correspond to a particular attribute for audio items in the media collection.</span></span> <span data-ttu-id="7dd99-123">以 ID = "Attribute" 建立的 HTML SELECT 元素，可讓使用者選取屬性，例如演出者、內容類型或專輯。</span><span class="sxs-lookup"><span data-stu-id="7dd99-123">An HTML SELECT element, created with ID = "Attribute", allows the user to select an attribute, such as Artist, Genre, or Album.</span></span> <span data-ttu-id="7dd99-124">以 ID = "AttributeVals" 建立的 HTML TEXTAREA 元素會顯示結果。</span><span class="sxs-lookup"><span data-stu-id="7dd99-124">An HTML TEXTAREA element, created with ID = "AttributeVals", displays the result.</span></span> <span data-ttu-id="7dd99-125">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="7dd99-125">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Clear the text in the display area.
AttributeVals.value = "";

// Store the mediaCollection object.
var library = Player.mediaCollection;

// Get the string collection for the attribute type the user selects.
var all = library.getAttributeStringCollection(Attribute.value, "Audio");

// Loop through the string collection.
for (i = 0; i < all.count; i++){

    // Display the items one line at a time.
    AttributeVals.value += all.item(i);
    AttributeVals.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="7dd99-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="7dd99-126">Requirements</span></span>



| <span data-ttu-id="7dd99-127">需求</span><span class="sxs-lookup"><span data-stu-id="7dd99-127">Requirement</span></span> | <span data-ttu-id="7dd99-128">值</span><span class="sxs-lookup"><span data-stu-id="7dd99-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd99-129">版本</span><span class="sxs-lookup"><span data-stu-id="7dd99-129">Version</span></span><br/> | <span data-ttu-id="7dd99-130">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7dd99-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7dd99-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7dd99-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="7dd99-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dd99-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd99-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7dd99-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd99-134">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="7dd99-134">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="7dd99-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7dd99-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7dd99-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7dd99-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7dd99-137">**StringCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="7dd99-137">**StringCollection Object**</span></span>](stringcollection-object.md)
</dt> </dl>

 

 





