---
title: 'IBackgroundCopyError GetFile 方法 (>deliveryoptimization .h) '
description: 捕獲與錯誤相關聯之檔案物件的介面指標。
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile 方法
- GetFile 方法，IBackgroundCopyError 介面
- IBackgroundCopyError 介面，GetFile 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969158"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a><span data-ttu-id="8ddbf-106">IBackgroundCopyError：： GetFile 方法</span><span class="sxs-lookup"><span data-stu-id="8ddbf-106">IBackgroundCopyError::GetFile method</span></span>

<span data-ttu-id="8ddbf-107">捕獲與錯誤相關聯之檔案物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-107">Retrieves an interface pointer to the file object associated with the error.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ddbf-108">語法</span><span class="sxs-lookup"><span data-stu-id="8ddbf-108">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="8ddbf-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ddbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ddbf-110">*ppFile* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8ddbf-110">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ddbf-111">[**IBackgroundCopyFile**](ibackgroundcopyfile.md)介面指標，其方法可用來判斷與錯誤相關聯的本機和遠端檔案名。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-111">An [**IBackgroundCopyFile**](ibackgroundcopyfile.md) interface pointer whose methods you use to determine the local and remote file names associated with the error.</span></span> <span data-ttu-id="8ddbf-112">如果錯誤未與本機或遠端檔案相關聯， *ppFile* 參數會設為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-112">The *ppFile* parameter is set to **NULL** if the error is not associated with the local or remote file.</span></span> <span data-ttu-id="8ddbf-113">完成時，發行 *ppFile*。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-113">When done, release *ppFile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ddbf-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ddbf-114">Return value</span></span>

<span data-ttu-id="8ddbf-115">這個方法會傳回下列 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-115">This method returns the following **HRESULT** values.</span></span>



| <span data-ttu-id="8ddbf-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8ddbf-116">Return code</span></span>                                                                                                | <span data-ttu-id="8ddbf-117">Description</span><span class="sxs-lookup"><span data-stu-id="8ddbf-117">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8ddbf-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="8ddbf-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                   | <span data-ttu-id="8ddbf-119">已成功取出檔案物件的介面指標。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-119">Successfully retrieved an interface pointer to the file object.</span></span><br/>                                     |
| <dl> <span data-ttu-id="8ddbf-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="8ddbf-120"><dt>**DO_E_FILE_NOT_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="8ddbf-121">錯誤未與本機或遠端檔案相關聯。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-121">The error is not associated with a local or remote file.</span></span> <span data-ttu-id="8ddbf-122">*PpFile* 參數設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8ddbf-122">The *ppFile* parameter is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8ddbf-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ddbf-123">Requirements</span></span>



| <span data-ttu-id="8ddbf-124">需求</span><span class="sxs-lookup"><span data-stu-id="8ddbf-124">Requirement</span></span> | <span data-ttu-id="8ddbf-125">值</span><span class="sxs-lookup"><span data-stu-id="8ddbf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ddbf-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ddbf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8ddbf-127">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ddbf-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8ddbf-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ddbf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8ddbf-129">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8ddbf-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8ddbf-130">標頭</span><span class="sxs-lookup"><span data-stu-id="8ddbf-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ddbf-131"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="8ddbf-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="8ddbf-132">Idl</span><span class="sxs-lookup"><span data-stu-id="8ddbf-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8ddbf-133"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ddbf-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="8ddbf-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="8ddbf-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="8ddbf-135"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ddbf-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="8ddbf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="8ddbf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ddbf-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ddbf-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="8ddbf-138">IID</span><span class="sxs-lookup"><span data-stu-id="8ddbf-138">IID</span></span><br/>                      | <span data-ttu-id="8ddbf-139">IID_IBackgroundCopyError 定義為19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="8ddbf-139">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="8ddbf-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ddbf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ddbf-141">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="8ddbf-141">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="8ddbf-142">**IBackgroundCopyError::GetError**</span><span class="sxs-lookup"><span data-stu-id="8ddbf-142">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





