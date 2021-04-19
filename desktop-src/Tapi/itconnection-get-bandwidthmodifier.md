---
description: Get \_ BandwidthModifier 方法會取得頻寬修飾詞，這是單一的英數位元，可提供頻寬圖的意義。 定義的兩個修飾詞為 CT (會議總計) 和 (應用程式特定的最大) 。
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'ITConnection：： get_BandwidthModifier 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981111"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a><span data-ttu-id="e24a0-104">ITConnection：： get \_ BandwidthModifier 方法</span><span class="sxs-lookup"><span data-stu-id="e24a0-104">ITConnection::get\_BandwidthModifier method</span></span>

<span data-ttu-id="e24a0-105">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="e24a0-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e24a0-106">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="e24a0-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e24a0-107">**Get \_ BandwidthModifier** 方法會取得頻寬修飾詞，這是單一的英數位元，可提供頻寬圖的意義。</span><span class="sxs-lookup"><span data-stu-id="e24a0-107">The **get\_BandwidthModifier** method gets the bandwidth modifier, which is a single, alphanumeric word giving the meaning of the bandwidth figure.</span></span> <span data-ttu-id="e24a0-108">定義的兩個修飾詞為 CT (會議總計) 和 (應用程式特定的最大) 。</span><span class="sxs-lookup"><span data-stu-id="e24a0-108">The two modifiers defined are CT (Conference Total) and AS (Application Specific Maximum).</span></span>

## <a name="syntax"></a><span data-ttu-id="e24a0-109">語法</span><span class="sxs-lookup"><span data-stu-id="e24a0-109">Syntax</span></span>


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a><span data-ttu-id="e24a0-110">參數</span><span class="sxs-lookup"><span data-stu-id="e24a0-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e24a0-111">*ppModifier* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e24a0-111">*ppModifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e24a0-112">包含頻寬修飾詞之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="e24a0-112">Pointer to a **BSTR** containing the bandwidth modifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e24a0-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="e24a0-113">Return value</span></span>

<span data-ttu-id="e24a0-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e24a0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e24a0-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e24a0-115">Return code</span></span>                                                                                   | <span data-ttu-id="e24a0-116">Description</span><span class="sxs-lookup"><span data-stu-id="e24a0-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="e24a0-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e24a0-118">方法成功。</span><span class="sxs-lookup"><span data-stu-id="e24a0-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="e24a0-119"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e24a0-120">*PpModifier* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="e24a0-120">The *ppModifier* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="e24a0-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e24a0-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="e24a0-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="e24a0-123"><dt>**E \_ 失敗**</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="e24a0-124">未指定的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e24a0-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="e24a0-125"><dt>**E \_ >NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e24a0-126">尚未實作這個方法。</span><span class="sxs-lookup"><span data-stu-id="e24a0-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="e24a0-127">備註</span><span class="sxs-lookup"><span data-stu-id="e24a0-127">Remarks</span></span>

<span data-ttu-id="e24a0-128">應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppModifier* 參數的記憶體。</span><span class="sxs-lookup"><span data-stu-id="e24a0-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppModifier* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e24a0-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="e24a0-129">Requirements</span></span>



| <span data-ttu-id="e24a0-130">需求</span><span class="sxs-lookup"><span data-stu-id="e24a0-130">Requirement</span></span> | <span data-ttu-id="e24a0-131">值</span><span class="sxs-lookup"><span data-stu-id="e24a0-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e24a0-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e24a0-132">TAPI version</span></span><br/> | <span data-ttu-id="e24a0-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e24a0-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="e24a0-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e24a0-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e24a0-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="e24a0-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="e24a0-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e24a0-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="e24a0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e24a0-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e24a0-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e24a0-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e24a0-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e24a0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e24a0-141">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="e24a0-141">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

