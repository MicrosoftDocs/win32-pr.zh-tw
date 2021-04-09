---
title: 'IEnumBackgroundCopyFiles GetCount 方法 (>deliveryoptimization .h) '
description: 捕獲列舉中的檔案數目計數。
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount 方法
- GetCount 方法，IEnumBackgroundCopyFiles 介面
- IEnumBackgroundCopyFiles 介面，GetCount 方法
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685900"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="59bbe-106">IEnumBackgroundCopyFiles：： GetCount 方法</span><span class="sxs-lookup"><span data-stu-id="59bbe-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="59bbe-107">捕獲列舉中的檔案數目計數。</span><span class="sxs-lookup"><span data-stu-id="59bbe-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="59bbe-108">語法</span><span class="sxs-lookup"><span data-stu-id="59bbe-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="59bbe-109">參數</span><span class="sxs-lookup"><span data-stu-id="59bbe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59bbe-110">*pCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="59bbe-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="59bbe-111">列舉中的檔案數目。</span><span class="sxs-lookup"><span data-stu-id="59bbe-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59bbe-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="59bbe-112">Return value</span></span>

<span data-ttu-id="59bbe-113">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="59bbe-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="59bbe-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="59bbe-114">Requirements</span></span>



| <span data-ttu-id="59bbe-115">需求</span><span class="sxs-lookup"><span data-stu-id="59bbe-115">Requirement</span></span> | <span data-ttu-id="59bbe-116">值</span><span class="sxs-lookup"><span data-stu-id="59bbe-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59bbe-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59bbe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="59bbe-118">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59bbe-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="59bbe-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59bbe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="59bbe-120">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59bbe-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="59bbe-121">標頭</span><span class="sxs-lookup"><span data-stu-id="59bbe-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="59bbe-122"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="59bbe-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="59bbe-123">Idl</span><span class="sxs-lookup"><span data-stu-id="59bbe-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="59bbe-124"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="59bbe-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="59bbe-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="59bbe-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="59bbe-126"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="59bbe-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="59bbe-127">DLL</span><span class="sxs-lookup"><span data-stu-id="59bbe-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59bbe-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59bbe-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="59bbe-129">IID</span><span class="sxs-lookup"><span data-stu-id="59bbe-129">IID</span></span><br/>                      | <span data-ttu-id="59bbe-130">IID_IEnumBackgroundCopyFiles 定義為 CA51E165-C365-424C-8D41-24AAA4FF3C40</span><span class="sxs-lookup"><span data-stu-id="59bbe-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="59bbe-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59bbe-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59bbe-132">**IEnumBackgroundCopyFiles**</span><span class="sxs-lookup"><span data-stu-id="59bbe-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





