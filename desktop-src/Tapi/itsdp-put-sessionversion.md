---
description: Put \_ SessionVersion 方法會設定會話版本。
ms.assetid: 8984d608-0fad-4979-9c58-ac2fb7926796
title: 'ITSdp：:p ut_SessionVersion 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a096117f894a2ff33f127c683b84ba50e88308e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991223"
---
# <a name="itsdpput_sessionversion-method"></a><span data-ttu-id="2f886-103">ITSdp：:p 的 \_ SessionVersion 方法</span><span class="sxs-lookup"><span data-stu-id="2f886-103">ITSdp::put\_SessionVersion method</span></span>

<span data-ttu-id="2f886-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="2f886-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f886-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="2f886-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2f886-106">**Put \_ SessionVersion** 方法會設定會話版本。</span><span class="sxs-lookup"><span data-stu-id="2f886-106">The **put\_SessionVersion** method sets the session version.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f886-107">語法</span><span class="sxs-lookup"><span data-stu-id="2f886-107">Syntax</span></span>


```C++
HRESULT put_SessionVersion(
  [in] DOUBLE SessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="2f886-108">參數</span><span class="sxs-lookup"><span data-stu-id="2f886-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f886-109">*SessionVersion* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f886-109">*SessionVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f886-110">會話版本值。</span><span class="sxs-lookup"><span data-stu-id="2f886-110">Session version value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f886-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f886-111">Return value</span></span>

<span data-ttu-id="2f886-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2f886-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2f886-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2f886-113">Return code</span></span>                                                                                   | <span data-ttu-id="2f886-114">Description</span><span class="sxs-lookup"><span data-stu-id="2f886-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2f886-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2f886-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="2f886-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2f886-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2f886-118">*SessionVersion* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="2f886-118">The *SessionVersion* parameter is not valid.</span></span><br/>         |
| <dl> <span data-ttu-id="2f886-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2f886-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="2f886-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2f886-121"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2f886-122">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="2f886-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2f886-123"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2f886-124">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="2f886-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2f886-125">備註</span><span class="sxs-lookup"><span data-stu-id="2f886-125">Remarks</span></span>

<span data-ttu-id="2f886-126">這個方法的傳回值可以是 **ulong**，但是 Visual Basic 不支援 **ulong** 型別。</span><span class="sxs-lookup"><span data-stu-id="2f886-126">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="2f886-127">**DOUBLE** 是下一個最小的型別，其中包含所需的整個值範圍。</span><span class="sxs-lookup"><span data-stu-id="2f886-127">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

<span data-ttu-id="2f886-128">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="2f886-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="2f886-129">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="2f886-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f886-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f886-130">Requirements</span></span>



| <span data-ttu-id="2f886-131">需求</span><span class="sxs-lookup"><span data-stu-id="2f886-131">Requirement</span></span> | <span data-ttu-id="2f886-132">值</span><span class="sxs-lookup"><span data-stu-id="2f886-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f886-133">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="2f886-133">TAPI version</span></span><br/> | <span data-ttu-id="2f886-134">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2f886-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2f886-135">標頭</span><span class="sxs-lookup"><span data-stu-id="2f886-135">Header</span></span><br/>       | <dl> <span data-ttu-id="2f886-136"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f886-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f886-137">Library</span></span><br/>      | <dl> <span data-ttu-id="2f886-138"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2f886-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2f886-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="2f886-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f886-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f886-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f886-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f886-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="2f886-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="2f886-143">**ITSdp：： get \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="2f886-143">**ITSdp::get\_SessionVersion**</span></span>](itsdp-get-sessionversion.md)
</dt> </dl>

 

 




