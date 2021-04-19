---
title: MediaCollection. getByAttribute 方法
description: GetByAttribute 方法會抓取媒體專案的播放清單，其中包含指定之屬性的指定值。
ms.assetid: a89f9c52-c655-4420-858e-c0eed661856f
keywords:
- getByAttribute 方法 Windows Media Player
- getByAttribute 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，getByAttribute 方法
topic_type:
- apiref
api_name:
- MediaCollection.getByAttribute
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533823127364416f8f4492c82381e682173c5c78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987863"
---
# <a name="mediacollectiongetbyattribute-method"></a><span data-ttu-id="bb516-106">MediaCollection. getByAttribute 方法</span><span class="sxs-lookup"><span data-stu-id="bb516-106">MediaCollection.getByAttribute method</span></span>

<span data-ttu-id="bb516-107">**GetByAttribute** 方法會抓取媒體專案的播放清單，其中包含指定之屬性的指定值。</span><span class="sxs-lookup"><span data-stu-id="bb516-107">The **getByAttribute** method retrieves a playlist of media items that contain a specified value for a specified attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb516-108">語法</span><span class="sxs-lookup"><span data-stu-id="bb516-108">Syntax</span></span>


```JScript
retVal = MediaCollection.getByAttribute(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="bb516-109">參數</span><span class="sxs-lookup"><span data-stu-id="bb516-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb516-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb516-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb516-111">**字串** ，表示要搜尋的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="bb516-111">**String** indicating the name of the attribute to search.</span></span> <span data-ttu-id="bb516-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="bb516-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="bb516-113">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb516-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb516-114">**字串** ，表示屬性應該具有的值。</span><span class="sxs-lookup"><span data-stu-id="bb516-114">**String** indicating the value that the attribute should have.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb516-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb516-115">Return value</span></span>

<span data-ttu-id="bb516-116">這個方法會傳回 **播放清單** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb516-116">This method returns a **Playlist** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb516-117">備註</span><span class="sxs-lookup"><span data-stu-id="bb516-117">Remarks</span></span>

<span data-ttu-id="bb516-118">這個方法可以用來建立符合資料庫中屬性值之媒體專案的一般查詢。</span><span class="sxs-lookup"><span data-stu-id="bb516-118">This method can be used to create a generic query for media items that match a value for an attribute in the database.</span></span> <span data-ttu-id="bb516-119">在使用者定義的屬性中，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="bb516-119">This is useful in the case of user-defined attributes.</span></span> <span data-ttu-id="bb516-120">如果屬性不存在，則會產生錯誤。</span><span class="sxs-lookup"><span data-stu-id="bb516-120">If the attribute does not exist, an error will result.</span></span>

<span data-ttu-id="bb516-121">您可以使用這個方法來取得特定類型的所有媒體專案。</span><span class="sxs-lookup"><span data-stu-id="bb516-121">You can use this method to retrieve all of the media items of a specific type.</span></span> <span data-ttu-id="bb516-122">使用屬性名稱 "媒體" 和下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="bb516-122">Use the attribute name "MediaType" and one of the following values:</span></span>



| <span data-ttu-id="bb516-123">值</span><span class="sxs-lookup"><span data-stu-id="bb516-123">Value</span></span>    | <span data-ttu-id="bb516-124">描述</span><span class="sxs-lookup"><span data-stu-id="bb516-124">Description</span></span>                                                |
|----------|------------------------------------------------------------|
| <span data-ttu-id="bb516-125">音訊</span><span class="sxs-lookup"><span data-stu-id="bb516-125">audio</span></span>    | <span data-ttu-id="bb516-126">音樂和其他僅限音訊的專案。</span><span class="sxs-lookup"><span data-stu-id="bb516-126">Music and other audio-only items.</span></span>                          |
| <span data-ttu-id="bb516-127">播放清單</span><span class="sxs-lookup"><span data-stu-id="bb516-127">playlist</span></span> | <span data-ttu-id="bb516-128">以 **媒體** 物件表示的播放清單。</span><span class="sxs-lookup"><span data-stu-id="bb516-128">Playlists represented as **Media** objects.</span></span>                |
| <span data-ttu-id="bb516-129">radio</span><span class="sxs-lookup"><span data-stu-id="bb516-129">radio</span></span>    | <span data-ttu-id="bb516-130">無線電站專案。</span><span class="sxs-lookup"><span data-stu-id="bb516-130">Radio station items.</span></span> <span data-ttu-id="bb516-131">Windows Media Player 10 未使用。</span><span class="sxs-lookup"><span data-stu-id="bb516-131">Not used by Windows Media Player 10.</span></span>  |
| <span data-ttu-id="bb516-132">影片</span><span class="sxs-lookup"><span data-stu-id="bb516-132">video</span></span>    | <span data-ttu-id="bb516-133">影片專案。</span><span class="sxs-lookup"><span data-stu-id="bb516-133">Video items.</span></span>                                               |
| <span data-ttu-id="bb516-134">相片</span><span class="sxs-lookup"><span data-stu-id="bb516-134">photo</span></span>    | <span data-ttu-id="bb516-135">相片專案。</span><span class="sxs-lookup"><span data-stu-id="bb516-135">Photo items.</span></span> <span data-ttu-id="bb516-136">需要 Windows Media Player 10。</span><span class="sxs-lookup"><span data-stu-id="bb516-136">Requires Windows Media Player 10.</span></span>             |
| <span data-ttu-id="bb516-137">其他</span><span class="sxs-lookup"><span data-stu-id="bb516-137">other</span></span>    | <span data-ttu-id="bb516-138">其他專案，例如 ASF 檔案或串流媒體的 Url。</span><span class="sxs-lookup"><span data-stu-id="bb516-138">Other items, such as ASF files or URLs to streaming media.</span></span> |



 

<span data-ttu-id="bb516-139">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="bb516-139">To use this method, read access to the library is required.</span></span> <span data-ttu-id="bb516-140">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="bb516-140">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="bb516-141">範例</span><span class="sxs-lookup"><span data-stu-id="bb516-141">Examples</span></span>

<span data-ttu-id="bb516-142">下列 JScript 範例會使用 *MediaCollection*。**getByAttribute** ，以名為 Triode 48 的演出者播放媒體櫃中的所有內容。</span><span class="sxs-lookup"><span data-stu-id="bb516-142">The following JScript example uses *MediaCollection*.**getByAttribute** to play all content from the library by the artist named Triode 48.</span></span> <span data-ttu-id="bb516-143">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="bb516-143">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get a playlist object filled with media items by a 
// particular artist.
var pl = Player.mediaCollection.getByAttribute("Artist", "Triode 48");

// Make the new playlist the current one.
Player.currentPlaylist = pl;

// Start Windows Media Player.
Player.controls.play();

```



## <a name="requirements"></a><span data-ttu-id="bb516-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb516-144">Requirements</span></span>



| <span data-ttu-id="bb516-145">需求</span><span class="sxs-lookup"><span data-stu-id="bb516-145">Requirement</span></span> | <span data-ttu-id="bb516-146">值</span><span class="sxs-lookup"><span data-stu-id="bb516-146">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb516-147">版本</span><span class="sxs-lookup"><span data-stu-id="bb516-147">Version</span></span><br/> | <span data-ttu-id="bb516-148">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="bb516-148">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="bb516-149">DLL</span><span class="sxs-lookup"><span data-stu-id="bb516-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb516-150"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb516-150"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb516-151">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb516-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb516-152">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="bb516-152">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="bb516-153">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="bb516-153">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="bb516-154">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bb516-154">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="bb516-155">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="bb516-155">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





