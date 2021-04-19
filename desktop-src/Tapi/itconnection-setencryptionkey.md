---
description: SetEncryptionKey 方法會設定解密會話所需的加密金鑰，或用來取得以外部方式取得可用金鑰之機制的指示。
ms.assetid: 9efcf90e-3645-49f4-b27d-9a8246637310
title: 'ITConnection：： SetEncryptionKey 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d0ce079d3815897c348e553df0af8dece8592b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982977"
---
# <a name="itconnectionsetencryptionkey-method"></a><span data-ttu-id="8a664-103">ITConnection：： SetEncryptionKey 方法</span><span class="sxs-lookup"><span data-stu-id="8a664-103">ITConnection::SetEncryptionKey method</span></span>

<span data-ttu-id="8a664-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="8a664-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8a664-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="8a664-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8a664-106">**SetEncryptionKey** 方法會設定解密會話所需的加密金鑰，或用來取得以外部方式取得可用金鑰之機制的指示。</span><span class="sxs-lookup"><span data-stu-id="8a664-106">The **SetEncryptionKey** method sets the encryption key needed to decrypt the session or an indication to a mechanism to obtain a usable key by external means.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a664-107">語法</span><span class="sxs-lookup"><span data-stu-id="8a664-107">Syntax</span></span>


```C++
HRESULT SetEncryptionKey(
  [in] BSTR pKeyType,
  [in] BSTR *ppKeyData
);
```



## <a name="parameters"></a><span data-ttu-id="8a664-108">參數</span><span class="sxs-lookup"><span data-stu-id="8a664-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a664-109">*pKeyType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a664-109">*pKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a664-110">包含加密金鑰類型之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="8a664-110">Pointer to a **BSTR** containing the encryption key type.</span></span>

</dd> <dt>

<span data-ttu-id="8a664-111">*ppKeyData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a664-111">*ppKeyData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a664-112">包含加密金鑰資訊之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="8a664-112">Pointer to a **BSTR** containing encryption key information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a664-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a664-113">Return value</span></span>

<span data-ttu-id="8a664-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8a664-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8a664-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8a664-115">Return code</span></span>                                                                          | <span data-ttu-id="8a664-116">Description</span><span class="sxs-lookup"><span data-stu-id="8a664-116">Description</span></span>                  |
|--------------------------------------------------------------------------------------|------------------------------|
| <dl> <span data-ttu-id="8a664-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8a664-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a664-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="8a664-118">Method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8a664-119">備註</span><span class="sxs-lookup"><span data-stu-id="8a664-119">Remarks</span></span>

<span data-ttu-id="8a664-120">應用程式必須使用 [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) 來配置 *pKeyType* 和 *ppKeyData* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="8a664-120">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pKeyType* and *ppKeyData* parameters.</span></span> <span data-ttu-id="8a664-121">當不再需要變數時，應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="8a664-121">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variables are no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a664-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a664-122">Requirements</span></span>



| <span data-ttu-id="8a664-123">需求</span><span class="sxs-lookup"><span data-stu-id="8a664-123">Requirement</span></span> | <span data-ttu-id="8a664-124">值</span><span class="sxs-lookup"><span data-stu-id="8a664-124">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a664-125">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8a664-125">TAPI version</span></span><br/> | <span data-ttu-id="8a664-126">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8a664-126">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8a664-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8a664-127">Header</span></span><br/>       | <dl> <span data-ttu-id="8a664-128"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a664-128"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a664-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="8a664-129">Library</span></span><br/>      | <dl> <span data-ttu-id="8a664-130"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="8a664-130"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8a664-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8a664-131">DLL</span></span><br/>          | <dl> <span data-ttu-id="8a664-132"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a664-132"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a664-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a664-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a664-134">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="8a664-134">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

