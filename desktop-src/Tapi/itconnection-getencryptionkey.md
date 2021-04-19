---
description: GetEncryptionKey 方法會取得加密金鑰。
ms.assetid: a80d8660-d13e-483f-b1d7-ee2043ef5cab
title: 'ITConnection：： GetEncryptionKey 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a826dc8424222587f2838804ec035fb23c2e41d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000736"
---
# <a name="itconnectiongetencryptionkey-method"></a><span data-ttu-id="659e7-103">ITConnection：： GetEncryptionKey 方法</span><span class="sxs-lookup"><span data-stu-id="659e7-103">ITConnection::GetEncryptionKey method</span></span>

<span data-ttu-id="659e7-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="659e7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="659e7-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="659e7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="659e7-106">**GetEncryptionKey** 方法會取得加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="659e7-106">The **GetEncryptionKey** method gets the encryption key.</span></span>

## <a name="syntax"></a><span data-ttu-id="659e7-107">語法</span><span class="sxs-lookup"><span data-stu-id="659e7-107">Syntax</span></span>


```C++
HRESULT GetEncryptionKey(
  [out] BSTR         *ppKeyType,
  [out] VARIANT_BOOL *pfValidKeyData,
  [out] BSTR         *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="659e7-108">參數</span><span class="sxs-lookup"><span data-stu-id="659e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="659e7-109">*ppKeyType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="659e7-109">*ppKeyType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659e7-110">包含加密金鑰類型之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="659e7-110">Pointer to a **BSTR** containing the type of encryption key.</span></span>

</dd> <dt>

<span data-ttu-id="659e7-111">*pfValidKeyData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="659e7-111">*pfValidKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659e7-112">指出加密金鑰資料的有效性。</span><span class="sxs-lookup"><span data-stu-id="659e7-112">Indicates validity of encryption key data.</span></span>

</dd> <dt>

<span data-ttu-id="659e7-113">*ppKeyData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="659e7-113">*ppKeyData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="659e7-114">包含加密金鑰資料之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="659e7-114">Pointer to a **BSTR** containing the encryption key data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="659e7-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="659e7-115">Return value</span></span>

<span data-ttu-id="659e7-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="659e7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="659e7-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="659e7-117">Return code</span></span>                                                                                   | <span data-ttu-id="659e7-118">Description</span><span class="sxs-lookup"><span data-stu-id="659e7-118">Description</span></span>                                                                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="659e7-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="659e7-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="659e7-120">Method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="659e7-121"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="659e7-122">*PpKeyType、pfValidKeyData* 或 *ppKeyData* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="659e7-122">The *ppKeyType, pfValidKeyData,* or *ppKeyData* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="659e7-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="659e7-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="659e7-124">Insufficient memory exists to perform the operation.</span></span><br/>                              |
| <dl> <span data-ttu-id="659e7-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="659e7-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="659e7-126">Unspecified error.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="659e7-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="659e7-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="659e7-128">This method is not yet implemented.</span></span><br/>                                               |



 

## <a name="remarks"></a><span data-ttu-id="659e7-129">備註</span><span class="sxs-lookup"><span data-stu-id="659e7-129">Remarks</span></span>

<span data-ttu-id="659e7-130">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppKeyType* 和 *ppKeyData* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="659e7-130">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppKeyType* and *ppKeyData* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="659e7-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="659e7-131">Requirements</span></span>



| <span data-ttu-id="659e7-132">需求</span><span class="sxs-lookup"><span data-stu-id="659e7-132">Requirement</span></span> | <span data-ttu-id="659e7-133">值</span><span class="sxs-lookup"><span data-stu-id="659e7-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="659e7-134">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="659e7-134">TAPI version</span></span><br/> | <span data-ttu-id="659e7-135">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="659e7-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="659e7-136">標頭</span><span class="sxs-lookup"><span data-stu-id="659e7-136">Header</span></span><br/>       | <dl> <span data-ttu-id="659e7-137"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="659e7-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="659e7-138">Library</span></span><br/>      | <dl> <span data-ttu-id="659e7-139"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="659e7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="659e7-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="659e7-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="659e7-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="659e7-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="659e7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="659e7-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="659e7-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

