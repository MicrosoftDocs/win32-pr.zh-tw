---
description: SetPortInfo 方法會設定第一個埠的16位埠值，以及會話所需的埠數目。
ms.assetid: 4726b39b-cd10-4630-8f38-8671db4f432b
title: 'ITMedia：： SetPortInfo 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c605c1768316871f6c3c9ec10f991f21c1643794
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995073"
---
# <a name="itmediasetportinfo-method"></a><span data-ttu-id="6a8e4-103">ITMedia：： SetPortInfo 方法</span><span class="sxs-lookup"><span data-stu-id="6a8e4-103">ITMedia::SetPortInfo method</span></span>

<span data-ttu-id="6a8e4-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="6a8e4-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="6a8e4-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="6a8e4-106">**SetPortInfo** 方法會設定第一個埠的16位埠值，以及會話所需的埠數目。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-106">The **SetPortInfo** method sets the 16-bit port value for the first port and the number of ports needed for a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a8e4-107">語法</span><span class="sxs-lookup"><span data-stu-id="6a8e4-107">Syntax</span></span>


```C++
HRESULT SetPortInfo(
  [in] LONG StartPort,
  [in] LONG NumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="6a8e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="6a8e4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a8e4-109">*StartPort* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a8e4-109">*StartPort* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8e4-110">啟動埠。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-110">Starting port.</span></span> <span data-ttu-id="6a8e4-111">這可以是範圍0-65535 中的值。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-111">This can be a value in the range 0-65535.</span></span>

</dd> <dt>

<span data-ttu-id="6a8e4-112">*NumPorts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6a8e4-112">*NumPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a8e4-113">埠數目。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-113">Number of ports.</span></span> <span data-ttu-id="6a8e4-114">這可以是範圍0-65535 中的值。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-114">This can be a value in the range 0-65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a8e4-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a8e4-115">Return value</span></span>

<span data-ttu-id="6a8e4-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-116">This method can return one of these values.</span></span>



| <span data-ttu-id="6a8e4-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a8e4-117">Return code</span></span>                                                                                   | <span data-ttu-id="6a8e4-118">Description</span><span class="sxs-lookup"><span data-stu-id="6a8e4-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="6a8e4-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="6a8e4-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6a8e4-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="6a8e4-122">*StartPort 或 NumPorts* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-122">The *StartPort or NumPorts* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="6a8e4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="6a8e4-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6a8e4-125"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="6a8e4-126">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="6a8e4-127"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="6a8e4-128">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="6a8e4-129">備註</span><span class="sxs-lookup"><span data-stu-id="6a8e4-129">Remarks</span></span>

<span data-ttu-id="6a8e4-130">此函式可能會以未加密的形式，在網路上傳送資料。因此，在網路上竊聽的人可以讀取資料。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-130">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="6a8e4-131">使用這個方法之前，請先考慮以純文字傳送資料的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="6a8e4-131">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a8e4-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="6a8e4-132">Requirements</span></span>



| <span data-ttu-id="6a8e4-133">需求</span><span class="sxs-lookup"><span data-stu-id="6a8e4-133">Requirement</span></span> | <span data-ttu-id="6a8e4-134">值</span><span class="sxs-lookup"><span data-stu-id="6a8e4-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a8e4-135">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6a8e4-135">TAPI version</span></span><br/> | <span data-ttu-id="6a8e4-136">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6a8e4-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="6a8e4-137">標頭</span><span class="sxs-lookup"><span data-stu-id="6a8e4-137">Header</span></span><br/>       | <dl> <span data-ttu-id="6a8e4-138"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="6a8e4-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="6a8e4-139">Library</span></span><br/>      | <dl> <span data-ttu-id="6a8e4-140"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="6a8e4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6a8e4-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="6a8e4-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a8e4-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a8e4-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a8e4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a8e4-144">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="6a8e4-144">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




