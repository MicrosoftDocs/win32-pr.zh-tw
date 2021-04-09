---
description: 應用 \_ 程式驗證方法會驗證應用程式。 它可讓應用程式在智慧卡要求驗證時，使用挑戰/簽章通訊協定) 驗證自己 (。
ms.assetid: 0b86ce09-ca17-4d74-bc14-46b17262e669
title: ISCardAuth：： APP_Auth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardAuth.APP_Auth
api_type:
- COM
api_location: ''
ms.openlocfilehash: 792cd1b43a43f020e62e87048741935a82da28dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848498"
---
# <a name="iscardauthapp_auth-method"></a><span data-ttu-id="51589-104">ISCardAuth：： APP \_ Auth 方法</span><span class="sxs-lookup"><span data-stu-id="51589-104">ISCardAuth::APP\_Auth method</span></span>

<span data-ttu-id="51589-105">\[**應用程式 \_ 驗證** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="51589-105">\[The **APP\_Auth** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="51589-106">它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="51589-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="51589-107">[智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="51589-107">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="51589-108">應用 **程式 \_ 驗證** 方法會驗證應用程式。</span><span class="sxs-lookup"><span data-stu-id="51589-108">The **APP\_Auth** method authenticates the application.</span></span> <span data-ttu-id="51589-109">它可讓應用程式在 [*智慧卡*](../secgloss/s-gly.md)要求驗證時，使用挑戰/簽章通訊協定) 驗證自己 (。</span><span class="sxs-lookup"><span data-stu-id="51589-109">It allows an application to authenticate itself (using a challenge/signature protocol) when authentication is requested by a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="51589-110">語法</span><span class="sxs-lookup"><span data-stu-id="51589-110">Syntax</span></span>


```C++
HRESULT APP_Auth(
  [in] LONG         lAlgoID,
  [in] LPBYTEBUFFER pParam,
  [in] LPBYTEBUFFER pBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="51589-111">參數</span><span class="sxs-lookup"><span data-stu-id="51589-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51589-112">*lAlgoID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51589-112">*lAlgoID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51589-113">要在驗證程式中使用的演算法。</span><span class="sxs-lookup"><span data-stu-id="51589-113">Algorithm to be used in the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="51589-114">*pParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51589-114">*pParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51589-115">[**IByteBuffer**](ibytebuffer.md) ，其中包含驗證程式的特定廠商參數。</span><span class="sxs-lookup"><span data-stu-id="51589-115">An [**IByteBuffer**](ibytebuffer.md) containing vendor-specific parameters of the authentication process.</span></span>

</dd> <dt>

<span data-ttu-id="51589-116">*pBuffer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="51589-116">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51589-117">計算所需的資料。</span><span class="sxs-lookup"><span data-stu-id="51589-117">Data required for the calculation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51589-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="51589-118">Return value</span></span>

<span data-ttu-id="51589-119">方法會傳回下列其中一個可能的值。</span><span class="sxs-lookup"><span data-stu-id="51589-119">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="51589-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="51589-120">Return code</span></span>                                                                                   | <span data-ttu-id="51589-121">Description</span><span class="sxs-lookup"><span data-stu-id="51589-121">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="51589-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="51589-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="51589-123">作業順利完成。</span><span class="sxs-lookup"><span data-stu-id="51589-123">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="51589-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="51589-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="51589-125">無效的參數。</span><span class="sxs-lookup"><span data-stu-id="51589-125">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="51589-126"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="51589-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="51589-127">傳入了錯誤指標。</span><span class="sxs-lookup"><span data-stu-id="51589-127">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="51589-128"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="51589-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="51589-129">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="51589-129">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="51589-130">備註</span><span class="sxs-lookup"><span data-stu-id="51589-130">Remarks</span></span>

<span data-ttu-id="51589-131">如需此介面所提供的所有方法清單，請參閱 [**ISCardAuth**](iscardauth.md)。</span><span class="sxs-lookup"><span data-stu-id="51589-131">For a list of all the methods provided by this interface, see [**ISCardAuth**](iscardauth.md).</span></span>

<span data-ttu-id="51589-132">除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="51589-132">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="51589-133">如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。</span><span class="sxs-lookup"><span data-stu-id="51589-133">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51589-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="51589-134">Requirements</span></span>



| <span data-ttu-id="51589-135">需求</span><span class="sxs-lookup"><span data-stu-id="51589-135">Requirement</span></span> | <span data-ttu-id="51589-136">值</span><span class="sxs-lookup"><span data-stu-id="51589-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51589-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51589-137">Minimum supported client</span></span><br/> | <span data-ttu-id="51589-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51589-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="51589-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51589-139">Minimum supported server</span></span><br/> | <span data-ttu-id="51589-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51589-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51589-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="51589-141">End of client support</span></span><br/>    | <span data-ttu-id="51589-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="51589-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="51589-143">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="51589-143">End of server support</span></span><br/>    | <span data-ttu-id="51589-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="51589-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="51589-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51589-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51589-146">**ISCardAuth**</span><span class="sxs-lookup"><span data-stu-id="51589-146">**ISCardAuth**</span></span>](iscardauth.md)
</dt> <dt>

[<span data-ttu-id="51589-147">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="51589-147">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> </dl>

 

 
