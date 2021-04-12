---
title: 'INapComponentInfo GetLocalizedString 方法 (NapCommon .h) '
description: NAP 系統會使用它來取得當地語系化的字串。
ms.assetid: ad5be180-6329-4c91-b4d1-871a4d83c323
keywords:
- GetLocalizedString 方法 NAP
- GetLocalizedString 方法 NAP，INapComponentInfo 介面
- INapComponentInfo 介面 NAP，GetLocalizedString 方法
topic_type:
- apiref
api_name:
- INapComponentInfo.GetLocalizedString
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 781e4e8c93f58039c72a98f40a529243e5722d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935140"
---
# <a name="inapcomponentinfogetlocalizedstring-method"></a><span data-ttu-id="0587d-106">INapComponentInfo：： GetLocalizedString 方法</span><span class="sxs-lookup"><span data-stu-id="0587d-106">INapComponentInfo::GetLocalizedString method</span></span>

> [!Note]  
> <span data-ttu-id="0587d-107">從 Windows 10 開始，無法使用網路存取保護平臺</span><span class="sxs-lookup"><span data-stu-id="0587d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="0587d-108">**INapComponentInfo：： GetLocalizedString** 回呼方法是由 NAP 系統用來取得當地語系化的字串。</span><span class="sxs-lookup"><span data-stu-id="0587d-108">The **INapComponentInfo::GetLocalizedString** callback method is used by the NAP System to get localized strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="0587d-109">語法</span><span class="sxs-lookup"><span data-stu-id="0587d-109">Syntax</span></span>


```C++
HRESULT GetLocalizedString(
  [in]  MessageId     msgId,
  [out] CountedString **string
);
```



## <a name="parameters"></a><span data-ttu-id="0587d-110">參數</span><span class="sxs-lookup"><span data-stu-id="0587d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0587d-111">*msgId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0587d-111">*msgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0587d-112">[**MessageId**](nap-datatypes.md) ，其中包含要當地語系化之字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="0587d-112">A [**MessageId**](nap-datatypes.md) that contains the resource ID of the string to localize.</span></span>

</dd> <dt>

<span data-ttu-id="0587d-113">*字串* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0587d-113">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0587d-114">指向 [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) 的指標，其中包含當地語系化的訊息版本。</span><span class="sxs-lookup"><span data-stu-id="0587d-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) that contains the localized version of the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0587d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="0587d-115">Return value</span></span>

<span data-ttu-id="0587d-116">根據此作業的結果傳回這些錯誤碼的其中一個。</span><span class="sxs-lookup"><span data-stu-id="0587d-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="0587d-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0587d-117">Return code</span></span>                                                                                     | <span data-ttu-id="0587d-118">Description</span><span class="sxs-lookup"><span data-stu-id="0587d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="0587d-119"><dt>**S \_確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0587d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="0587d-120">作業成功。</span><span class="sxs-lookup"><span data-stu-id="0587d-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="0587d-121"><dt>**E \_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="0587d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="0587d-122">許可權錯誤，拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="0587d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="0587d-123"><dt>**E \_OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="0587d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="0587d-124">系統資源限制，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="0587d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0587d-125">備註</span><span class="sxs-lookup"><span data-stu-id="0587d-125">Remarks</span></span>

<span data-ttu-id="0587d-126">字串應根據呼叫執行緒的語言識別項進行當地語系化。</span><span class="sxs-lookup"><span data-stu-id="0587d-126">Strings should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="0587d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0587d-127">Requirements</span></span>



| <span data-ttu-id="0587d-128">需求</span><span class="sxs-lookup"><span data-stu-id="0587d-128">Requirement</span></span> | <span data-ttu-id="0587d-129">值</span><span class="sxs-lookup"><span data-stu-id="0587d-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0587d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0587d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="0587d-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0587d-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0587d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0587d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="0587d-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0587d-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0587d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="0587d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="0587d-135"><dt>NapCommon。h</dt></span><span class="sxs-lookup"><span data-stu-id="0587d-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="0587d-136">Idl</span><span class="sxs-lookup"><span data-stu-id="0587d-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0587d-137"><dt>NapCommon .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0587d-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0587d-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0587d-138">See also</span></span>

<dl> <span data-ttu-id="0587d-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0587d-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="0587d-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="0587d-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





