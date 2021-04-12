---
title: IDODownloadInternal：： GetPropertyEx 方法
description: 抓取包含特定延伸下載屬性值之 **變數** 的指標。
keywords:
- IDODownloadInternal：： GetPropertyEx 方法
topic_type:
- apiref
api_name:
- IDODownloadInternal.GetPropertyEx
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 908f9b15df5c0c4a2769149419ff12d545201e5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375836"
---
# <a name="idodownloadinternalgetpropertyex-method"></a><span data-ttu-id="6682b-104">IDODownloadInternal：： GetPropertyEx 方法</span><span class="sxs-lookup"><span data-stu-id="6682b-104">IDODownloadInternal::GetPropertyEx method</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6682b-105">**IDODownloadInternal** 介面已被取代。</span><span class="sxs-lookup"><span data-stu-id="6682b-105">The **IDODownloadInternal** interface is deprecated.</span></span> <span data-ttu-id="6682b-106">請改用 [IDODownload](../do/nn-do-idodownload.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="6682b-106">Instead, use the [IDODownload](../do/nn-do-idodownload.md) interface.</span></span>

<span data-ttu-id="6682b-107">抓取包含特定延伸下載屬性值之 **變數** 的指標。</span><span class="sxs-lookup"><span data-stu-id="6682b-107">Retrieves a pointer to a **VARIANT** that contains a specific extended download property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="6682b-108">語法</span><span class="sxs-lookup"><span data-stu-id="6682b-108">Syntax</span></span>

```cpp
HRESULT GetPropertyEx(
  DODownloadPropertyEx propId, 
  VARIANT* propVal
);
```

## <a name="parameters"></a><span data-ttu-id="6682b-109">參數</span><span class="sxs-lookup"><span data-stu-id="6682b-109">Parameters</span></span>

`propId`

<span data-ttu-id="6682b-110">取得 **DODownloadPropertyEx**) 類型 (所需的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="6682b-110">The required property ID to get (of type **DODownloadPropertyEx**).</span></span>

`propVal`

<span data-ttu-id="6682b-111">產生的屬性值，儲存在 **變數** 中。</span><span class="sxs-lookup"><span data-stu-id="6682b-111">The resulting property value, stored in a **VARIANT**.</span></span>

## <a name="return-value"></a><span data-ttu-id="6682b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6682b-112">Return Value</span></span>

<span data-ttu-id="6682b-113">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="6682b-113">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="6682b-114">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="6682b-114">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

|<span data-ttu-id="6682b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6682b-115">Return value</span></span>|<span data-ttu-id="6682b-116">描述</span><span class="sxs-lookup"><span data-stu-id="6682b-116">Description</span></span>|
|-|-|
|<span data-ttu-id="6682b-117">DO_E_UNKNOWN_PROPERTY_ID</span><span class="sxs-lookup"><span data-stu-id="6682b-117">DO_E_UNKNOWN_PROPERTY_ID</span></span>|<span data-ttu-id="6682b-118">*propId* 未知。</span><span class="sxs-lookup"><span data-stu-id="6682b-118">*propId* is unknown.</span></span>|
|<span data-ttu-id="6682b-119">DO_E_WRITE_ONLY_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="6682b-119">DO_E_WRITE_ONLY_PROPERTY</span></span>|<span data-ttu-id="6682b-120">屬性為僅限寫入，無法讀取。</span><span class="sxs-lookup"><span data-stu-id="6682b-120">The property is write-only, and cannot be read.</span></span>|
|<span data-ttu-id="6682b-121">E_NOT_SET</span><span class="sxs-lookup"><span data-stu-id="6682b-121">E_NOT_SET</span></span>|<span data-ttu-id="6682b-122">未透過 **SetPropertyEx** 設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="6682b-122">No such property was set via **SetPropertyEx**.</span></span>|

## <a name="requirements"></a><span data-ttu-id="6682b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6682b-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6682b-124">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="6682b-124">**Minimum supported client**</span></span> | <span data-ttu-id="6682b-125">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6682b-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6682b-126">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="6682b-126">**Minimum supported server**</span></span> | <span data-ttu-id="6682b-127">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6682b-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6682b-128">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6682b-128">**Header**</span></span> | <span data-ttu-id="6682b-129">DODownloadInternal。h</span><span class="sxs-lookup"><span data-stu-id="6682b-129">DODownloadInternal.h</span></span> |