---
title: CdromCollection 專案方法
description: Item 方法會在指定的索引處，捕獲 Cdrom 物件。
ms.assetid: c1efa972-736d-4fa0-9835-14ee594ae719
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，CdromCollection 類別
- CdromCollection 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- CdromCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a67dc58ae75819fa42940346b4f588b23a2f645a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995969"
---
# <a name="cdromcollectionitem-method"></a><span data-ttu-id="b7440-106">CdromCollection 專案方法</span><span class="sxs-lookup"><span data-stu-id="b7440-106">CdromCollection.item method</span></span>

<span data-ttu-id="b7440-107">**Item** 方法會在指定的索引處，捕獲 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7440-107">The **item** method retrieves the **Cdrom** object at the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7440-108">語法</span><span class="sxs-lookup"><span data-stu-id="b7440-108">Syntax</span></span>


```JScript
retVal = CdromCollection.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="b7440-109">參數</span><span class="sxs-lookup"><span data-stu-id="b7440-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7440-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b7440-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7440-111">包含索引的 (**長**) **數目**。</span><span class="sxs-lookup"><span data-stu-id="b7440-111">**Number** (**long**) containing the index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7440-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b7440-112">Return value</span></span>

<span data-ttu-id="b7440-113">這個方法會傳回一個 **Cdrom** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7440-113">This method returns a **Cdrom** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7440-114">備註</span><span class="sxs-lookup"><span data-stu-id="b7440-114">Remarks</span></span>

<span data-ttu-id="b7440-115">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b7440-115">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b7440-116">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b7440-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b7440-117">**Windows Media Player 10** 行動裝置版：不支援這個方法。</span><span class="sxs-lookup"><span data-stu-id="b7440-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="b7440-118">範例</span><span class="sxs-lookup"><span data-stu-id="b7440-118">Examples</span></span>

<span data-ttu-id="b7440-119">下列 JScript 範例會使用 *CdromCollection*。用來從電腦上每一張 CD 列印播放清單名稱的 **專案** 。</span><span class="sxs-lookup"><span data-stu-id="b7440-119">The following JScript example uses *CdromCollection*.**item** to print the playlist name from each CD available on the computer.</span></span> <span data-ttu-id="b7440-120">如果磁片磁碟機實際包含 DVD 內容，則需要 Windows XP 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b7440-120">If the drive actually contains DVD content, Windows XP or later is required.</span></span> <span data-ttu-id="b7440-121">使用 ID = "播放清單" 建立的 HTML TextArea 元素。</span><span class="sxs-lookup"><span data-stu-id="b7440-121">An HTML TextArea element was created with ID = "playlists".</span></span> <span data-ttu-id="b7440-122">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="b7440-122">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Create an array to store the CD playlists.
var cdPlaylists = new Array();

// Loop through the available CD drives.
for (var i = 0; i < Player.cdromCollection.count; i++){

     // Fill the cdPlaylists array with playlist objects.
     cdPlaylists[i] = Player.cdromCollection.item(i).Playlist;

     // Print each drive specifier.
     playlists.value+=Player.cdromCollection.item(i).driveSpecifier + " ";

     // Print the name of each CD playlist to the text area.
     playlists.value += cdPlaylists[i].name + "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="b7440-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b7440-123">Requirements</span></span>



| <span data-ttu-id="b7440-124">需求</span><span class="sxs-lookup"><span data-stu-id="b7440-124">Requirement</span></span> | <span data-ttu-id="b7440-125">值</span><span class="sxs-lookup"><span data-stu-id="b7440-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7440-126">版本</span><span class="sxs-lookup"><span data-stu-id="b7440-126">Version</span></span><br/> | <span data-ttu-id="b7440-127">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b7440-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b7440-128">DLL</span><span class="sxs-lookup"><span data-stu-id="b7440-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="b7440-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7440-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7440-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b7440-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7440-131">**DriveSpecifier**</span><span class="sxs-lookup"><span data-stu-id="b7440-131">**Cdrom.driveSpecifier**</span></span>](cdrom-drivespecifier.md)
</dt> <dt>

[<span data-ttu-id="b7440-132">**CdromCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="b7440-132">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="b7440-133">**CdromCollection 計數**</span><span class="sxs-lookup"><span data-stu-id="b7440-133">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="b7440-134">**Playlist.name**</span><span class="sxs-lookup"><span data-stu-id="b7440-134">**Playlist.name**</span></span>](playlist-name.md)
</dt> <dt>

[<span data-ttu-id="b7440-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b7440-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b7440-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b7440-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





