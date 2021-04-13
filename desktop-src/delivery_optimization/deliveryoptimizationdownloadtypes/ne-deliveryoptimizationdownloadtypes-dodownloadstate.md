---
title: DODownloadState 列舉
description: 指定目前下載狀態的識別碼，這是 **DO_DOWNLOAD_STATUS** 結構的一部分。
keywords:
- DODownloadState 列舉，DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509087"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="cec0d-104">DODownloadState 列舉</span><span class="sxs-lookup"><span data-stu-id="cec0d-104">DODownloadState enumeration</span></span>

<span data-ttu-id="cec0d-105">**DODownloadState** 列舉會指定目前下載狀態的識別碼，這是 **DO_DOWNLOAD_STATUS** 結構的一部分。</span><span class="sxs-lookup"><span data-stu-id="cec0d-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec0d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cec0d-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="cec0d-107">常數</span><span class="sxs-lookup"><span data-stu-id="cec0d-107">Constants</span></span>

| <span data-ttu-id="cec0d-108">需求</span><span class="sxs-lookup"><span data-stu-id="cec0d-108">Requirement</span></span> | <span data-ttu-id="cec0d-109">值</span><span class="sxs-lookup"><span data-stu-id="cec0d-109">Value</span></span> |
|-|-|
| <span data-ttu-id="cec0d-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="cec0d-110">DODownloadState_Created</span></span> | <span data-ttu-id="cec0d-111">已建立下載物件，但尚未啟動。</span><span class="sxs-lookup"><span data-stu-id="cec0d-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="cec0d-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="cec0d-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="cec0d-113">下載正在進行中。</span><span class="sxs-lookup"><span data-stu-id="cec0d-113">Download is in progress.</span></span> |
| <span data-ttu-id="cec0d-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="cec0d-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="cec0d-115">下載已傳送，而且可以藉由下載檔案的另一部分來重新開機。</span><span class="sxs-lookup"><span data-stu-id="cec0d-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="cec0d-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="cec0d-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="cec0d-117">下載已完成，無法再次啟動。</span><span class="sxs-lookup"><span data-stu-id="cec0d-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="cec0d-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="cec0d-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="cec0d-119">下載已中止。</span><span class="sxs-lookup"><span data-stu-id="cec0d-119">Download was aborted.</span></span> |
| <span data-ttu-id="cec0d-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="cec0d-120">DODownloadState_Paused</span></span> | <span data-ttu-id="cec0d-121">下載已隨選暫停，或因為暫時性錯誤而暫停。</span><span class="sxs-lookup"><span data-stu-id="cec0d-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="cec0d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec0d-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cec0d-123">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="cec0d-123">**Minimum supported client**</span></span> | <span data-ttu-id="cec0d-124">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec0d-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cec0d-125">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="cec0d-125">**Minimum supported server**</span></span> | <span data-ttu-id="cec0d-126">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec0d-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="cec0d-127">**標頭**</span><span class="sxs-lookup"><span data-stu-id="cec0d-127">**Header**</span></span> | <span data-ttu-id="cec0d-128">DeliveryOptimizationDownloadTypes。h</span><span class="sxs-lookup"><span data-stu-id="cec0d-128">DeliveryOptimizationDownloadTypes.h</span></span> |
