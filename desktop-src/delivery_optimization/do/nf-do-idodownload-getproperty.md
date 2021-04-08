---
title: IDODownload：： GetProperty 方法
description: 抓取包含特定下載屬性之 **變數** 的指標。
keywords:
- IDODownload：： GetProperty 方法
topic_type:
- apiref
api_name:
- IDODownload.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: e734f109e596663ee699c764ca85f1ee45ad7947
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103841732"
---
# <a name="idodownloadgetproperty-method"></a><span data-ttu-id="96496-104">IDODownload：： GetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="96496-104">IDODownload::GetProperty method</span></span>

<span data-ttu-id="96496-105">抓取包含特定下載屬性之 **變數** 的指標。</span><span class="sxs-lookup"><span data-stu-id="96496-105">Retrieves a pointer to a **VARIANT** that contains a specific download property.</span></span>

## <a name="syntax"></a><span data-ttu-id="96496-106">語法</span><span class="sxs-lookup"><span data-stu-id="96496-106">Syntax</span></span>

```cpp
HRESULT GetProperty(
  DODownloadProperty propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="96496-107">參數</span><span class="sxs-lookup"><span data-stu-id="96496-107">Parameters</span></span>

`propId`

<span data-ttu-id="96496-108">取得 **DODownloadProperty**) 類型 (所需的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="96496-108">The required property ID to get (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="96496-109">產生的屬性值，儲存在 **變數** 中。</span><span class="sxs-lookup"><span data-stu-id="96496-109">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="96496-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="96496-110">Return Value</span></span>

<span data-ttu-id="96496-111">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="96496-111">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="96496-112">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="96496-112">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="96496-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="96496-113">Return value</span></span>|<span data-ttu-id="96496-114">描述</span><span class="sxs-lookup"><span data-stu-id="96496-114">Description</span></span>|
|-|-|
|<span data-ttu-id="96496-115">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="96496-115">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="96496-116">*propId* 未知。</span><span class="sxs-lookup"><span data-stu-id="96496-116">*propId* is unknown.</span></span>|
|<span data-ttu-id="96496-117">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="96496-117">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="96496-118">屬性為僅限寫入，無法讀取。</span><span class="sxs-lookup"><span data-stu-id="96496-118">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="96496-119">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="96496-119">E_NOT_SET</span></span>|<span data-ttu-id="96496-120">未透過 **SetProperty** 設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="96496-120">No such property was set via **SetProperty**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="96496-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="96496-121">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="96496-122">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="96496-122">**Minimum supported client**</span></span> | <span data-ttu-id="96496-123">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96496-123">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="96496-124">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="96496-124">**Minimum supported server**</span></span> | <span data-ttu-id="96496-125">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="96496-125">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="96496-126">**標頭**</span><span class="sxs-lookup"><span data-stu-id="96496-126">**Header**</span></span> | <span data-ttu-id="96496-127">Do。h</span><span class="sxs-lookup"><span data-stu-id="96496-127">Do.h</span></span> |
