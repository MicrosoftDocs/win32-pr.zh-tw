---
title: 'INapComponentInfo ConvertErrorCodeToMessageId 方法 (NapCommon .h) '
description: NAP 系統會使用它來要求健康情況用戶端將 HRESULT 錯誤碼轉換成訊息識別碼。
ms.assetid: 760dd039-5b9c-4227-9939-ad6ea23f5b81
keywords:
- ConvertErrorCodeToMessageId 方法 NAP
- ConvertErrorCodeToMessageId 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，ConvertErrorCodeToMessageId 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.ConvertErrorCodeToMessageId
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7ed8eee06ed6bd553ffcce68e76e375dd706238
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466776"
---
# <a name="inapcomponentinfoconverterrorcodetomessageid-method"></a><span data-ttu-id="d7fe1-106">INapComponentInfo：： ConvertErrorCodeToMessageId 方法</span><span class="sxs-lookup"><span data-stu-id="d7fe1-106">INapComponentInfo::ConvertErrorCodeToMessageId method</span></span>

> [!Note]  
> <span data-ttu-id="d7fe1-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="d7fe1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d7fe1-108">**INapComponentInfo：： ConvertErrorCodeToMessageId** 回呼方法是由 NAP 系統用來要求健康情況用戶端將 HRESULT 錯誤碼轉換成訊息識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-108">The **INapComponentInfo::ConvertErrorCodeToMessageId** callback method is used by the NAP System to request the health client convert an HRESULT error code into a message ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7fe1-109">語法</span><span class="sxs-lookup"><span data-stu-id="d7fe1-109">Syntax</span></span>


```C++
HRESULT ConvertErrorCodeToMessageId(
  [in]  HRESULT   errorCode,
  [out] MessageId *msgId
);
```



## <a name="parameters"></a><span data-ttu-id="d7fe1-110">參數</span><span class="sxs-lookup"><span data-stu-id="d7fe1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7fe1-111">*errorCode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7fe1-111">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fe1-112">從 NAP 系統轉換成 **MessageId** 的 [**錯誤碼**](nap-error-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-112">The [**error code**](nap-error-constants.md) from the NAP System that is to be converted into a **MessageId**.</span></span>

</dd> <dt>

<span data-ttu-id="d7fe1-113">*msgId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d7fe1-113">*msgId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7fe1-114">[**MessageId**](nap-datatypes.md)的指標，其中包含對應之當地語系化字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-114">A pointer to a [**MessageId**](nap-datatypes.md) that contains the resource ID of the corresponding localized string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7fe1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7fe1-115">Return value</span></span>

<span data-ttu-id="d7fe1-116">根據此作業的結果傳回這些錯誤碼的其中一個。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="d7fe1-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d7fe1-117">Return code</span></span>                                                                                     | <span data-ttu-id="d7fe1-118">Description</span><span class="sxs-lookup"><span data-stu-id="d7fe1-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7fe1-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe1-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d7fe1-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="d7fe1-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe1-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d7fe1-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d7fe1-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe1-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d7fe1-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7fe1-125">備註</span><span class="sxs-lookup"><span data-stu-id="d7fe1-125">Remarks</span></span>

<span data-ttu-id="d7fe1-126">NAP 系統會使用傳回的 **MessageId** 來取出當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="d7fe1-126">The returned **MessageId** is used by the NAP System to retrieve a localized string.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7fe1-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7fe1-127">Requirements</span></span>



| <span data-ttu-id="d7fe1-128">需求</span><span class="sxs-lookup"><span data-stu-id="d7fe1-128">Requirement</span></span> | <span data-ttu-id="d7fe1-129">值</span><span class="sxs-lookup"><span data-stu-id="d7fe1-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7fe1-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7fe1-130">Minimum supported client</span></span><br/> | <span data-ttu-id="d7fe1-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7fe1-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d7fe1-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7fe1-132">Minimum supported server</span></span><br/> | <span data-ttu-id="d7fe1-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7fe1-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d7fe1-134">標頭</span><span class="sxs-lookup"><span data-stu-id="d7fe1-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7fe1-135"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe1-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d7fe1-136">Idl</span><span class="sxs-lookup"><span data-stu-id="d7fe1-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d7fe1-137"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d7fe1-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7fe1-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7fe1-138">See also</span></span>

<dl> <span data-ttu-id="d7fe1-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d7fe1-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="d7fe1-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="d7fe1-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





