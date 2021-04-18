---
title: DriveSpecifier
description: DriveSpecifier 屬性會抓取 CD 或 DVD 光碟機號。
ms.assetid: f592819e-61ba-4ae1-b748-b6f29df88067
keywords:
- DriveSpecifier Windows Media Player
topic_type:
- apiref
api_name:
- Cdrom.driveSpecifier
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fef04f56de87bb6aeb4843e5aedb6e5ed74418a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508404"
---
# <a name="cdromdrivespecifier"></a><span data-ttu-id="26dd9-104">DriveSpecifier</span><span class="sxs-lookup"><span data-stu-id="26dd9-104">Cdrom.driveSpecifier</span></span>

<span data-ttu-id="26dd9-105">**DriveSpecifier** 屬性會抓取 CD 或 DVD 光碟機號。</span><span class="sxs-lookup"><span data-stu-id="26dd9-105">The **driveSpecifier** property retrieves the CD or DVD drive letter.</span></span>

``` syntax
player.cdromCollection.item(
        index
        ).driveSpecifier
      
```

## <a name="possible-values"></a><span data-ttu-id="26dd9-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="26dd9-106">Possible Values</span></span>

<span data-ttu-id="26dd9-107">這個屬性是唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="26dd9-107">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="26dd9-108">備註</span><span class="sxs-lookup"><span data-stu-id="26dd9-108">Remarks</span></span>

<span data-ttu-id="26dd9-109">DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。</span><span class="sxs-lookup"><span data-stu-id="26dd9-109">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span> <span data-ttu-id="26dd9-110">這個屬性會在使用 *CdromCollection* 抓取的範圍內，針對以零為基礎的磁片磁碟機索引抓取磁片磁碟機規範。**計數**。</span><span class="sxs-lookup"><span data-stu-id="26dd9-110">This property retrieves a drive specifier for a zero-based drive index within the range retrieved using *CdromCollection*.**count**.</span></span> <span data-ttu-id="26dd9-111">抓取的值採用 *x*：形式，其中 *X* 代表磁碟機號。</span><span class="sxs-lookup"><span data-stu-id="26dd9-111">The value retrieved takes the form *X*:, where *X* represents the drive letter.</span></span>

<span data-ttu-id="26dd9-112">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="26dd9-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="26dd9-113">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="26dd9-113">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="26dd9-114">**Windows Media Player 10** 行動裝置版：不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="26dd9-114">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="26dd9-115">範例</span><span class="sxs-lookup"><span data-stu-id="26dd9-115">Examples</span></span>

<span data-ttu-id="26dd9-116">下列 JScript 範例會使用 *光碟*。**driveSpecifier** 以逗號分隔的可用 CD 和 DVD 光碟機清單來填滿名為 MYTEXT 的 HTML 文字區域。</span><span class="sxs-lookup"><span data-stu-id="26dd9-116">The following JScript example uses *Cdrom*.**driveSpecifier** to fill an HTML text area named myText with a comma-separated list of available CD and DVD drives.</span></span> <span data-ttu-id="26dd9-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="26dd9-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Allocate an array to store the drive specifiers.
var MYdriveSpecifiers = new Array();

// Loop through the available drives using CdromCollection.count.
for (var i = 0; i < Player.cdRomCollection.count; i++){

// For each available drive, add a corresponding item 
// to the MYdriveSpecifiers array. 
    MYdriveSpecifiers[i] = Player.CDRomCollection.item(i).driveSpecifier;
}

// Write the array of drive letter specifiers to the text area.
myText.value = "Drive letters found: " + MYdriveSpecifiers;
```



## <a name="requirements"></a><span data-ttu-id="26dd9-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="26dd9-118">Requirements</span></span>



| <span data-ttu-id="26dd9-119">需求</span><span class="sxs-lookup"><span data-stu-id="26dd9-119">Requirement</span></span> | <span data-ttu-id="26dd9-120">值</span><span class="sxs-lookup"><span data-stu-id="26dd9-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="26dd9-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26dd9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26dd9-122">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26dd9-122">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="26dd9-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26dd9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26dd9-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26dd9-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="26dd9-125">版本</span><span class="sxs-lookup"><span data-stu-id="26dd9-125">Version</span></span><br/>                  | <span data-ttu-id="26dd9-126">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="26dd9-126">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="26dd9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26dd9-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26dd9-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26dd9-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26dd9-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26dd9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26dd9-130">**Cdrom 物件**</span><span class="sxs-lookup"><span data-stu-id="26dd9-130">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="26dd9-131">**CdromCollection 計數**</span><span class="sxs-lookup"><span data-stu-id="26dd9-131">**CdromCollection.count**</span></span>](cdromcollection-count.md)
</dt> <dt>

[<span data-ttu-id="26dd9-132">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="26dd9-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="26dd9-133">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="26dd9-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





