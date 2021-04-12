---
title: IDODownloadStatusCallback 介面
description: 用來接收有關下載的通知。
keywords:
- IDODownloadStatusCallback 介面
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback
api_location:
- do.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0917b73939535854469a1fe02ea89acc904cf055
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375421"
---
# <a name="idodownloadstatuscallback-interface"></a><span data-ttu-id="58aac-104">IDODownloadStatusCallback 介面</span><span class="sxs-lookup"><span data-stu-id="58aac-104">IDODownloadStatusCallback interface</span></span>

<span data-ttu-id="58aac-105">**IDODownloadStatusCallback** 介面可用來接收有關下載的通知。</span><span class="sxs-lookup"><span data-stu-id="58aac-105">The **IDODownloadStatusCallback** interface is used to receive notifications about a download.</span></span>

## <a name="methods"></a><span data-ttu-id="58aac-106">方法</span><span class="sxs-lookup"><span data-stu-id="58aac-106">Methods</span></span>

<span data-ttu-id="58aac-107">**IDODownloadStatusCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="58aac-107">The **IDODownloadStatusCallback** interface has these methods.</span></span>

| <span data-ttu-id="58aac-108">方法</span><span class="sxs-lookup"><span data-stu-id="58aac-108">Method</span></span> | <span data-ttu-id="58aac-109">描述</span><span class="sxs-lookup"><span data-stu-id="58aac-109">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="58aac-110">IDODownloadStatusCallback::OnStatusChanged</span><span class="sxs-lookup"><span data-stu-id="58aac-110">IDODownloadStatusCallback::OnStatusChanged</span></span>](./nf-do-idodownloadstatuscallback-onstatuschanged.md) | <span data-ttu-id="58aac-111">只要下載狀態變更，就會呼叫此方法的執行。</span><span class="sxs-lookup"><span data-stu-id="58aac-111">DO calls your implementation of this method any time a download status has changed.</span></span> |

## <a name="requirements"></a><span data-ttu-id="58aac-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="58aac-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="58aac-113">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="58aac-113">**Minimum supported client**</span></span> | <span data-ttu-id="58aac-114">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58aac-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="58aac-115">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="58aac-115">**Minimum supported server**</span></span> | <span data-ttu-id="58aac-116">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="58aac-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="58aac-117">**標頭**</span><span class="sxs-lookup"><span data-stu-id="58aac-117">**Header**</span></span> | <span data-ttu-id="58aac-118">Do。h</span><span class="sxs-lookup"><span data-stu-id="58aac-118">Do.h</span></span> |