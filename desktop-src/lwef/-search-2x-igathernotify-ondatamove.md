---
title: IGatherNotify OnDataMove (已淘汰的) 方法
description: 此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search ISearchPersistentItemsChangedSink API 取代。 |IGatherNotify OnDataMove (已淘汰的) 方法
ms.assetid: cc223d0f-6508-4e38-b365-c60660db5324
keywords:
- OnDataMove (淘汰的) 方法舊版 Windows 環境功能
- OnDataMove (淘汰的) 方法舊版 Windows 環境功能，IGatherNotify 介面
- IGatherNotify 介面舊版 Windows 環境功能，OnDataMove (已淘汰的) 方法
topic_type:
- apiref
api_name:
- IGatherNotify.OnDataMove (Deprecated)
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9fe38cd11e9072981334e5b724445ea3393d4361
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322179"
---
# <a name="igathernotifyondatamove-deprecated-method"></a><span data-ttu-id="2c6d4-107">IGatherNotify：： OnDataMove (已淘汰的) 方法</span><span class="sxs-lookup"><span data-stu-id="2c6d4-107">IGatherNotify::OnDataMove (Deprecated) method</span></span>

<span data-ttu-id="2c6d4-108">\[**OnDataMove** 可能會在作業系統或產品的後續版本中變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="2c6d4-108">\[**OnDataMove** may be altered or unavailable in subsequent versions of the operating system or product.\]</span></span>

<span data-ttu-id="2c6d4-109">此 Windows 桌面搜尋介面主題已被取代，並已由 Windows SDK 中的 Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API 取代。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-109">This Windows Desktop Search interface topic is deprecated and is superseded by the Windows Search [**ISearchPersistentItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchpersistentitemschangedsink) API in the Windows SDK.</span></span>

<span data-ttu-id="2c6d4-110">這個方法會通知索引子已移動的資料。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-110">This method notifies the indexer of data that has been moved.</span></span> <span data-ttu-id="2c6d4-111">當它將通知傳送至索引子時，它會包含舊的位址、新位址和邏輯位址。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-111">When it sends the notification to the indexer, it includes the old address, new address, and logical address.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c6d4-112">語法</span><span class="sxs-lookup"><span data-stu-id="2c6d4-112">Syntax</span></span>


```C++
void OnDataMove (Deprecated)(
  [in] long eChangeAdviseSemantics,
  [in] BSTR bstrOldAddress,
  [in] BSTR bstrNewAddress,
  [in] BSTR bstrLogicalAddress
);
```



## <a name="parameters"></a><span data-ttu-id="2c6d4-113">參數</span><span class="sxs-lookup"><span data-stu-id="2c6d4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c6d4-114">*eChangeAdviseSemantics* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c6d4-114">*eChangeAdviseSemantics* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6d4-115">類型： **long**</span><span class="sxs-lookup"><span data-stu-id="2c6d4-115">Type: **long**</span></span>

<span data-ttu-id="2c6d4-116">列舉參數，描述發生的移動類型。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-116">An enumerated parameter that describes the type of move that occurred.</span></span>

</dd> <dt>

<span data-ttu-id="2c6d4-117">*bstrOldAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c6d4-117">*bstrOldAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6d4-118">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2c6d4-118">Type: **BSTR**</span></span>

<span data-ttu-id="2c6d4-119">移動之專案的舊位址。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-119">The old address of the item that moved.</span></span> <span data-ttu-id="2c6d4-120">若為一般檔案，*eChangeAdviseSematics* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-120">For normal files,*eChangeAdviseSematics* is **NULL**.</span></span> <span data-ttu-id="2c6d4-121">針對資料夾或目錄，將 *eChangeAdviseSematics* 設定為 GTHR \_ CA \_ 語義 \_ 目錄。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-121">For a folder or directory, set *eChangeAdviseSematics* to GTHR\_CA\_SEMANTICS\_DIRECTORY.</span></span>

</dd> <dt>

<span data-ttu-id="2c6d4-122">*bstrNewAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c6d4-122">*bstrNewAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6d4-123">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2c6d4-123">Type: **BSTR**</span></span>

<span data-ttu-id="2c6d4-124">要移動之專案的新位址。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-124">The new address of the item that moved.</span></span>

</dd> <dt>

<span data-ttu-id="2c6d4-125">*bstrLogicalAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c6d4-125">*bstrLogicalAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c6d4-126">類型： **BSTR**</span><span class="sxs-lookup"><span data-stu-id="2c6d4-126">Type: **BSTR**</span></span>

<span data-ttu-id="2c6d4-127">移動之專案的邏輯位址。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-127">The logical address of the item that moved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c6d4-128">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c6d4-128">Return value</span></span>

<span data-ttu-id="2c6d4-129">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2c6d4-129">This method does not return a value.</span></span>

 

 
