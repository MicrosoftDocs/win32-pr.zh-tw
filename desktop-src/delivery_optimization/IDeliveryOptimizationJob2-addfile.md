---
title: IDeliveryOptimizationJob2 AddFile 方法
description: AddFile 方法會將單一檔案新增至現有的作業。
keywords:
- AddFile 方法
- AddFile 方法，IDeliveryOptimizationJob2 介面
- IDeliveryOptimizationJob2 介面，AddFile 方法
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.AddFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8225db8cccb1e1d3bb364ba1dc29f30526fe36b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094195"
---
# <a name="ideliveryoptimizationjob2addfilewithranges-method"></a><span data-ttu-id="a9324-106">IDeliveryOptimizationJob2：： AddFileWithRanges 方法</span><span class="sxs-lookup"><span data-stu-id="a9324-106">IDeliveryOptimizationJob2::AddFileWithRanges method</span></span>

<span data-ttu-id="a9324-107">AddFile 方法會將單一檔案新增至現有的作業。</span><span class="sxs-lookup"><span data-stu-id="a9324-107">The AddFile method adds a single file to an existing DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9324-108">語法</span><span class="sxs-lookup"><span data-stu-id="a9324-108">Syntax</span></span>

```C++
HRESULT AddFile(
  [in]                              LPCWSTR       fileId,
  [in, unique]                      LPCWSTR       remoteUrl,
  [in]                              DWORD         rangeCount,
  [in, size_is(rangeCount), unique] BG_FILE_RANGE ranges[],
  [in]                              REFIID        riid,
  [out]                             void          **object
);
```

## <a name="parameters"></a><span data-ttu-id="a9324-109">參數</span><span class="sxs-lookup"><span data-stu-id="a9324-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9324-110">*fileId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9324-110">*fileId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9324-111">檔案識別碼字串，可唯一識別要下載的檔案。</span><span class="sxs-lookup"><span data-stu-id="a9324-111">The file ID string, which uniquely identifies the file to be downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="a9324-112">*remoteUrl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9324-112">*remoteUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9324-113">將嘗試連接以下載檔案的檔案 URL。</span><span class="sxs-lookup"><span data-stu-id="a9324-113">The file URL that DO will attempt to connect to download the file.</span></span>

</dd> <dt>

<span data-ttu-id="a9324-114">*rangeCount* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9324-114">*rangeCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9324-115">*範圍* 中包含的專案數目。</span><span class="sxs-lookup"><span data-stu-id="a9324-115">The number of items contained in *ranges*.</span></span> <span data-ttu-id="a9324-116">零值表示沒有任何範圍用於檔案。</span><span class="sxs-lookup"><span data-stu-id="a9324-116">A zero value means that no ranges are used for the file.</span></span>

</dd> <dt>

<span data-ttu-id="a9324-117">*範圍* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9324-117">*ranges* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9324-118">選用的範圍清單。</span><span class="sxs-lookup"><span data-stu-id="a9324-118">The optional range list.</span></span> <span data-ttu-id="a9324-119">清單中的每個範圍都是 [**BG_FILE_RANGE**](bg-file-range.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="a9324-119">Each range in the list is a [**BG_FILE_RANGE**](bg-file-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a9324-120">*riid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a9324-120">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9324-121">物件中包含的物件類型。</span><span class="sxs-lookup"><span data-stu-id="a9324-121">The type of object contained in object.</span></span> <span data-ttu-id="a9324-122">這必須由類型 IID_IDeliveryOptimizationFile。</span><span class="sxs-lookup"><span data-stu-id="a9324-122">This must by of type IID_IDeliveryOptimizationFile.</span></span>

</dd> <dt>

<span data-ttu-id="a9324-123">*物件* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a9324-123">*object* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9324-124">IDeliveryOptimizationFile 物件，代表下載檔案。</span><span class="sxs-lookup"><span data-stu-id="a9324-124">The IDeliveryOptimizationFile object, which represents the download file.</span></span> 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9324-125">傳回值</span><span class="sxs-lookup"><span data-stu-id="a9324-125">Return value</span></span>

<span data-ttu-id="a9324-126">這個方法會在成功時傳回 S_OK，或在發生錯誤時傳回其中一個標準 HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="a9324-126">This method returns S_OK on success or one of the standard HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9324-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9324-127">Requirements</span></span>

| <span data-ttu-id="a9324-128">需求</span><span class="sxs-lookup"><span data-stu-id="a9324-128">Requirement</span></span> | <span data-ttu-id="a9324-129">值</span><span class="sxs-lookup"><span data-stu-id="a9324-129">Value</span></span> |
|---------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="a9324-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9324-130">Minimum supported client</span></span>  | <span data-ttu-id="a9324-131">Windows 10， \[ 僅限1803版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9324-131">Windows 10, version 1803 \[desktop apps only\]</span></span>                                  |
| <span data-ttu-id="a9324-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9324-132">Minimum supported server</span></span>  | <span data-ttu-id="a9324-133">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9324-133">Windows Server, version 1709 \[desktop apps only\]</span></span>                              |
| <span data-ttu-id="a9324-134">標頭</span><span class="sxs-lookup"><span data-stu-id="a9324-134">Header</span></span>                    | <span data-ttu-id="a9324-135">>deliveryoptimization。h</span><span class="sxs-lookup"><span data-stu-id="a9324-135">Deliveryoptimization.h</span></span>                                                          |
| <span data-ttu-id="a9324-136">Idl</span><span class="sxs-lookup"><span data-stu-id="a9324-136">IDL</span></span>                       | <span data-ttu-id="a9324-137">>deliveryoptimization .idl</span><span class="sxs-lookup"><span data-stu-id="a9324-137">DeliveryOptimization.idl</span></span>                                                        |
| <span data-ttu-id="a9324-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="a9324-138">Library</span></span>                   | <span data-ttu-id="a9324-139">Dosvc .lib</span><span class="sxs-lookup"><span data-stu-id="a9324-139">Dosvc.lib</span></span>                                                                       |
| <span data-ttu-id="a9324-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a9324-140">DLL</span></span>                       | <span data-ttu-id="a9324-141">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="a9324-141">Dosvc.dll</span></span>                                                                       |
| <span data-ttu-id="a9324-142">IID</span><span class="sxs-lookup"><span data-stu-id="a9324-142">IID</span></span>                       | <span data-ttu-id="a9324-143">IID_IDeliveryOptimizationJob 定義為 EE2584CF-A69C-4848-B633-2649962B3EF7</span><span class="sxs-lookup"><span data-stu-id="a9324-143">IID_IDeliveryOptimizationJob is defined as EE2584CF-A69C-4848-B633-2649962B3EF7</span></span> |

## <a name="see-also"></a><span data-ttu-id="a9324-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a9324-144">See also</span></span>

[<span data-ttu-id="a9324-145">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="a9324-145">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
