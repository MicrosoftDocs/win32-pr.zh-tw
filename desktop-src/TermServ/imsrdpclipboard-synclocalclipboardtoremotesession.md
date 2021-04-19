---
title: IMsRdpClipboard SyncLocalClipboardToRemoteSession 方法
description: 將本機剪貼簿同步到遠端會話。
ms.tgt_platform: multiple
keywords:
- SyncLocalClipboardToRemoteSession 方法遠端桌面服務
- SyncLocalClipboardToRemoteSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，SyncLocalClipboardToRemoteSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 55e407b86a34cf08d356676181d3225b4a5a768c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106973122"
---
# <a name="imsrdpclipboardsynclocalclipboardtoremotesession-method"></a><span data-ttu-id="e2a1f-106">IMsRdpClipboard：： SyncLocalClipboardToRemoteSession 方法</span><span class="sxs-lookup"><span data-stu-id="e2a1f-106">IMsRdpClipboard::SyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="e2a1f-107">將本機剪貼簿同步到遠端會話。</span><span class="sxs-lookup"><span data-stu-id="e2a1f-107">Syncs the local Clipboard to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2a1f-108">語法</span><span class="sxs-lookup"><span data-stu-id="e2a1f-108">Syntax</span></span>

```C++
HRESULT SyncLocalClipboardToRemoteSession();
```

## <a name="parameters"></a><span data-ttu-id="e2a1f-109">參數</span><span class="sxs-lookup"><span data-stu-id="e2a1f-109">Parameters</span></span>

<span data-ttu-id="e2a1f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e2a1f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e2a1f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2a1f-111">Return value</span></span>

<span data-ttu-id="e2a1f-112">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e2a1f-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2a1f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2a1f-113">Requirements</span></span>

| <span data-ttu-id="e2a1f-114">需求</span><span class="sxs-lookup"><span data-stu-id="e2a1f-114">Requirement</span></span> | <span data-ttu-id="e2a1f-115">值</span><span class="sxs-lookup"><span data-stu-id="e2a1f-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e2a1f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2a1f-116">Minimum supported client</span></span>| <span data-ttu-id="e2a1f-117">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="e2a1f-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e2a1f-118">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e2a1f-118">Type library</span></span>            | <span data-ttu-id="e2a1f-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e2a1f-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e2a1f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e2a1f-120">DLL</span></span>                  | <span data-ttu-id="e2a1f-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e2a1f-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e2a1f-122">IID</span><span class="sxs-lookup"><span data-stu-id="e2a1f-122">IID</span></span>                      | <span data-ttu-id="e2a1f-123">IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="e2a1f-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="e2a1f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2a1f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a1f-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="e2a1f-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>
