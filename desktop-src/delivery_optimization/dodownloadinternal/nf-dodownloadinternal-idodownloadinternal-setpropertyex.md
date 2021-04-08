---
title: IDODownloadInternal：： SetPropertyEx 方法
description: 設定延伸的下載屬性。 方法會接受 **VARIANT** 的指標，其中包含要套用至下載的特定屬性值。
keywords:
- IDODownloadInternal：： SetPropertyEx 方法
topic_type:
- apiref
api_name:
- IDODownloadInternal.SetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: e6630cc3e767531dd94da39fe73d88284c9ca0d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933288"
---
# <a name="idodownloadinternalsetpropertyex-method"></a><span data-ttu-id="5b973-105">IDODownloadInternal：： SetPropertyEx 方法</span><span class="sxs-lookup"><span data-stu-id="5b973-105">IDODownloadInternal::SetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5b973-106">**IDODownloadInternal** 介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="5b973-106">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="5b973-107">請改用 [IDODownload](../do/nn-do-idodownload.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="5b973-107">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="5b973-108">設定延伸的下載屬性。</span><span class="sxs-lookup"><span data-stu-id="5b973-108">Sets an extended download property.</span></span> <span data-ttu-id="5b973-109">方法會接受 **VARIANT** 的指標，其中包含要套用至下載的特定屬性值。</span><span class="sxs-lookup"><span data-stu-id="5b973-109">The method accepts a pointer to a **VARIANT** that contains a specific property value to apply to the download.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b973-110">語法</span><span class="sxs-lookup"><span data-stu-id="5b973-110">Syntax</span></span>

```cpp
HRESULT SetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="5b973-111">參數</span><span class="sxs-lookup"><span data-stu-id="5b973-111">Parameters</span></span>

`propId`

<span data-ttu-id="5b973-112">要設定 **DODownloadPropertyEx**) 類型 (所需的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b973-112">The required property ID to set (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="5b973-113">要設定的屬性值，儲存在 **變數** 中。</span><span class="sxs-lookup"><span data-stu-id="5b973-113">The property value to set, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="5b973-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b973-114">Return Value</span></span>

<span data-ttu-id="5b973-115">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="5b973-115">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="5b973-116">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="5b973-116">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="5b973-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b973-117">Return value</span></span>|<span data-ttu-id="5b973-118">描述</span><span class="sxs-lookup"><span data-stu-id="5b973-118">Description</span></span>|
|-|-|
|<span data-ttu-id="5b973-119">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="5b973-119">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="5b973-120">*propId* 未知。</span><span class="sxs-lookup"><span data-stu-id="5b973-120">*propId* is unknown.</span></span>|
|<span data-ttu-id="5b973-121">DO_E_INVALID_STATE</span><span class="sxs-lookup"><span data-stu-id="5b973-121">DO_E_INVALID_STATE</span></span>|<span data-ttu-id="5b973-122">下載目前不是允許設定屬性的狀態。</span><span class="sxs-lookup"><span data-stu-id="5b973-122">The download is not currently in a state that allows setting properties.</span></span>|

## <a name="requirements"></a><span data-ttu-id="5b973-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b973-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5b973-124">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="5b973-124">**Minimum supported client**</span></span> | <span data-ttu-id="5b973-125">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b973-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="5b973-126">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="5b973-126">**Minimum supported server**</span></span> | <span data-ttu-id="5b973-127">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5b973-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="5b973-128">**標頭**</span><span class="sxs-lookup"><span data-stu-id="5b973-128">**Header**</span></span> | <span data-ttu-id="5b973-129">DODownloadInternal。h</span><span class="sxs-lookup"><span data-stu-id="5b973-129">DODownloadInternal.h</span></span> |