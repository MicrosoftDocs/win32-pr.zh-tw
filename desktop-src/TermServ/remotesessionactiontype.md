---
title: RemoteSessionActionType 列舉
description: 用來指定遠端動作的類型。
ms.assetid: C0DA0FA2-6FE0-4B40-B169-4592A1BE2AD6
ms.tgt_platform: multiple
keywords:
- RemoteSessionActionType 列舉遠端桌面服務
topic_type:
- apiref
api_name:
- RemoteSessionActionType
api_location:
- MsTscAx.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 291bb9fdd2cadfef3881bc27a47f9fc1bb1bce68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967324"
---
# <a name="remotesessionactiontype-enumeration"></a><span data-ttu-id="f5bb2-104">RemoteSessionActionType 列舉</span><span class="sxs-lookup"><span data-stu-id="f5bb2-104">RemoteSessionActionType enumeration</span></span>

<span data-ttu-id="f5bb2-105">用來指定遠端動作的類型。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-105">Used to specify the type of remote action.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5bb2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5bb2-106">Syntax</span></span>


```C++
typedef enum _RemoteSessionActionType { 
  RemoteSessionActionCharms        = 0,
  RemoteSessionActionAppbar        = 1,
  RemoteSessionActionSnap          = 2,
  RemoteSessionActionStartScreen   = 3,
  RemoteSessionActionAppSwitch     = 4,
  RemoteSessionActionActionCenter  = 4
} RemoteSessionActionType;
```



## <a name="constants"></a><span data-ttu-id="f5bb2-107">常數</span><span class="sxs-lookup"><span data-stu-id="f5bb2-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f5bb2-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-108"><span id="RemoteSessionActionCharms"></span><span id="remotesessionactioncharms"></span><span id="REMOTESESSIONACTIONCHARMS"></span>**RemoteSessionActionCharms**</span></span>
</dt> <dd>

<span data-ttu-id="f5bb2-109">顯示遠端會話中的常用鍵。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-109">Displays the charms in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb2-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-110"><span id="RemoteSessionActionAppbar"></span><span id="remotesessionactionappbar"></span><span id="REMOTESESSIONACTIONAPPBAR"></span>**RemoteSessionActionAppbar**</span></span>
</dt> <dd>

<span data-ttu-id="f5bb2-111">在遠端會話中顯示應用程式行。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-111">Displays the app bar in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb2-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-112"><span id="RemoteSessionActionSnap"></span><span id="remotesessionactionsnap"></span><span id="REMOTESESSIONACTIONSNAP"></span>**RemoteSessionActionSnap**</span></span>
</dt> <dd>

<span data-ttu-id="f5bb2-113">將應用程式停駐在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-113">Docks the application in the remote session.</span></span> <span data-ttu-id="f5bb2-114">此選項已被取代，不應該使用。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-114">This option has been deprecated and should not be used.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb2-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-115"><span id="RemoteSessionActionStartScreen"></span><span id="remotesessionactionstartscreen"></span><span id="REMOTESESSIONACTIONSTARTSCREEN"></span>**RemoteSessionActionStartScreen**</span></span>
</dt> <dd>

<span data-ttu-id="f5bb2-116">使開始畫面顯示在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-116">Causes the start screen to be displayed in the remote session.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb2-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-117"><span id="RemoteSessionActionAppSwitch"></span><span id="remotesessionactionappswitch"></span><span id="REMOTESESSIONACTIONAPPSWITCH"></span>**RemoteSessionActionAppSwitch**</span></span>
</dt> <dd>

<span data-ttu-id="f5bb2-118">使應用程式切換視窗顯示在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-118">Causes the application switch window to be displayed in the remote session.</span></span> <span data-ttu-id="f5bb2-119">這與按下 Alt + Tab 鍵的使用者相同。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-119">This is the same as the user pressing Alt+Tab.</span></span>

</dd> <dt>

<span data-ttu-id="f5bb2-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-120"><span id="RemoteSessionActionActionCenter"></span><span id="remotesessionactionactioncenter"></span><span id="REMOTESESSIONACTIONACTIONCENTER"></span>**RemoteSessionActionActionCenter**</span></span>
</dt> <dd>

<span data-ttu-id="f5bb2-121">使動作中心顯示在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-121">Causes the Action Center to be displayed in the remote session.</span></span> <span data-ttu-id="f5bb2-122">這與按下 Win + A 的使用者相同。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-122">This is the same as the user pressing Win+A.</span></span>

<span data-ttu-id="f5bb2-123">**Windows server 2012 R2、Windows 8.1、Windows server 2012 和 Windows 8：** 在 Windows Server 2016 和 Windows 10 之前，不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="f5bb2-123">**Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:** This value is not supported before Windows Server 2016 and Windows 10.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f5bb2-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5bb2-124">Requirements</span></span>



| <span data-ttu-id="f5bb2-125">需求</span><span class="sxs-lookup"><span data-stu-id="f5bb2-125">Requirement</span></span> | <span data-ttu-id="f5bb2-126">值</span><span class="sxs-lookup"><span data-stu-id="f5bb2-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5bb2-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5bb2-127">Minimum supported client</span></span><br/> | <span data-ttu-id="f5bb2-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f5bb2-128">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="f5bb2-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5bb2-129">Minimum supported server</span></span><br/> | <span data-ttu-id="f5bb2-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f5bb2-130">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="f5bb2-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f5bb2-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="f5bb2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5bb2-132"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5bb2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5bb2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5bb2-134">**IMsRdpClient8::SendRemoteAction**</span><span class="sxs-lookup"><span data-stu-id="f5bb2-134">**IMsRdpClient8::SendRemoteAction**</span></span>](imsrdpclient8-sendremoteaction.md)
</dt> </dl>

 

 





