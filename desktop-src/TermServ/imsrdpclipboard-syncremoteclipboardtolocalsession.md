---
title: IMsRdpClipboard SyncRemoteClipboardToLocalSession 方法
description: 將遠端剪貼簿同步處理至本機會話。
ms.tgt_platform: multiple
keywords:
- SyncRemoteClipboardToLocalSession 方法遠端桌面服務
- SyncRemoteClipboardToLocalSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，SyncRemoteClipboardToLocalSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.SyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d397d7c1ca4407a5125877721be9aa022f8132a7
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104509742"
---
# <a name="imsrdpclipboardsyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="f8ec7-106">IMsRdpClipboard：： SyncRemoteClipboardToLocalSession 方法</span><span class="sxs-lookup"><span data-stu-id="f8ec7-106">IMsRdpClipboard::SyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="f8ec7-107">將遠端剪貼簿同步處理至本機會話。</span><span class="sxs-lookup"><span data-stu-id="f8ec7-107">Syncs the remote Clipboard to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8ec7-108">語法</span><span class="sxs-lookup"><span data-stu-id="f8ec7-108">Syntax</span></span>

```C++
HRESULT SyncRemoteClipboardToLocalSession();
```

## <a name="parameters"></a><span data-ttu-id="f8ec7-109">參數</span><span class="sxs-lookup"><span data-stu-id="f8ec7-109">Parameters</span></span>

<span data-ttu-id="f8ec7-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f8ec7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f8ec7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8ec7-111">Return value</span></span>

<span data-ttu-id="f8ec7-112">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="f8ec7-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ec7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8ec7-113">Requirements</span></span>

| <span data-ttu-id="f8ec7-114">需求</span><span class="sxs-lookup"><span data-stu-id="f8ec7-114">Requirement</span></span> | <span data-ttu-id="f8ec7-115">值</span><span class="sxs-lookup"><span data-stu-id="f8ec7-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f8ec7-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8ec7-116">Minimum supported client</span></span>| <span data-ttu-id="f8ec7-117">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="f8ec7-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f8ec7-118">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f8ec7-118">Type library</span></span>            | <span data-ttu-id="f8ec7-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f8ec7-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f8ec7-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f8ec7-120">DLL</span></span>                  | <span data-ttu-id="f8ec7-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f8ec7-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f8ec7-122">IID</span><span class="sxs-lookup"><span data-stu-id="f8ec7-122">IID</span></span>                      | <span data-ttu-id="f8ec7-123">IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="f8ec7-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f8ec7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8ec7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8ec7-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="f8ec7-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>