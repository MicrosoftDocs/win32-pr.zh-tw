---
title: IWMDRMDevice2 GetPartialSyncList 方法
description: GetPartialSyncList 方法會取得部分同步處理清單。
ms.assetid: 4ee8e9d7-d5d1-4614-b7a1-1dcb7f07b161
keywords:
- GetPartialSyncList 方法 windows Media 裝置管理員
- GetPartialSyncList 方法 windows Media 裝置管理員，IWMDRMDevice2 介面
- IWMDRMDevice2 interface windows Media 裝置管理員，GetPartialSyncList 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetPartialSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c68c9c9a0bc47dcbea25158bb1f25db6cd084075
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996040"
---
# <a name="iwmdrmdevice2getpartialsynclist-method"></a><span data-ttu-id="abe2e-106">IWMDRMDevice2：： GetPartialSyncList 方法</span><span class="sxs-lookup"><span data-stu-id="abe2e-106">IWMDRMDevice2::GetPartialSyncList method</span></span>

<span data-ttu-id="abe2e-107">**GetPartialSyncList** 方法會取得部分同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="abe2e-107">The **GetPartialSyncList** method gets a partial synchronization list.</span></span>

## <a name="syntax"></a><span data-ttu-id="abe2e-108">語法</span><span class="sxs-lookup"><span data-stu-id="abe2e-108">Syntax</span></span>


```C++
HRESULT GetPartialSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [in]  DWORD dwStartingIndex,
  [in]  DWORD cItems,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList,
  [out] DWORD *pdwNextStartingIndex,
  [out] DWORD *pcItemsProcessed
);
```



## <a name="parameters"></a><span data-ttu-id="abe2e-109">參數</span><span class="sxs-lookup"><span data-stu-id="abe2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abe2e-110">*cMinCountThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-110">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-111">最小計數閾值。</span><span class="sxs-lookup"><span data-stu-id="abe2e-111">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-112">*cMinHoursThreshold* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-112">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-113">最小時間閾值。</span><span class="sxs-lookup"><span data-stu-id="abe2e-113">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-114">*dwStartingIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-114">*dwStartingIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-115">索引的開始位置。</span><span class="sxs-lookup"><span data-stu-id="abe2e-115">Start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-116">*cItems* \[在\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-116">*cItems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-117">要編制索引的專案計數。</span><span class="sxs-lookup"><span data-stu-id="abe2e-117">Count of items to be indexed.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-118">*ppbSyncList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-118">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-119">已取出授權同步處理清單。</span><span class="sxs-lookup"><span data-stu-id="abe2e-119">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-120">*pcbSyncList* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-120">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-121">授權同步清單的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="abe2e-121">Size of the license synchronization list, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-122">*pdwNextStartingIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-122">*pdwNextStartingIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-123">索引的下一個開始位置。</span><span class="sxs-lookup"><span data-stu-id="abe2e-123">Next start position for indexing.</span></span>

</dd> <dt>

<span data-ttu-id="abe2e-124">*pcItemsProcessed* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="abe2e-124">*pcItemsProcessed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abe2e-125">正在處理的專案計數。</span><span class="sxs-lookup"><span data-stu-id="abe2e-125">Count of items being processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abe2e-126">傳回值</span><span class="sxs-lookup"><span data-stu-id="abe2e-126">Return value</span></span>

<span data-ttu-id="abe2e-127">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="abe2e-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="abe2e-128">Windows Media 裝置管理員中的所有介面方法都可以傳回下列任何錯誤碼類別：</span><span class="sxs-lookup"><span data-stu-id="abe2e-128">All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:</span></span>

-   <span data-ttu-id="abe2e-129">標準 COM 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="abe2e-129">Standard COM error codes</span></span>
-   <span data-ttu-id="abe2e-130">轉換成 HRESULT 值的 Windows 錯誤碼</span><span class="sxs-lookup"><span data-stu-id="abe2e-130">Windows error codes converted to HRESULT values</span></span>
-   <span data-ttu-id="abe2e-131">Windows Media 裝置管理員錯誤碼</span><span class="sxs-lookup"><span data-stu-id="abe2e-131">Windows Media Device Manager error codes</span></span>

<span data-ttu-id="abe2e-132">如需可能錯誤碼的詳細清單，請參閱 [錯誤碼](error-codes.md)。</span><span class="sxs-lookup"><span data-stu-id="abe2e-132">For an extensive list of possible error codes, see [Error Codes](error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abe2e-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="abe2e-133">Requirements</span></span>



| <span data-ttu-id="abe2e-134">需求</span><span class="sxs-lookup"><span data-stu-id="abe2e-134">Requirement</span></span> | <span data-ttu-id="abe2e-135">值</span><span class="sxs-lookup"><span data-stu-id="abe2e-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="abe2e-136">標頭</span><span class="sxs-lookup"><span data-stu-id="abe2e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="abe2e-137"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="abe2e-137"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="abe2e-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="abe2e-138">Library</span></span><br/> | <dl> <span data-ttu-id="abe2e-139"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="abe2e-139"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abe2e-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="abe2e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abe2e-141">**IWMDRMDevice::GetSyncList**</span><span class="sxs-lookup"><span data-stu-id="abe2e-141">**IWMDRMDevice::GetSyncList**</span></span>](iwmdrmdevice-getsynclist.md)
</dt> <dt>

[<span data-ttu-id="abe2e-142">**IWMDRMDevice2 介面**</span><span class="sxs-lookup"><span data-stu-id="abe2e-142">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





