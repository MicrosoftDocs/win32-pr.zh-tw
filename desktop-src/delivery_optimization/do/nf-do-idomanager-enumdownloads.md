---
title: IDOManager：： EnumDownloads 方法
description: 抓取列舉值物件的介面指標，此列舉值物件是用來列舉現有的下載。
keywords:
- IDOManager：： EnumDownloads 方法
topic_type:
- apiref
api_name:
- IDOManager.EnumDownloads
api_location:
- dosvc.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/03/2019
ms.openlocfilehash: a1e7fed2955fdc1b5ac0c11cfebc34aa95517603
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106968475"
---
# <a name="idomanagerenumdownloads-method"></a><span data-ttu-id="6ecb2-104">IDOManager：： EnumDownloads 方法</span><span class="sxs-lookup"><span data-stu-id="6ecb2-104">IDOManager::EnumDownloads method</span></span>

<span data-ttu-id="6ecb2-105">抓取列舉值物件的介面指標，此列舉值物件是用來列舉現有的下載。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-105">Retrieves an interface pointer to an enumerator object that is used to enumerate existing downloads.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ecb2-106">語法</span><span class="sxs-lookup"><span data-stu-id="6ecb2-106">Syntax</span></span>

```cpp
HRESULT EnumDownloads(
  DO_DOWNLOAD_ENUM_CATEGORY *category, 
  IEnumUnknown **ppEnum
);
```

## <a name="parameters"></a><span data-ttu-id="6ecb2-107">參數</span><span class="sxs-lookup"><span data-stu-id="6ecb2-107">Parameters</span></span>

`category`

<span data-ttu-id="6ecb2-108">選擇性。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-108">Optional.</span></span> <span data-ttu-id="6ecb2-109">要用來做為列舉類別的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-109">The property name to be used as a category to enumerate.</span></span> <span data-ttu-id="6ecb2-110">傳遞 `nullptr` 將會取得所有現有的下載。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-110">Passing `nullptr` will retrieve all existing downloads.</span></span> <span data-ttu-id="6ecb2-111">以下是支援類別的屬性。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-111">The following properties are supported as a category.</span></span>

- <span data-ttu-id="6ecb2-112">**DODownloadProperty_Id**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-112">**DODownloadProperty_Id**</span></span>
- <span data-ttu-id="6ecb2-113">**DODownloadProperty_Uri**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-113">**DODownloadProperty_Uri**</span></span>
- <span data-ttu-id="6ecb2-114">**DODownloadProperty_ContentId**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-114">**DODownloadProperty_ContentId**</span></span>
- <span data-ttu-id="6ecb2-115">**DODownloadProperty_DisplayName**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-115">**DODownloadProperty_DisplayName**</span></span>
- <span data-ttu-id="6ecb2-116">**DODownloadProperty_LocalPath**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-116">**DODownloadProperty_LocalPath**</span></span>

`ppEnum`

<span data-ttu-id="6ecb2-117">**IEnumUnknown** 介面指標的位址，用來列舉現有的下載。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-117">The address of an interface pointer to **IEnumUnknown**, which is used to enumerate existing downloads.</span></span> <span data-ttu-id="6ecb2-118">列舉值的內容取決於 *類別* 的值。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-118">The contents of the enumerator depend on the value of *category*.</span></span> <span data-ttu-id="6ecb2-119">列舉介面中包含的下載專案是先前由相同呼叫端為此函式建立的下載專案。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-119">The downloads included in the enumeration interface are the ones that were previously created by the same caller to this function.</span></span> 

## <a name="return-value"></a><span data-ttu-id="6ecb2-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ecb2-120">Return Value</span></span>

<span data-ttu-id="6ecb2-121">如果函式成功，它會傳回 **S_OK**。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-121">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="6ecb2-122">否則，它會傳回 [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [錯誤碼](/windows/desktop/com/com-error-codes-10)。</span><span class="sxs-lookup"><span data-stu-id="6ecb2-122">Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) [error code](/windows/desktop/com/com-error-codes-10).</span></span>

## <a name="requirements"></a><span data-ttu-id="6ecb2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ecb2-123">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6ecb2-124">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-124">**Minimum supported client**</span></span> | <span data-ttu-id="6ecb2-125">\[僅限 Windows 10 版本1809的 Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ecb2-125">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6ecb2-126">**最低支援的伺服器**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-126">**Minimum supported server**</span></span> | <span data-ttu-id="6ecb2-127">Windows Server，僅限1809版的 \[ Win32 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ecb2-127">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="6ecb2-128">**標頭**</span><span class="sxs-lookup"><span data-stu-id="6ecb2-128">**Header**</span></span> | <span data-ttu-id="6ecb2-129">Do。h</span><span class="sxs-lookup"><span data-stu-id="6ecb2-129">Do.h</span></span> |
