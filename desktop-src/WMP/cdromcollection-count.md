---
title: CdromCollection 計數
description: Count 屬性會抓取系統上的可用 CD 和 DVD 光碟機數目。
ms.assetid: 98d24713-6a55-409f-af9a-fc941ad6d8f5
keywords:
- CdromCollection Windows Media Player 計數
topic_type:
- apiref
api_name:
- CdromCollection.count
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf7150ca31caaf68fa51ae42fded223d24a8e59f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001863"
---
# <a name="cdromcollectioncount"></a><span data-ttu-id="97206-104">CdromCollection 計數</span><span class="sxs-lookup"><span data-stu-id="97206-104">CdromCollection.count</span></span>

<span data-ttu-id="97206-105">**Count** 屬性會抓取系統上的可用 CD 和 DVD 光碟機數目。</span><span class="sxs-lookup"><span data-stu-id="97206-105">The **count** property retrieves the number of available CD and DVD drives on the system.</span></span>

``` syntax
player.cdromCollection.count
      
```

## <a name="possible-values"></a><span data-ttu-id="97206-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="97206-106">Possible Values</span></span>

<span data-ttu-id="97206-107">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="97206-107">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="97206-108">備註</span><span class="sxs-lookup"><span data-stu-id="97206-108">Remarks</span></span>

<span data-ttu-id="97206-109">若要取得這個屬性的值，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="97206-109">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="97206-110">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="97206-110">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="97206-111">DVD-ROM 磁片磁碟機的計算方式與 CD 光碟機完全一樣。</span><span class="sxs-lookup"><span data-stu-id="97206-111">DVD-ROM drives are counted exactly like CD drives.</span></span> <span data-ttu-id="97206-112">不過，Windows Media Player 控制項僅支援 Windows XP 或更新版本作業系統的 DVD 功能。</span><span class="sxs-lookup"><span data-stu-id="97206-112">However, the Windows Media Player control only supports DVD functionality for Windows XP or later operating systems.</span></span> <span data-ttu-id="97206-113">DVD 光碟機通常可以播放 CD 媒體，但 CD 光碟機無法播放 DVD 媒體。</span><span class="sxs-lookup"><span data-stu-id="97206-113">Typically, DVD drives can play CD media, but CD drives cannot play DVD media.</span></span>

<span data-ttu-id="97206-114">**Windows Media Player 10** 行動裝置版：這個方法一律會傳回0。</span><span class="sxs-lookup"><span data-stu-id="97206-114">**Windows Media Player 10 Mobile:** This method always returns 0.</span></span>

## <a name="examples"></a><span data-ttu-id="97206-115">範例</span><span class="sxs-lookup"><span data-stu-id="97206-115">Examples</span></span>

<span data-ttu-id="97206-116">下列 JScript 範例會使用 *CdromCollection*。顯示使用者電腦上可用的 CD 和 DVD 光碟機數目的 **計數** 。</span><span class="sxs-lookup"><span data-stu-id="97206-116">The following JScript example uses *CdromCollection*.**count** to display the number of CD and DVD drives available on the user's computer.</span></span> <span data-ttu-id="97206-117">使用 ID = "Player" 建立 player 物件。</span><span class="sxs-lookup"><span data-stu-id="97206-117">The player object was created with ID = "Player".</span></span>


```JScript
// Store the count of drives found on the computer.
var numCDROMS = Player.cdromCollection.count;

// Build the string to display to the user.
var displayString = numCDROMS + " drive(s) found.";

// Show a message box with the count information.
alert(displayString);
```



## <a name="requirements"></a><span data-ttu-id="97206-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="97206-118">Requirements</span></span>



| <span data-ttu-id="97206-119">需求</span><span class="sxs-lookup"><span data-stu-id="97206-119">Requirement</span></span> | <span data-ttu-id="97206-120">值</span><span class="sxs-lookup"><span data-stu-id="97206-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97206-121">版本</span><span class="sxs-lookup"><span data-stu-id="97206-121">Version</span></span><br/> | <span data-ttu-id="97206-122">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="97206-122">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="97206-123">DLL</span><span class="sxs-lookup"><span data-stu-id="97206-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="97206-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97206-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97206-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97206-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97206-126">**CdromCollection 物件**</span><span class="sxs-lookup"><span data-stu-id="97206-126">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="97206-127">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="97206-127">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="97206-128">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="97206-128">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





