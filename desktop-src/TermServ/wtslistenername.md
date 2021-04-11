---
title: 'WTSLISTENERNAME (Wtsapi32.dll) '
description: 代表遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上遠端桌面服務接聽程式的名稱。
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384953"
---
# <a name="wtslistenername"></a><span data-ttu-id="aa8bc-109">WTSLISTENERNAME</span><span class="sxs-lookup"><span data-stu-id="aa8bc-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="aa8bc-110">代表遠端桌面工作階段主機 (RD 工作階段主機) 伺服器上遠端桌面服務接聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="aa8bc-111">**WTSLISTENERNAMEW**</span><span class="sxs-lookup"><span data-stu-id="aa8bc-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="aa8bc-112">接聽程式的 Unicode 名稱。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="aa8bc-113">**WTSLISTENERNAMEA**</span><span class="sxs-lookup"><span data-stu-id="aa8bc-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="aa8bc-114">接聽程式之 ANSI 名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="aa8bc-115">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="aa8bc-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="aa8bc-116">接聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="aa8bc-117">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="aa8bc-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="aa8bc-118">接聽程式名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="aa8bc-119">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="aa8bc-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="aa8bc-120">接聽程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="aa8bc-121">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="aa8bc-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="aa8bc-122">接聽程式名稱的指標。</span><span class="sxs-lookup"><span data-stu-id="aa8bc-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aa8bc-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="aa8bc-123">Requirements</span></span>



| <span data-ttu-id="aa8bc-124">需求</span><span class="sxs-lookup"><span data-stu-id="aa8bc-124">Requirement</span></span> | <span data-ttu-id="aa8bc-125">值</span><span class="sxs-lookup"><span data-stu-id="aa8bc-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aa8bc-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aa8bc-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aa8bc-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa8bc-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="aa8bc-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aa8bc-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aa8bc-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa8bc-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="aa8bc-130">標頭</span><span class="sxs-lookup"><span data-stu-id="aa8bc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="aa8bc-131"><dt>Wtsapi32.dll。h</dt></span><span class="sxs-lookup"><span data-stu-id="aa8bc-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 





