---
title: IsReadOnlyItem 方法
description: IsReadOnlyItem 方法會傳回值，指出是否可以編輯媒體專案的指定屬性。
ms.assetid: 5e398e76-f64a-45b5-9b4f-679c65e5a0d1
keywords:
- isReadOnlyItem 方法 Windows Media Player
- isReadOnlyItem 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，isReadOnlyItem 方法
topic_type:
- apiref
api_name:
- Media.isReadOnlyItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0ac5bb8d445c3ba6418be4ee5c0c5e7a96f507d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997437"
---
# <a name="mediaisreadonlyitem-method"></a><span data-ttu-id="7a18c-106">IsReadOnlyItem 方法</span><span class="sxs-lookup"><span data-stu-id="7a18c-106">Media.isReadOnlyItem method</span></span>

<span data-ttu-id="7a18c-107">**IsReadOnlyItem** 方法會傳回值，指出是否可以編輯媒體專案的指定屬性。</span><span class="sxs-lookup"><span data-stu-id="7a18c-107">The **isReadOnlyItem** method returns a value indicating whether the specified attribute of the media item can be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a18c-108">語法</span><span class="sxs-lookup"><span data-stu-id="7a18c-108">Syntax</span></span>


```JScript
bRetVal = Media.isReadOnlyItem(
  attribute
)
```



## <a name="parameters"></a><span data-ttu-id="7a18c-109">參數</span><span class="sxs-lookup"><span data-stu-id="7a18c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a18c-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a18c-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a18c-111">表示要測試之屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="7a18c-111">**String** indicating the name of the attribute to test.</span></span> <span data-ttu-id="7a18c-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="7a18c-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a18c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7a18c-113">Return value</span></span>

<span data-ttu-id="7a18c-114">這個方法會傳回 **布林值**。</span><span class="sxs-lookup"><span data-stu-id="7a18c-114">This method returns a **Boolean**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a18c-115">備註</span><span class="sxs-lookup"><span data-stu-id="7a18c-115">Remarks</span></span>

<span data-ttu-id="7a18c-116">如果屬性是唯讀的，則無法使用 **setItemInfo** 方法來設定它。</span><span class="sxs-lookup"><span data-stu-id="7a18c-116">If an attribute is read-only, then it cannot be set with the **setItemInfo** method.</span></span> <span data-ttu-id="7a18c-117">請注意，使用不同版本的 Windows Media Player 時，這個方法可能會針對特定屬性傳回不同的值。</span><span class="sxs-lookup"><span data-stu-id="7a18c-117">Note that this method may return different values for a particular attribute when used with different versions of Windows Media Player.</span></span>

<span data-ttu-id="7a18c-118">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="7a18c-118">To use this method, read access to the library is required.</span></span> <span data-ttu-id="7a18c-119">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="7a18c-119">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="7a18c-120">**Windows Media Player 10** 行動裝置版：這個屬性一律會傳回 **true**。</span><span class="sxs-lookup"><span data-stu-id="7a18c-120">**Windows Media Player 10 Mobile:** This property always returns **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="7a18c-121">範例</span><span class="sxs-lookup"><span data-stu-id="7a18c-121">Examples</span></span>

<span data-ttu-id="7a18c-122">下列 JScript 範例會使用 *媒體*。**isReadOnlyItem** ，以目前媒體專案的相關資訊填入名為 RWTEXT 的 HTML TEXTAREA 元素。</span><span class="sxs-lookup"><span data-stu-id="7a18c-122">The following JScript example uses *Media*.**isReadOnlyItem** to fill an HTML TEXTAREA element named rwText with information about the current media item.</span></span> <span data-ttu-id="7a18c-123">程式碼會輸出目前媒體專案的每個屬性，以及指出屬性為唯讀還是讀取/寫入的文字。</span><span class="sxs-lookup"><span data-stu-id="7a18c-123">The code outputs each attribute of the current media item, along with text indicating whether the attribute is read-only or read/write.</span></span> <span data-ttu-id="7a18c-124">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="7a18c-124">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Store the current media item object.
var cm = Player.currentMedia;

// Create a variable to hold each attribute name.
var atName;

// Loop through the attribute list.
for(var i = 0; i < cm.attributeCount; i++){

   // Get the attribute name.
   atName = cm.getAttributeName(i);

   // Test whether the attribute is read-only.
   var test = ((cm.isReadOnlyItem(atName))?"Read-Only":"Read/Write");

// Print the attribute information to the text area.
   rwText.value += atName + " is " + test;
   rwText.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="7a18c-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a18c-125">Requirements</span></span>



| <span data-ttu-id="7a18c-126">需求</span><span class="sxs-lookup"><span data-stu-id="7a18c-126">Requirement</span></span> | <span data-ttu-id="7a18c-127">值</span><span class="sxs-lookup"><span data-stu-id="7a18c-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a18c-128">版本</span><span class="sxs-lookup"><span data-stu-id="7a18c-128">Version</span></span><br/> | <span data-ttu-id="7a18c-129">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="7a18c-129">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7a18c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="7a18c-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="7a18c-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a18c-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a18c-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a18c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a18c-133">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="7a18c-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="7a18c-134">**SetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="7a18c-134">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="7a18c-135">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7a18c-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="7a18c-136">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="7a18c-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





