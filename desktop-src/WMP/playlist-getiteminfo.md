---
title: GetItemInfo 方法
description: GetItemInfo 方法會捕獲播放清單屬性的值。
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- getItemInfo 方法 Windows Media Player
- getItemInfo 方法 Windows Media Player，播放清單類別
- 播放清單類別 Windows Media Player，getItemInfo 方法
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976558"
---
# <a name="playlistgetiteminfo-method"></a><span data-ttu-id="5872e-106">GetItemInfo 方法</span><span class="sxs-lookup"><span data-stu-id="5872e-106">Playlist.getItemInfo method</span></span>

<span data-ttu-id="5872e-107">**GetItemInfo** 方法會捕獲播放清單屬性的值。</span><span class="sxs-lookup"><span data-stu-id="5872e-107">The **getItemInfo** method retrieves the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="5872e-108">語法</span><span class="sxs-lookup"><span data-stu-id="5872e-108">Syntax</span></span>


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="5872e-109">參數</span><span class="sxs-lookup"><span data-stu-id="5872e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5872e-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5872e-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5872e-111">包含要抓取的屬性名稱的 **字串**。</span><span class="sxs-lookup"><span data-stu-id="5872e-111">**String** containing the name of the attribute to be retrieved.</span></span> <span data-ttu-id="5872e-112">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="5872e-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5872e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5872e-113">Return value</span></span>

<span data-ttu-id="5872e-114">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="5872e-114">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5872e-115">備註</span><span class="sxs-lookup"><span data-stu-id="5872e-115">Remarks</span></span>

<span data-ttu-id="5872e-116">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="5872e-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5872e-117">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="5872e-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5872e-118">範例</span><span class="sxs-lookup"><span data-stu-id="5872e-118">Examples</span></span>

<span data-ttu-id="5872e-119">如需使用這個屬性的範例程式碼，請參閱 [attributeCount](playlist-attributecount.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="5872e-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5872e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="5872e-120">Requirements</span></span>



| <span data-ttu-id="5872e-121">需求</span><span class="sxs-lookup"><span data-stu-id="5872e-121">Requirement</span></span> | <span data-ttu-id="5872e-122">值</span><span class="sxs-lookup"><span data-stu-id="5872e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5872e-123">版本</span><span class="sxs-lookup"><span data-stu-id="5872e-123">Version</span></span><br/> | <span data-ttu-id="5872e-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="5872e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5872e-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5872e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="5872e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5872e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5872e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5872e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5872e-128">**播放清單物件**</span><span class="sxs-lookup"><span data-stu-id="5872e-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="5872e-129">**播放清單。 setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="5872e-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="5872e-130">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5872e-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5872e-131">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="5872e-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





