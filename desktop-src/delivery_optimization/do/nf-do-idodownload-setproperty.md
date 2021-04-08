---
title: IDODownload：： SetProperty 方法
description: 設定下載屬性。
keywords:
- IDODownload：： SetProperty 方法
topic_type:
- apiref
api_name:
- IDODownload.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: 0d496f49851aab665e49f3aaeb51e4b941d6c183
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679243"
---
# <a name="idodownloadsetproperty-method"></a><span data-ttu-id="d9bf4-104">IDODownload：： SetProperty 方法</span><span class="sxs-lookup"><span data-stu-id="d9bf4-104">IDODownload::SetProperty method</span></span>

<span data-ttu-id="d9bf4-105">設定下載屬性。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-105">Sets a download property.</span></span> <span data-ttu-id="d9bf4-106">方法會接受 VARIANT 的指標，該 **變數** 包含要套用至下載的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-106">The method accepts a pointer to a **VARIANT** that contains a specific property to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9bf4-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9bf4-107">Syntax</span></span>

```cpp
HRESULT SetProperty(
  DODownloadProperty propId,
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="d9bf4-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9bf4-108">Parameters</span></span>

`propId`

<span data-ttu-id="d9bf4-109">要設定 **DODownloadProperty**) 類型 (所需的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-109">The required property ID to set (of type **DODownloadProperty**).</span></span>

`propVal`

<span data-ttu-id="d9bf4-110">要設定的屬性值，儲存在 **變數** 中。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-110">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9bf4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9bf4-111">Return Value</span></span>

<span data-ttu-id="d9bf4-112">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-112">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="d9bf4-113">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-113">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="d9bf4-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9bf4-114">Return value</span></span>|<span data-ttu-id="d9bf4-115">描述</span><span class="sxs-lookup"><span data-stu-id="d9bf4-115">Description</span></span>|
|-|-|
|<span data-ttu-id="d9bf4-116">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="d9bf4-116">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="d9bf4-117">*propId* 未知。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-117">*propId* is unknown.</span></span>|
|<span data-ttu-id="d9bf4-118">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="d9bf4-118">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="d9bf4-119">下載目前不是允許設定屬性的狀態。</span><span class="sxs-lookup"><span data-stu-id="d9bf4-119">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="d9bf4-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9bf4-120">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d9bf4-121">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="d9bf4-121">**Minimum supported client**</span></span> | <span data-ttu-id="d9bf4-122">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9bf4-122">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d9bf4-123">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="d9bf4-123">**Minimum supported server**</span></span> | <span data-ttu-id="d9bf4-124">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d9bf4-124">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="d9bf4-125">**標頭**</span><span class="sxs-lookup"><span data-stu-id="d9bf4-125">**Header**</span></span> | <span data-ttu-id="d9bf4-126">Do。h</span><span class="sxs-lookup"><span data-stu-id="d9bf4-126">Do.h</span></span> |
