---
title: 'INapComponentInfo GetVendorName 方法 (NapCommon .h) '
description: 是由 NAP 系統用來取得健康情況用戶端的廠商名稱。
ms.assetid: 7083b0b6-38fc-4c24-a5f7-fe0a1ebd5e88
keywords:
- GetVendorName 方法 NAP
- GetVendorName 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetVendorName 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVendorName
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3c82f4e7e4f76d827e71421c467a8a223428a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104467069"
---
# <a name="inapcomponentinfogetvendorname-method"></a><span data-ttu-id="c0f30-106">INapComponentInfo：： GetVendorName 方法</span><span class="sxs-lookup"><span data-stu-id="c0f30-106">INapComponentInfo::GetVendorName method</span></span>

> [!Note]  
> <span data-ttu-id="c0f30-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="c0f30-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c0f30-108">**INapComponentInfo：： GetVendorName** 回呼方法是由 NAP 系統用來取得健康情況用戶端的廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="c0f30-108">The **INapComponentInfo::GetVendorName** callback method is used by the NAP System to get the vendor name of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f30-109">語法</span><span class="sxs-lookup"><span data-stu-id="c0f30-109">Syntax</span></span>


```C++
HRESULT GetVendorName(
  [out] MessageId *vendorName
);
```



## <a name="parameters"></a><span data-ttu-id="c0f30-110">參數</span><span class="sxs-lookup"><span data-stu-id="c0f30-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0f30-111">*vendorName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c0f30-111">*vendorName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0f30-112">[**MessageId**](nap-datatypes.md)的指標，其中包含廠商名稱的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c0f30-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the vendor name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0f30-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0f30-113">Return value</span></span>

<span data-ttu-id="c0f30-114">根據此作業的結果傳回這些錯誤碼的其中一個。</span><span class="sxs-lookup"><span data-stu-id="c0f30-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="c0f30-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c0f30-115">Return code</span></span>                                                                                     | <span data-ttu-id="c0f30-116">Description</span><span class="sxs-lookup"><span data-stu-id="c0f30-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c0f30-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f30-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c0f30-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="c0f30-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="c0f30-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f30-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c0f30-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c0f30-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c0f30-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c0f30-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c0f30-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="c0f30-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c0f30-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0f30-123">Requirements</span></span>



| <span data-ttu-id="c0f30-124">需求</span><span class="sxs-lookup"><span data-stu-id="c0f30-124">Requirement</span></span> | <span data-ttu-id="c0f30-125">值</span><span class="sxs-lookup"><span data-stu-id="c0f30-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f30-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0f30-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c0f30-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0f30-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c0f30-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0f30-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c0f30-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0f30-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c0f30-130">標頭</span><span class="sxs-lookup"><span data-stu-id="c0f30-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0f30-131"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0f30-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0f30-132">Idl</span><span class="sxs-lookup"><span data-stu-id="c0f30-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0f30-133"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0f30-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f30-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0f30-134">See also</span></span>

<dl> <span data-ttu-id="c0f30-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c0f30-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="c0f30-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="c0f30-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





