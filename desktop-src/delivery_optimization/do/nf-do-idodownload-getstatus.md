---
title: IDODownload：： GetStatus 方法
description: 抓取 **DO_DOWNLOAD_STATUS** 結構的指標，此結構會反映下載的目前狀態。
keywords:
- IDODownload：： GetStatus 方法
topic_type:
- apiref
api_name:
- IDODownload.GetStatus
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 8b9b2603354bbb5345cf866ee0c94785a254952d
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104374023"
---
# <a name="idodownloadgetstatus-method"></a><span data-ttu-id="e7740-104">IDODownload：： GetStatus 方法</span><span class="sxs-lookup"><span data-stu-id="e7740-104">IDODownload::GetStatus method</span></span>

<span data-ttu-id="e7740-105">抓取 **DO_DOWNLOAD_STATUS** 結構的指標，此結構會反映下載的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="e7740-105">Retrieves a pointer to a **DO_DOWNLOAD_STATUS** structure that reflects the current status of the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7740-106">語法</span><span class="sxs-lookup"><span data-stu-id="e7740-106">Syntax</span></span>

```cpp
HRESULT GetStatus(
  DO_DOWNLOAD_STATUS *status
);
```

## <a name="parameters"></a><span data-ttu-id="e7740-107">參數</span><span class="sxs-lookup"><span data-stu-id="e7740-107">Parameters</span></span>

`status`

<span data-ttu-id="e7740-108">**DO_DOWNLOAD_STATUS** 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="e7740-108">A pointer to a **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="return-value"></a><span data-ttu-id="e7740-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="e7740-109">Return Value</span></span>

<span data-ttu-id="e7740-110">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="e7740-110">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="e7740-111">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="e7740-111">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="e7740-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7740-112">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="e7740-113">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="e7740-113">**Minimum supported client**</span></span> | <span data-ttu-id="e7740-114">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7740-114">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e7740-115">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="e7740-115">**Minimum supported server**</span></span> | <span data-ttu-id="e7740-116">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7740-116">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="e7740-117">**標頭**</span><span class="sxs-lookup"><span data-stu-id="e7740-117">**Header**</span></span> | <span data-ttu-id="e7740-118">Do。h</span><span class="sxs-lookup"><span data-stu-id="e7740-118">Do.h</span></span> |
