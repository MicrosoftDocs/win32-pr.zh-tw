---
title: IMsRdpClipboard CanSyncRemoteClipboardToLocalSession 方法
description: 指出遠端剪貼簿是否可同步處理至本機會話。
ms.tgt_platform: multiple
keywords:
- CanSyncRemoteClipboardToLocalSession 方法遠端桌面服務
- CanSyncRemoteClipboardToLocalSession 方法遠端桌面服務，IMsRdpClipboard 介面
- IMsRdpClipboard 介面遠端桌面服務，CanSyncRemoteClipboardToLocalSession 方法
topic_type:
- apiref
api_name:
- IMsRdpClipboard.CanSyncRemoteClipboardToLocalSession
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: ebb20057e3a312dbe0b24856c47ad2a7ef1b7292
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106991580"
---
# <a name="imsrdpclipboardcansyncremoteclipboardtolocalsession-method"></a><span data-ttu-id="44a47-106">IMsRdpClipboard：： CanSyncRemoteClipboardToLocalSession 方法</span><span class="sxs-lookup"><span data-stu-id="44a47-106">IMsRdpClipboard::CanSyncRemoteClipboardToLocalSession method</span></span>

<span data-ttu-id="44a47-107">指出遠端剪貼簿是否可同步處理至本機會話。</span><span class="sxs-lookup"><span data-stu-id="44a47-107">Indicates whether the remote Clipboard can be synced to the local session.</span></span>

## <a name="syntax"></a><span data-ttu-id="44a47-108">語法</span><span class="sxs-lookup"><span data-stu-id="44a47-108">Syntax</span></span>

```C++
HRESULT CanSyncRemoteClipboardToLocalSession(
  [out, retval] VARIANT_BOOL* pfSync
);
```

## <a name="parameters"></a><span data-ttu-id="44a47-109">參數</span><span class="sxs-lookup"><span data-stu-id="44a47-109">Parameters</span></span>

<span data-ttu-id="44a47-110">如果遠端剪貼簿可以同步處理至本機會話，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="44a47-110">**TRUE** if the remote Clipboard can be synced to the local session; otherwise, **FALSE**.</span></span>

## <a name="return-value"></a><span data-ttu-id="44a47-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="44a47-111">Return value</span></span>

<span data-ttu-id="44a47-112">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="44a47-112">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a47-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="44a47-113">Requirements</span></span>

| <span data-ttu-id="44a47-114">需求</span><span class="sxs-lookup"><span data-stu-id="44a47-114">Requirement</span></span> | <span data-ttu-id="44a47-115">值</span><span class="sxs-lookup"><span data-stu-id="44a47-115">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="44a47-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44a47-116">Minimum supported client</span></span>| <span data-ttu-id="44a47-117">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="44a47-117">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="44a47-118">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="44a47-118">Type library</span></span>            | <span data-ttu-id="44a47-119">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="44a47-119">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="44a47-120">DLL</span><span class="sxs-lookup"><span data-stu-id="44a47-120">DLL</span></span>                  | <span data-ttu-id="44a47-121">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="44a47-121">MsTscAx.dll</span></span>     |
| <span data-ttu-id="44a47-122">IID</span><span class="sxs-lookup"><span data-stu-id="44a47-122">IID</span></span>                      | <span data-ttu-id="44a47-123">IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="44a47-123">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>          |

## <a name="see-also"></a><span data-ttu-id="44a47-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44a47-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44a47-125">**IMsRdpClipboard**</span><span class="sxs-lookup"><span data-stu-id="44a47-125">**IMsRdpClipboard**</span></span>](imsrdpclipboard.md)
</dt> </dl>