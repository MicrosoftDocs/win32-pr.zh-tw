---
title: SetItemInfo 方法
description: SetItemInfo 方法會為目前的媒體專案設定指定之屬性的值。
ms.assetid: 8c4ce954-45cb-4a67-9660-1a013ecd64c3
keywords:
- setItemInfo 方法 Windows Media Player
- setItemInfo 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，setItemInfo 方法
topic_type:
- apiref
api_name:
- Media.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b918e6a388cab750cc379611f5f55c6a1b1d256c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999422"
---
# <a name="mediasetiteminfo-method"></a><span data-ttu-id="de3a5-106">SetItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="de3a5-106">Media.setItemInfo method</span></span>

<span data-ttu-id="de3a5-107">**SetItemInfo** 方法會為目前的媒體專案設定指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="de3a5-107">The **setItemInfo** method sets the value of the specified attribute for the current media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="de3a5-108">語法</span><span class="sxs-lookup"><span data-stu-id="de3a5-108">Syntax</span></span>


```JScript
Media.setItemInfo(
  attribute,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="de3a5-109">參數</span><span class="sxs-lookup"><span data-stu-id="de3a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de3a5-110">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de3a5-110">*attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3a5-111">包含屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="de3a5-111">**String** containing the attribute name.</span></span> <span data-ttu-id="de3a5-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="de3a5-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="de3a5-113">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="de3a5-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="de3a5-114">包含新值的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="de3a5-114">**String** containing the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de3a5-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="de3a5-115">Return value</span></span>

<span data-ttu-id="de3a5-116">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="de3a5-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de3a5-117">備註</span><span class="sxs-lookup"><span data-stu-id="de3a5-117">Remarks</span></span>

<span data-ttu-id="de3a5-118">**AttributeCount** 屬性包含指定 **媒體** 物件可用的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="de3a5-118">The **attributeCount** property contains the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="de3a5-119">然後，您可以搭配 **getAttributeName** 方法使用索引編號來判斷可搭配此方法使用的內建屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="de3a5-119">Index numbers can then be used with the **getAttributeName** method to determine the names of the built-in attributes that can be used with this method.</span></span>

<span data-ttu-id="de3a5-120">使用這個方法之前，請使用 **isReadOnlyItem** 方法來判斷是否可以設定特定屬性。</span><span class="sxs-lookup"><span data-stu-id="de3a5-120">Before using this method, use the **isReadOnlyItem** method to determine whether a particular attribute can be set.</span></span>

<span data-ttu-id="de3a5-121">若要使用此方法，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="de3a5-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="de3a5-122">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="de3a5-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="de3a5-123">**注意**</span><span class="sxs-lookup"><span data-stu-id="de3a5-123">**Note**</span></span>

<span data-ttu-id="de3a5-124">如果您在應用程式中內嵌 Windows Media Player 控制項，您所變更的檔案屬性將不會寫入數位媒體檔案，直到使用者執行 Windows Media Player 為止。</span><span class="sxs-lookup"><span data-stu-id="de3a5-124">If you embed the Windows Media Player control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="de3a5-125">如果您在以 c + + 撰寫的遠端應用程式中使用控制項，則在進行變更之後，將會立即將您變更的檔案屬性寫入數位媒體檔案。</span><span class="sxs-lookup"><span data-stu-id="de3a5-125">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="de3a5-126">無論是哪一種情況，您的程式碼都可以透過程式庫立即取得變更。</span><span class="sxs-lookup"><span data-stu-id="de3a5-126">In either case, the changes are immediately available to your code through the library.</span></span>

<span data-ttu-id="de3a5-127">**Windows Media Player 10** 行動裝置版：這個方法不會實作為。</span><span class="sxs-lookup"><span data-stu-id="de3a5-127">**Windows Media Player 10 Mobile:** This method is not implemented.</span></span>

## <a name="examples"></a><span data-ttu-id="de3a5-128">範例</span><span class="sxs-lookup"><span data-stu-id="de3a5-128">Examples</span></span>

<span data-ttu-id="de3a5-129">下列 JScript 範例會使用 *媒體*。**setItemInfo** ，以變更目前媒體專案的 [內容類型] 屬性值。</span><span class="sxs-lookup"><span data-stu-id="de3a5-129">The following JScript example uses *Media*.**setItemInfo** to change the value of the Genre attribute for the current media item.</span></span> <span data-ttu-id="de3a5-130">名為 GeNtext.c 就會的 HTML 文字輸入元素可讓使用者輸入文字字串，然後用它來變更屬性資訊。</span><span class="sxs-lookup"><span data-stu-id="de3a5-130">An HTML TEXT input element named genText allows the user to enter a text string, which is then used to change the attribute information.</span></span> <span data-ttu-id="de3a5-131">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="de3a5-131">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the button element. -->
<INPUT type = "BUTTON"  id = "NEWGEN"  name = "NEWGEN"  value = "Change Genre" 
onClick = "
    /* Store the current media item. */
    var cm = Player.currentMedia;

    /* Get the user input from the text box. */
    var atValue = genText.value;

    /* Test for read-only status of the attribute. */
    if(cm.isReadOnlyItem('Genre') == false){

        /* Change the attribute value. */
        cm.setItemInfo('Genre' ,atValue);
    } 
">

```



## <a name="requirements"></a><span data-ttu-id="de3a5-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="de3a5-132">Requirements</span></span>



| <span data-ttu-id="de3a5-133">需求</span><span class="sxs-lookup"><span data-stu-id="de3a5-133">Requirement</span></span> | <span data-ttu-id="de3a5-134">值</span><span class="sxs-lookup"><span data-stu-id="de3a5-134">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="de3a5-135">版本</span><span class="sxs-lookup"><span data-stu-id="de3a5-135">Version</span></span><br/> | <span data-ttu-id="de3a5-136">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="de3a5-136">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="de3a5-137">DLL</span><span class="sxs-lookup"><span data-stu-id="de3a5-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="de3a5-138"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de3a5-138"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3a5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="de3a5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3a5-140">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="de3a5-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="de3a5-141">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="de3a5-141">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="de3a5-142">**IsReadOnlyItem**</span><span class="sxs-lookup"><span data-stu-id="de3a5-142">**Media.isReadOnlyItem**</span></span>](media-isreadonlyitem.md)
</dt> <dt>

[<span data-ttu-id="de3a5-143">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="de3a5-143">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="de3a5-144">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="de3a5-144">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





