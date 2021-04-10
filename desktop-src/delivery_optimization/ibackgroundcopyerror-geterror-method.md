---
title: 'IBackgroundCopyError GetError 方法 (>deliveryoptimization .h) '
description: 抓取錯誤碼，並找出發生錯誤的內容。
ms.assetid: C87897CD-9648-4CEF-B963-68EE35356929
keywords:
- GetError 方法
- GetError 方法，IBackgroundCopyError 介面
- IBackgroundCopyError 介面，GetError 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e14803c225ade6085658582e18b9ba2d52fc90c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934285"
---
# <a name="ibackgroundcopyerrorgeterror-method"></a><span data-ttu-id="f3f76-106">IBackgroundCopyError：： GetError 方法</span><span class="sxs-lookup"><span data-stu-id="f3f76-106">IBackgroundCopyError::GetError method</span></span>

<span data-ttu-id="f3f76-107">抓取錯誤碼，並找出發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="f3f76-107">Retrieves the error code and identify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3f76-108">語法</span><span class="sxs-lookup"><span data-stu-id="f3f76-108">Syntax</span></span>


```C++
HRESULT GetError(
  [out] BG_ERROR_CONTEXT *pContext,
  [out] HRESULT          *pErrorCode
);
```



## <a name="parameters"></a><span data-ttu-id="f3f76-109">參數</span><span class="sxs-lookup"><span data-stu-id="f3f76-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3f76-110">*pCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3f76-110">*pContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f76-111">發生錯誤的內容。</span><span class="sxs-lookup"><span data-stu-id="f3f76-111">Context in which the error occurred.</span></span> <span data-ttu-id="f3f76-112">如需內容值的清單，請參閱 [**BG_ERROR_CONTEXT**](bg-error-context.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="f3f76-112">For a list of context values, see the [**BG_ERROR_CONTEXT**](bg-error-context.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="f3f76-113">*pErrorCode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f3f76-113">*pErrorCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f3f76-114">發生的錯誤錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f3f76-114">Error code of the error that occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3f76-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3f76-115">Return value</span></span>

<span data-ttu-id="f3f76-116">這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM HRESULT 值。</span><span class="sxs-lookup"><span data-stu-id="f3f76-116">This method returns **S_OK** on success or one of the standard COM HRESULT values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3f76-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3f76-117">Requirements</span></span>



| <span data-ttu-id="f3f76-118">需求</span><span class="sxs-lookup"><span data-stu-id="f3f76-118">Requirement</span></span> | <span data-ttu-id="f3f76-119">值</span><span class="sxs-lookup"><span data-stu-id="f3f76-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3f76-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3f76-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f3f76-121">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3f76-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f3f76-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3f76-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f3f76-123">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3f76-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="f3f76-124">標頭</span><span class="sxs-lookup"><span data-stu-id="f3f76-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3f76-125"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3f76-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="f3f76-126">Idl</span><span class="sxs-lookup"><span data-stu-id="f3f76-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f3f76-127"><dt>>deliveryoptimization .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f3f76-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="f3f76-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="f3f76-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="f3f76-129"><dt>Dosvc .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f3f76-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="f3f76-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f3f76-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3f76-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3f76-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="f3f76-132">IID</span><span class="sxs-lookup"><span data-stu-id="f3f76-132">IID</span></span><br/>                      | <span data-ttu-id="f3f76-133">IID_IBackgroundCopyError 定義為19C613A0-FCB8-4F28-81AE-897C3D078F81</span><span class="sxs-lookup"><span data-stu-id="f3f76-133">IID_IBackgroundCopyError is defined as 19C613A0-FCB8-4F28-81AE-897C3D078F81</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f3f76-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3f76-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3f76-135">**IBackgroundCopyError**</span><span class="sxs-lookup"><span data-stu-id="f3f76-135">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="f3f76-136">**IBackgroundCopyError：： GetFile**</span><span class="sxs-lookup"><span data-stu-id="f3f76-136">**IBackgroundCopyError::GetFile**</span></span>](ibackgroundcopyerror-getfile-method.md)
</dt> </dl>

 

 





