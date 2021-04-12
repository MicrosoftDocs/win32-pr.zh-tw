---
title: 'INapComponentInfo GetVersion 方法 (NapCommon .h) '
description: NAP 系統會使用它來取得健全狀況用戶端的版本。
ms.assetid: aabd13d9-d2ad-4554-a9f6-7845e6775ccd
keywords:
- GetVersion 方法 NAP
- GetVersion 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetVersion 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetVersion
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa1d62c22acf778430bfc2f9dc0e969887c7b306
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509457"
---
# <a name="inapcomponentinfogetversion-method"></a><span data-ttu-id="f6102-106">INapComponentInfo：： GetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="f6102-106">INapComponentInfo::GetVersion method</span></span>

> [!Note]  
> <span data-ttu-id="f6102-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="f6102-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="f6102-108">**INapComponentInfo：： GetVersion** 回呼方法是由 NAP 系統用來取得健全狀況用戶端的版本。</span><span class="sxs-lookup"><span data-stu-id="f6102-108">The **INapComponentInfo::GetVersion** callback method is used by the NAP System to get the version of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6102-109">語法</span><span class="sxs-lookup"><span data-stu-id="f6102-109">Syntax</span></span>


```C++
HRESULT GetVersion(
  [out] MessageId *version
);
```



## <a name="parameters"></a><span data-ttu-id="f6102-110">參數</span><span class="sxs-lookup"><span data-stu-id="f6102-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6102-111">*版本* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f6102-111">*version* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f6102-112">[**MessageId**](nap-datatypes.md)的指標，其中包含版本的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6102-112">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6102-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f6102-113">Return value</span></span>

<span data-ttu-id="f6102-114">根據此作業的結果傳回這些錯誤碼的其中一個。</span><span class="sxs-lookup"><span data-stu-id="f6102-114">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="f6102-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f6102-115">Return code</span></span>                                                                                     | <span data-ttu-id="f6102-116">Description</span><span class="sxs-lookup"><span data-stu-id="f6102-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="f6102-117"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f6102-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="f6102-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f6102-118">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="f6102-119"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="f6102-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="f6102-120">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="f6102-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="f6102-121"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="f6102-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="f6102-122">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="f6102-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f6102-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6102-123">Requirements</span></span>



| <span data-ttu-id="f6102-124">需求</span><span class="sxs-lookup"><span data-stu-id="f6102-124">Requirement</span></span> | <span data-ttu-id="f6102-125">值</span><span class="sxs-lookup"><span data-stu-id="f6102-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6102-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6102-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f6102-127">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6102-127">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f6102-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6102-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f6102-129">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6102-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f6102-130">標頭</span><span class="sxs-lookup"><span data-stu-id="f6102-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6102-131"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6102-131"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="f6102-132">Idl</span><span class="sxs-lookup"><span data-stu-id="f6102-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f6102-133"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f6102-133"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6102-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6102-134">See also</span></span>

<dl> <span data-ttu-id="f6102-135"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f6102-135"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="f6102-136">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="f6102-136">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





