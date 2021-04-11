---
title: IDODownload 介面
description: 用來啟動及管理下載。
keywords:
- IDODownload 介面
topic_type:
- apiref
api_name:
- IDODownload
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: ec2f74ce7daae6f612297d21e15e6993fcd78382
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315262"
---
# <a name="idodownload-interface"></a><span data-ttu-id="6c7df-104">IDODownload 介面</span><span class="sxs-lookup"><span data-stu-id="6c7df-104">IDODownload interface</span></span>

<span data-ttu-id="6c7df-105">**IDODownload** 介面可用來啟動及管理下載。</span><span class="sxs-lookup"><span data-stu-id="6c7df-105">The **IDODownload** interface is used to start and manage a download.</span></span>

## <a name="methods"></a><span data-ttu-id="6c7df-106">方法</span><span class="sxs-lookup"><span data-stu-id="6c7df-106">Methods</span></span>

<span data-ttu-id="6c7df-107">**IDODownload** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6c7df-107">The **IDODownload** interface has these methods.</span></span>

| <span data-ttu-id="6c7df-108">方法</span><span class="sxs-lookup"><span data-stu-id="6c7df-108">Method</span></span> | <span data-ttu-id="6c7df-109">描述</span><span class="sxs-lookup"><span data-stu-id="6c7df-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="6c7df-110">IDODownload：： Abort</span><span class="sxs-lookup"><span data-stu-id="6c7df-110">IDODownload::Abort</span></span>](./nf-do-idomanager-createdownload.md) | <span data-ttu-id="6c7df-111">中止下載。</span><span class="sxs-lookup"><span data-stu-id="6c7df-111">Aborts the download.</span></span> |
| [<span data-ttu-id="6c7df-112">IDODownload：： Finalize</span><span class="sxs-lookup"><span data-stu-id="6c7df-112">IDODownload::Finalize</span></span>](./nf-do-idodownload-finalize.md) | <span data-ttu-id="6c7df-113">完成下載。</span><span class="sxs-lookup"><span data-stu-id="6c7df-113">Finalizes the download.</span></span> |
| [<span data-ttu-id="6c7df-114">IDODownload：： GetProperty</span><span class="sxs-lookup"><span data-stu-id="6c7df-114">IDODownload::GetProperty</span></span>](./nf-do-idodownload-getproperty.md) | <span data-ttu-id="6c7df-115">抓取包含特定下載屬性之 **變數** 的指標。</span><span class="sxs-lookup"><span data-stu-id="6c7df-115">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span> |
| [<span data-ttu-id="6c7df-116">IDODownload：： GetStatus</span><span class="sxs-lookup"><span data-stu-id="6c7df-116">IDODownload::GetStatus</span></span>](./nf-do-idodownload-getstatus.md) | <span data-ttu-id="6c7df-117">抓取 **DO_DOWNLOAD_STATUS** 結構的指標，此結構會反映下載的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="6c7df-117">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span> |
| [<span data-ttu-id="6c7df-118">IDODownload：:P ause</span><span class="sxs-lookup"><span data-stu-id="6c7df-118">IDODownload::Pause</span></span>](./nf-do-idodownload-pause.md) | <span data-ttu-id="6c7df-119">暫停下載。</span><span class="sxs-lookup"><span data-stu-id="6c7df-119">Pauses the download.</span></span> |
| [<span data-ttu-id="6c7df-120">IDODownload：： SetProperty</span><span class="sxs-lookup"><span data-stu-id="6c7df-120">IDODownload::SetProperty</span></span>](./nf-do-idodownload-setproperty.md) | <span data-ttu-id="6c7df-121">設定下載屬性。</span><span class="sxs-lookup"><span data-stu-id="6c7df-121">Sets a download property.</span></span> |
| [<span data-ttu-id="6c7df-122">IDODownload：： Start</span><span class="sxs-lookup"><span data-stu-id="6c7df-122">IDODownload::Start</span></span>](./nf-do-idodownload-start.md) | <span data-ttu-id="6c7df-123">啟動或繼續進行下載。</span><span class="sxs-lookup"><span data-stu-id="6c7df-123">Starts or resumes a download.</span></span> |

## <a name="requirements"></a><span data-ttu-id="6c7df-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c7df-124">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6c7df-125">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="6c7df-125">**Minimum supported client**</span></span> | <span data-ttu-id="6c7df-126">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c7df-126">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6c7df-127">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="6c7df-127">**Minimum supported server**</span></span> | <span data-ttu-id="6c7df-128">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c7df-128">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6c7df-129">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6c7df-129">**Header**</span></span> | <span data-ttu-id="6c7df-130">Do。h</span><span class="sxs-lookup"><span data-stu-id="6c7df-130">Do.h</span></span> |