---
description: 使用者 \_ 驗證方法允許存取使用者驗證服務。
ms.assetid: 110da052-c581-46bc-8e81-5be112ee9b43
title: ISCardAuth：： User_Auth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.User_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae810f93c322449109576b37f01afa4f277fc32f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847935"
---
# <a name="iscardauthuser_auth-method"></a><span data-ttu-id="8c528-103">ISCardAuth：： User \_ Auth 方法</span><span class="sxs-lookup"><span data-stu-id="8c528-103">ISCardAuth::User\_Auth method</span></span>

<span data-ttu-id="8c528-104">\[**使用者 \_ 驗證** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8c528-104">\[The **User\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8c528-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="8c528-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8c528-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8c528-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="8c528-107">使用者驗證方法允許存取使用者驗證服務。 **\_**</span><span class="sxs-lookup"><span data-stu-id="8c528-107">The **User\_Auth** method allows access to user authentication services.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c528-108">語法</span><span class="sxs-lookup"><span data-stu-id="8c528-108">Syntax</span></span>


```C++
HRESULT User_Auth(
  [in] LONG         lAlgorID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="8c528-109">參數</span><span class="sxs-lookup"><span data-stu-id="8c528-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c528-110">*lAlgorID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c528-110">*lAlgorID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c528-111">要在驗證程式中使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="8c528-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8c528-112">*pParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c528-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c528-113">[**IByteBuffer**](ibytebuffer.md)物件，其中包含驗證程式的特定廠商參數。</span><span class="sxs-lookup"><span data-stu-id="8c528-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="8c528-114">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8c528-114">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c528-115">要在驗證程式中使用的資料。</span><span class="sxs-lookup"><span data-stu-id="8c528-115">Data to be used in the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c528-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c528-116">Return value</span></span>

<span data-ttu-id="8c528-117">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="8c528-117">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="8c528-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8c528-118">Return code</span></span>                                                                                   | <span data-ttu-id="8c528-119">Description</span><span class="sxs-lookup"><span data-stu-id="8c528-119">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="8c528-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8c528-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8c528-121">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="8c528-121">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="8c528-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="8c528-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="8c528-123">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="8c528-123">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="8c528-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="8c528-124"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8c528-125">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="8c528-125">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="8c528-126"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8c528-126"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8c528-127">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="8c528-127">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="8c528-128">備註</span><span class="sxs-lookup"><span data-stu-id="8c528-128">Remarks</span></span>

<span data-ttu-id="8c528-129">如需此介面所提供的所有方法清單，請參閱 [**ISCardAuth**](iscardauth.md)。</span><span class="sxs-lookup"><span data-stu-id="8c528-129">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="8c528-130">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8c528-130">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="8c528-131">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="8c528-131">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c528-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c528-132">Requirements</span></span>



| <span data-ttu-id="8c528-133">需求</span><span class="sxs-lookup"><span data-stu-id="8c528-133">Requirement</span></span> | <span data-ttu-id="8c528-134">值</span><span class="sxs-lookup"><span data-stu-id="8c528-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c528-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c528-135">Minimum supported client</span></span><br/> | <span data-ttu-id="8c528-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c528-136">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="8c528-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c528-137">Minimum supported server</span></span><br/> | <span data-ttu-id="8c528-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c528-138">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="8c528-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8c528-139">End of client support</span></span><br/>    | <span data-ttu-id="8c528-140">Windows XP</span><span class="sxs-lookup"><span data-stu-id="8c528-140">Windows XP</span></span><br/>                                |
| <span data-ttu-id="8c528-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8c528-141">End of server support</span></span><br/>    | <span data-ttu-id="8c528-142">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8c528-142">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="8c528-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c528-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c528-144">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="8c528-144">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="8c528-145">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="8c528-145">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
