---
description: ICC \_ 驗證方法可讓應用程式驗證智慧卡。
ms.assetid: 98aea241-6bdc-4f47-b56c-a90f69fcd9a4
title: ISCardAuth：： ICC_Auth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.ICC_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 015b5c395f025abea4ab2dc756c03691bbc27e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943372"
---
# <a name="iscardauthicc_auth-method"></a><span data-ttu-id="19304-103">ISCardAuth：： ICC \_ 驗證方法</span><span class="sxs-lookup"><span data-stu-id="19304-103">ISCardAuth::ICC\_Auth method</span></span>

<span data-ttu-id="19304-104">\[您可以在 [需求] 區段中指定的作業系統中使用「 **ICC \_ 驗證** 」方法。</span><span class="sxs-lookup"><span data-stu-id="19304-104">\[The **ICC\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="19304-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="19304-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="19304-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="19304-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="19304-107">**ICC \_ 驗證** 方法可讓應用程式驗證智慧卡。</span><span class="sxs-lookup"><span data-stu-id="19304-107">The **ICC\_Auth** method allows an application to authenticate the smart card.</span></span>

## <a name="syntax"></a><span data-ttu-id="19304-108">語法</span><span class="sxs-lookup"><span data-stu-id="19304-108">Syntax</span></span>


```C++
HRESULT ICC_Auth(
  [in]      LONG         lAlgoID,
  [in]      LPBYTEBUFFER pParam,
  [in, out] LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="19304-109">參數</span><span class="sxs-lookup"><span data-stu-id="19304-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19304-110">*lAlgoID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19304-110">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19304-111">要在驗證程式中使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="19304-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="19304-112">*pParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19304-112">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19304-113">[**IByteBuffer**](ibytebuffer.md)物件，其中包含驗證程式的特定廠商參數。</span><span class="sxs-lookup"><span data-stu-id="19304-113">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="19304-114">*pBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="19304-114">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="19304-115">在輸入時，包含要在驗證程式中使用的資料。</span><span class="sxs-lookup"><span data-stu-id="19304-115">On input, contains data to be used in the authentication process.</span></span>

<span data-ttu-id="19304-116">在輸出時包含驗證程式的結果。</span><span class="sxs-lookup"><span data-stu-id="19304-116">On output, contains the result of the authentication process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19304-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="19304-117">Return value</span></span>

<span data-ttu-id="19304-118">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="19304-118">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="19304-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="19304-119">Return code</span></span>                                                                                   | <span data-ttu-id="19304-120">Description</span><span class="sxs-lookup"><span data-stu-id="19304-120">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="19304-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="19304-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="19304-122">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="19304-122">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="19304-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="19304-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="19304-124">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="19304-124">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="19304-125"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="19304-125"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="19304-126">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="19304-126">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="19304-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="19304-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="19304-128">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="19304-128">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="19304-129">備註</span><span class="sxs-lookup"><span data-stu-id="19304-129">Remarks</span></span>

<span data-ttu-id="19304-130">如需此介面所提供的所有方法清單，請參閱 [**ISCardAuth**](iscardauth.md)。</span><span class="sxs-lookup"><span data-stu-id="19304-130">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="19304-131">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="19304-131">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="19304-132">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="19304-132">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="19304-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="19304-133">Requirements</span></span>



| <span data-ttu-id="19304-134">需求</span><span class="sxs-lookup"><span data-stu-id="19304-134">Requirement</span></span> | <span data-ttu-id="19304-135">值</span><span class="sxs-lookup"><span data-stu-id="19304-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="19304-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19304-136">Minimum supported client</span></span><br/> | <span data-ttu-id="19304-137">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19304-137">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="19304-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19304-138">Minimum supported server</span></span><br/> | <span data-ttu-id="19304-139">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19304-139">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="19304-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="19304-140">End of client support</span></span><br/>    | <span data-ttu-id="19304-141">Windows XP</span><span class="sxs-lookup"><span data-stu-id="19304-141">Windows XP</span></span><br/>                                |
| <span data-ttu-id="19304-142">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="19304-142">End of server support</span></span><br/>    | <span data-ttu-id="19304-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="19304-143">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="19304-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19304-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19304-145">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="19304-145">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
