---
title: IMsRdpClipboard CanSyncLocalClipboardToRemoteSession 方法
description: 指出本機剪貼簿是否可以同步到遠端會話。
ms.tgt_platform: multiple
keywords:
- CanSyncLocalClipboardToRemoteSession 方法遠端桌面服務
- CanSyncLocalClipboardToRemoteSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，CanSyncLocalClipboardToRemoteSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncLocalClipboardToRemoteSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d2dd6fa5fc4d442d7cc22f036c293ebfaba841b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106973933"
---
# <a name="imsrdpclipboardcansynclocalclipboardtoremotesession-method"></a><span data-ttu-id="513c0-106">IMsRdpClipboard：： CanSyncLocalClipboardToRemoteSession 方法</span><span class="sxs-lookup"><span data-stu-id="513c0-106">IMsRdpClipboard::CanSyncLocalClipboardToRemoteSession method</span></span>

<span data-ttu-id="513c0-107">指出本機剪貼簿是否可以同步到遠端會話。</span><span class="sxs-lookup"><span data-stu-id="513c0-107">Indicates whether the local Clipboard can be synced to the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="513c0-108">語法</span><span class="sxs-lookup"><span data-stu-id="513c0-108">Syntax</span></span>

```C++
HRESULT CanSyncLocalClipboardToRemoteSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="513c0-109">參數</span><span class="sxs-lookup"><span data-stu-id="513c0-109">Parameters</span></span>

<span data-ttu-id="513c0-110">如果本機剪貼簿可以同步到遠端會話，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="513c0-110">**TRUE** if the local Clipboard can be synced to the remote session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="513c0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="513c0-111">Return value</span></span>

<span data-ttu-id="513c0-112">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="513c0-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="513c0-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="513c0-113">Requirements</span></span>

| <span data-ttu-id="513c0-114">需求</span><span class="sxs-lookup"><span data-stu-id="513c0-114">Requirement</span></span> | <span data-ttu-id="513c0-115">值</span><span class="sxs-lookup"><span data-stu-id="513c0-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="513c0-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="513c0-116">Minimum supported client</span></span>| <span data-ttu-id="513c0-117">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="513c0-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="513c0-118">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="513c0-118">Type library</span></span>            | <span data-ttu-id="513c0-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="513c0-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="513c0-120">DLL</span><span class="sxs-lookup"><span data-stu-id="513c0-120">DLL</span></span>                  | <span data-ttu-id="513c0-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="513c0-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="513c0-122">IID</span><span class="sxs-lookup"><span data-stu-id="513c0-122">IID</span></span>                      | <span data-ttu-id="513c0-123">IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="513c0-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="513c0-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="513c0-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="513c0-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="513c0-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>