---
title: Media.name
description: Name 屬性會指定或抓取媒體專案的名稱。
ms.assetid: 68aba78a-86fd-4411-9ac4-58f38d915e2c
keywords:
- Media.name Windows Media Player
topic_type:
- apiref
api_name:
- Media.name
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9de8095d88c3ddec9049e0b43461adcf5553ec74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999365"
---
# <a name="medianame"></a><span data-ttu-id="ce5dc-104">Media.name</span><span class="sxs-lookup"><span data-stu-id="ce5dc-104">Media.name</span></span>

<span data-ttu-id="ce5dc-105">**Name** 屬性會指定或抓取媒體專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-105">The **name** property specifies or retrieves the name of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce5dc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce5dc-106">Syntax</span></span>

<span data-ttu-id="ce5dc-107">*玩家*。*currentMedia*。**名稱**</span><span class="sxs-lookup"><span data-stu-id="ce5dc-107">*player*.*currentMedia*.**name**</span></span>

## <a name="possible-values"></a><span data-ttu-id="ce5dc-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="ce5dc-108">Possible Values</span></span>

<span data-ttu-id="ce5dc-109">這個屬性是包含媒體專案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-109">This property is a read/write **String** containing the name of the media item.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce5dc-110">備註</span><span class="sxs-lookup"><span data-stu-id="ce5dc-110">Remarks</span></span>

<span data-ttu-id="ce5dc-111">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-111">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="ce5dc-112">若要指定此屬性的值，需要有程式庫的完整存取權。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-112">To specify the value of this property, full access to the library is required.</span></span> <span data-ttu-id="ce5dc-113">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="ce5dc-114">使用這個方法來指定媒體專案的名稱之前，請使用 **isReadOnlyItem** 來判斷是否可以設定名稱。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-114">Before using this method to specify the name of a media item, use **isReadOnlyItem** to determine whether the name can be set.</span></span>

<span data-ttu-id="ce5dc-115">**Windows Media Player 10** 行動裝置版：這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-115">**Windows Media Player 10 Mobile:** This property is read-only.</span></span>

## <a name="examples"></a><span data-ttu-id="ce5dc-116">範例</span><span class="sxs-lookup"><span data-stu-id="ce5dc-116">Examples</span></span>

<span data-ttu-id="ce5dc-117">下列 JScript 範例會使用 *媒體*。要變更目前媒體專案名稱的 **名稱** 。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-117">The following JScript example uses *Media*.**name** to change the name of the current media item.</span></span> <span data-ttu-id="ce5dc-118">名為 NameText 的 HTML 文字輸入元素可讓使用者輸入新名稱的文字字串。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-118">An HTML TEXT input element named NameText allows the user to enter a text string for the new name.</span></span> <span data-ttu-id="ce5dc-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an HTML BUTTON element to execute the name change. -->
<INPUT type = "BUTTON"  id = "NewName"  name = "NewName"  value = "Change Name" 
    onClick = "

        /* Store the current media item. */
        var cm = Player.currentMedia;

        /* Change the name. */
        cm.name = NameText.value;
">

```



## <a name="requirements"></a><span data-ttu-id="ce5dc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce5dc-120">Requirements</span></span>



| <span data-ttu-id="ce5dc-121">需求</span><span class="sxs-lookup"><span data-stu-id="ce5dc-121">Requirement</span></span> | <span data-ttu-id="ce5dc-122">值</span><span class="sxs-lookup"><span data-stu-id="ce5dc-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ce5dc-123">版本</span><span class="sxs-lookup"><span data-stu-id="ce5dc-123">Version</span></span><br/> | <span data-ttu-id="ce5dc-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="ce5dc-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="ce5dc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ce5dc-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="ce5dc-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce5dc-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce5dc-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce5dc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce5dc-128">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="ce5dc-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="ce5dc-129">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce5dc-129">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="ce5dc-130">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="ce5dc-130">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





