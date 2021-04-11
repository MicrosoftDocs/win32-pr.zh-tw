---
title: IDODownloadStatusCallback：： OnStatusChange 方法
description: 只要下載狀態變更，就會呼叫此方法的執行。
keywords:
- IDODownloadStatusCallback：： OnStatusChange 方法
topic_type:
- apiref
api_name:
- IDODownloadStatusCallback.OnStatusChange
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 9abf13969a6183f98102792b9bcf7a3329ca243d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104022880"
---
# <a name="idodownloadstatuscallbackonstatuschange-method"></a><span data-ttu-id="6bb79-104">IDODownloadStatusCallback：： OnStatusChange 方法</span><span class="sxs-lookup"><span data-stu-id="6bb79-104">IDODownloadStatusCallback::OnStatusChange method</span></span>

<span data-ttu-id="6bb79-105">只要下載狀態變更，就會呼叫此方法的執行。</span><span class="sxs-lookup"><span data-stu-id="6bb79-105">DO calls your implementation of this method any time a download status has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb79-106">語法</span><span class="sxs-lookup"><span data-stu-id="6bb79-106">Syntax</span></span>

```cpp
HRESULT OnStatusChange(
  IDODownload *download,
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="6bb79-107">參數</span><span class="sxs-lookup"><span data-stu-id="6bb79-107">Parameters</span></span>

`download`

<span data-ttu-id="6bb79-108">**IDODownload** 介面的指標，其狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="6bb79-108">An pointer to the **IDODownload** interface whose status changed.</span></span>

`status`

<span data-ttu-id="6bb79-109">**DO_DOWNLOAD_STATUS** 結構的指標，其中包含下載的狀態。</span><span class="sxs-lookup"><span data-stu-id="6bb79-109">A pointer to a **DO_DOWNLOAD_STATUS** structure containing the download's status.</span></span>

## <a name="return-value"></a><span data-ttu-id="6bb79-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="6bb79-110">Return Value</span></span>

<span data-ttu-id="6bb79-111">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="6bb79-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="6bb79-112">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="6bb79-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb79-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6bb79-113">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6bb79-114">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="6bb79-114">**Minimum supported client**</span></span> | <span data-ttu-id="6bb79-115">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-115">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6bb79-116">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="6bb79-116">**Minimum supported server**</span></span> | <span data-ttu-id="6bb79-117">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6bb79-117">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6bb79-118">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6bb79-118">**Header**</span></span> | <span data-ttu-id="6bb79-119">Do。h</span><span class="sxs-lookup"><span data-stu-id="6bb79-119">Do.h</span></span> |
