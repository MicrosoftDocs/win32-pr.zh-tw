---
title: MediaCollection 方法
description: Remove 方法會從媒體集合中移除專案。
ms.assetid: 7d4c03ed-01c8-4112-90b6-5de52eacb199
keywords:
- 移除方法 Windows Media Player
- remove 方法 Windows Media Player，MediaCollection 類別
- MediaCollection 類別 Windows Media Player，remove 方法
topic_type:
- apiref
api_name:
- MediaCollection.remove
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6667a5b95920ac63f38d3a581e6f8e05bdf8d233
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997655"
---
# <a name="mediacollectionremove-method"></a><span data-ttu-id="c3adf-106">MediaCollection 方法</span><span class="sxs-lookup"><span data-stu-id="c3adf-106">MediaCollection.remove method</span></span>

<span data-ttu-id="c3adf-107">**Remove** 方法會從媒體集合中移除專案。</span><span class="sxs-lookup"><span data-stu-id="c3adf-107">The **remove** method removes an item from the media collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3adf-108">語法</span><span class="sxs-lookup"><span data-stu-id="c3adf-108">Syntax</span></span>


```JScript
MediaCollection.remove(
  item,
  delete
)
```



## <a name="parameters"></a><span data-ttu-id="c3adf-109">參數</span><span class="sxs-lookup"><span data-stu-id="c3adf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3adf-110">*專案* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3adf-110">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3adf-111">要移除的 **媒體** 物件。</span><span class="sxs-lookup"><span data-stu-id="c3adf-111">**Media** object to be removed.</span></span>

</dd> <dt>

<span data-ttu-id="c3adf-112">*刪除* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3adf-112">*delete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3adf-113">指出是否要移除專案的 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="c3adf-113">**Boolean** indicating whether to remove the item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3adf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3adf-114">Return value</span></span>

<span data-ttu-id="c3adf-115">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c3adf-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3adf-116">備註</span><span class="sxs-lookup"><span data-stu-id="c3adf-116">Remarks</span></span>

<span data-ttu-id="c3adf-117">這個方法會從程式庫中刪除專案。</span><span class="sxs-lookup"><span data-stu-id="c3adf-117">This method deletes an item from the library.</span></span> <span data-ttu-id="c3adf-118">這個方法不會刪除使用者電腦中的檔案。</span><span class="sxs-lookup"><span data-stu-id="c3adf-118">This method does not delete files from the user's computer.</span></span>

<span data-ttu-id="c3adf-119">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="c3adf-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="c3adf-120">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="c3adf-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c3adf-121">範例</span><span class="sxs-lookup"><span data-stu-id="c3adf-121">Examples</span></span>

<span data-ttu-id="c3adf-122">下列 JScript 範例在提示使用者之後，會使用 *MediaCollection* 永久刪除媒體集合中的第一個媒體專案。**移除**。</span><span class="sxs-lookup"><span data-stu-id="c3adf-122">The following JScript example, after prompting the user, permanently deletes the first media item in the media collection by using *MediaCollection*.**remove**.</span></span> <span data-ttu-id="c3adf-123">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c3adf-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first item from the media collection.
var mediaObject = Player.mediaCollection.getAll().item(0);

// Store the name of the retrieved object.
var mediaName = mediaObject.name;

// Prompt the user for permission to delete the object.
var answer = confirm("OK to permanently delete " + mediaName + "?");

// Check the user response.
if (answer){

    // Permanently delete the item.
    Player.mediaCollection.remove(mediaObject, true);

    // Report that the item was deleted.
    alert("Deleted item " + mediaName);
}

```



## <a name="requirements"></a><span data-ttu-id="c3adf-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3adf-124">Requirements</span></span>



| <span data-ttu-id="c3adf-125">需求</span><span class="sxs-lookup"><span data-stu-id="c3adf-125">Requirement</span></span> | <span data-ttu-id="c3adf-126">值</span><span class="sxs-lookup"><span data-stu-id="c3adf-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c3adf-127">版本</span><span class="sxs-lookup"><span data-stu-id="c3adf-127">Version</span></span><br/> | <span data-ttu-id="c3adf-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c3adf-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c3adf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="c3adf-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="c3adf-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3adf-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3adf-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3adf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3adf-132">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="c3adf-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="c3adf-133">**MediaCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="c3adf-133">**MediaCollection Object**</span></span>](mediacollection-object.md)
</dt> <dt>

[<span data-ttu-id="c3adf-134">**MediaCollection 新增**</span><span class="sxs-lookup"><span data-stu-id="c3adf-134">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="c3adf-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c3adf-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c3adf-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c3adf-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





