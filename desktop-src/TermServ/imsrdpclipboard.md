---
title: IMsRdpClipboard 介面
description: 代表在啟用手動剪貼簿同步處理的情況下，用來同步處理本機和遠端寫字板的剪貼簿控制器。
ms.tgt_platform: multiple
keywords:
- IMsRdpClipboard 介面遠端桌面服務
- IMsRdpClipboard 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClipboard
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 1baa65264226d5c4bd1e32acbe0666545e79b7a0
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108368"
---
# <a name="imsrdpclipboard-interface"></a><span data-ttu-id="5797d-105">IMsRdpClipboard 介面</span><span class="sxs-lookup"><span data-stu-id="5797d-105">IMsRdpClipboard interface</span></span>

<span data-ttu-id="5797d-106">代表在啟用手動剪貼簿同步處理的情況下，用來同步處理本機和遠端寫字板的剪貼簿控制器 (也就是說， [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) 屬性值設定為 **True**) 。</span><span class="sxs-lookup"><span data-stu-id="5797d-106">Represents the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled (that is, the [ManualClipboardSyncEnabled](imsrdpextendedsettings-property.md) property value is set to **True**).</span></span>

## <a name="members"></a><span data-ttu-id="5797d-107">成員</span><span class="sxs-lookup"><span data-stu-id="5797d-107">Members</span></span>

<span data-ttu-id="5797d-108">**IMsRdpClipboard** 介面繼承自 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="5797d-108">The **IMsRdpClipboard** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="5797d-109">**IMsRdpClipboard** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="5797d-109">**IMsRdpClipboard** also has these types of members:</span></span>

- [<span data-ttu-id="5797d-110">方法</span><span class="sxs-lookup"><span data-stu-id="5797d-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5797d-111">方法</span><span class="sxs-lookup"><span data-stu-id="5797d-111">Methods</span></span>

<span data-ttu-id="5797d-112">**IMsRdpClipboard** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="5797d-112">The **IMsRdpClipboard** interface has these methods.</span></span>


| <span data-ttu-id="5797d-113">方法</span><span class="sxs-lookup"><span data-stu-id="5797d-113">Method</span></span>        | <span data-ttu-id="5797d-114">描述</span><span class="sxs-lookup"><span data-stu-id="5797d-114">Description</span></span>      |
|:---------------|:----------------|
| [<span data-ttu-id="5797d-115">**CanSyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="5797d-115">**CanSyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-cansynclocalclipboardtoremotesession.md)       |  <span data-ttu-id="5797d-116">指出本機剪貼簿是否可以同步到遠端會話。</span><span class="sxs-lookup"><span data-stu-id="5797d-116">Indicates whether the local Clipboard can be synced to the remote session.</span></span>                   |
| [<span data-ttu-id="5797d-117">**CanSyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="5797d-117">**CanSyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-cansyncremoteclipboardtolocalsession.md)       |  <span data-ttu-id="5797d-118">指出遠端剪貼簿是否可同步處理至本機會話。</span><span class="sxs-lookup"><span data-stu-id="5797d-118">Indicates whether the remote Clipboard can be synced to the local session.</span></span>                   |
| [<span data-ttu-id="5797d-119">**SyncLocalClipboardToRemoteSession**</span><span class="sxs-lookup"><span data-stu-id="5797d-119">**SyncLocalClipboardToRemoteSession**</span></span>](imsrdpclipboard-synclocalclipboardtoremotesession.md)       |  <span data-ttu-id="5797d-120">將本機剪貼簿同步到遠端會話。</span><span class="sxs-lookup"><span data-stu-id="5797d-120">Syncs the local Clipboard to the remote session.</span></span>                   |
| [<span data-ttu-id="5797d-121">**SyncRemoteClipboardToLocalSession**</span><span class="sxs-lookup"><span data-stu-id="5797d-121">**SyncRemoteClipboardToLocalSession**</span></span>](imsrdpclipboard-syncremoteclipboardtolocalsession.md)       |   <span data-ttu-id="5797d-122">將遠端剪貼簿同步處理至本機會話。</span><span class="sxs-lookup"><span data-stu-id="5797d-122">Syncs the remote Clipboard to the local session.</span></span>                      |

## <a name="requirements"></a><span data-ttu-id="5797d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5797d-123">Requirements</span></span>

| <span data-ttu-id="5797d-124">需求</span><span class="sxs-lookup"><span data-stu-id="5797d-124">Requirement</span></span> | <span data-ttu-id="5797d-125">值</span><span class="sxs-lookup"><span data-stu-id="5797d-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="5797d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5797d-126">Minimum supported client</span></span>| <span data-ttu-id="5797d-127">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="5797d-127">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="5797d-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5797d-128">Type library</span></span>            | <span data-ttu-id="5797d-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="5797d-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="5797d-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5797d-130">DLL</span></span>                  | <span data-ttu-id="5797d-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="5797d-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="5797d-132">IID</span><span class="sxs-lookup"><span data-stu-id="5797d-132">IID</span></span>                      | <span data-ttu-id="5797d-133">IID \_ IMsRdpClipboard 定義為2E769EE8-00C7-43DC-AFD9-235D75B72A40</span><span class="sxs-lookup"><span data-stu-id="5797d-133">IID\_IMsRdpClipboard is defined as 2E769EE8-00C7-43DC-AFD9-235D75B72A40</span></span>            |

## <a name="see-also"></a><span data-ttu-id="5797d-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5797d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5797d-135">**IMsRdpClientNonScriptable7：：剪貼簿**</span><span class="sxs-lookup"><span data-stu-id="5797d-135">**IMsRdpClientNonScriptable7::Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)
</dt> </dl>
