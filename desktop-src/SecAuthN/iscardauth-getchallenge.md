---
description: GetChallenge 方法會從智慧卡傳回挑戰。
ms.assetid: a114ebfd-831f-4c6b-8156-ce631a732c9b
title: ISCardAuth：： GetChallenge 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.GetChallenge
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9282c0a922a1f8c8daff07c31dcafa7e47e923a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191853"
---
# <a name="iscardauthgetchallenge-method"></a><span data-ttu-id="cafec-103">ISCardAuth：： GetChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="cafec-103">ISCardAuth::GetChallenge method</span></span>

<span data-ttu-id="cafec-104">\[**GetChallenge** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="cafec-104">\[The **GetChallenge** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cafec-105">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="cafec-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cafec-106">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="cafec-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cafec-107">**GetChallenge** 方法會從 [*智慧卡*](../secgloss/s-gly.md)傳回挑戰。</span><span class="sxs-lookup"><span data-stu-id="cafec-107">The **GetChallenge** method returns a challenge from the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cafec-108">語法</span><span class="sxs-lookup"><span data-stu-id="cafec-108">Syntax</span></span>


```C++
HRESULT GetChallenge(
  [in, optional] LONG         lAlgoID,
  [in]           LONG         lLengthOfChallenge,
  [in]           LPBYTEBUFFER pParam,
  [in, out]      LPBYTEBUFFER *pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="cafec-109">參數</span><span class="sxs-lookup"><span data-stu-id="cafec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cafec-110">*lAlgoID* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="cafec-110">*lAlgoID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cafec-111">要在驗證程式中使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="cafec-111">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="cafec-112">*lLengthOfChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cafec-112">*lLengthOfChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cafec-113">預期回應的最大長度。</span><span class="sxs-lookup"><span data-stu-id="cafec-113">Maximum length of expected response.</span></span>

</dd> <dt>

<span data-ttu-id="cafec-114">*pParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cafec-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cafec-115">[**IByteBuffer**](ibytebuffer.md)物件，其中包含驗證程式的特定廠商參數。</span><span class="sxs-lookup"><span data-stu-id="cafec-115">An [**IByteBuffer**](ibytebuffer.md) object containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="cafec-116">*pBuffer* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="cafec-116">*pBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cafec-117">在輸入時，指向緩衝區。</span><span class="sxs-lookup"><span data-stu-id="cafec-117">On input, points to the buffer.</span></span>

<span data-ttu-id="cafec-118">在輸出時，會包含來自卡片的挑戰資料。</span><span class="sxs-lookup"><span data-stu-id="cafec-118">On output, contains the challenge data from the card.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cafec-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="cafec-119">Return value</span></span>

<span data-ttu-id="cafec-120">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="cafec-120">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cafec-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cafec-121">Return code</span></span>                                                                                   | <span data-ttu-id="cafec-122">Description</span><span class="sxs-lookup"><span data-stu-id="cafec-122">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="cafec-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cafec-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cafec-124">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="cafec-124">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cafec-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cafec-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cafec-126">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="cafec-126">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="cafec-127"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="cafec-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cafec-128">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="cafec-128">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="cafec-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cafec-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cafec-130">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="cafec-130">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="cafec-131">備註</span><span class="sxs-lookup"><span data-stu-id="cafec-131">Remarks</span></span>

<span data-ttu-id="cafec-132">如需此介面所提供的所有方法清單，請參閱 [**ISCardAuth**](iscardauth.md)。</span><span class="sxs-lookup"><span data-stu-id="cafec-132">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="cafec-133">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="cafec-133">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cafec-134">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="cafec-134">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cafec-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="cafec-135">Requirements</span></span>



| <span data-ttu-id="cafec-136">需求</span><span class="sxs-lookup"><span data-stu-id="cafec-136">Requirement</span></span> | <span data-ttu-id="cafec-137">值</span><span class="sxs-lookup"><span data-stu-id="cafec-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cafec-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cafec-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cafec-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cafec-139">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="cafec-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cafec-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cafec-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cafec-141">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="cafec-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cafec-142">End of client support</span></span><br/>    | <span data-ttu-id="cafec-143">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cafec-143">Windows XP</span></span><br/>                                |
| <span data-ttu-id="cafec-144">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="cafec-144">End of server support</span></span><br/>    | <span data-ttu-id="cafec-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cafec-145">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="cafec-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cafec-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cafec-147">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="cafec-147">**ISCardAuth**</span></span>](iscardauth.md)
</dt> </dl>

 

 
