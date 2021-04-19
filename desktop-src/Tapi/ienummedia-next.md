---
description: 下一個方法會取得列舉順序中的下一個指定元素數目。
ms.assetid: 39c6d082-415f-4375-8cad-6d4c734d277f
title: 'IEnumMedia：： Next 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f04b92220d8fe93058533427ff8cc7bcc7ad7a02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991353"
---
# <a name="ienummedianext-method"></a><span data-ttu-id="94e84-103">IEnumMedia：： Next 方法</span><span class="sxs-lookup"><span data-stu-id="94e84-103">IEnumMedia::Next method</span></span>

<span data-ttu-id="94e84-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="94e84-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94e84-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="94e84-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="94e84-106">**下一個** 方法會取得列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="94e84-106">The **Next** method gets the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e84-107">語法</span><span class="sxs-lookup"><span data-stu-id="94e84-107">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG   celt,
  [out] ITMedia **pVal,
  [out] ULONG   *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="94e84-108">參數</span><span class="sxs-lookup"><span data-stu-id="94e84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94e84-109">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94e84-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94e84-110">要求的元素數目。</span><span class="sxs-lookup"><span data-stu-id="94e84-110">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="94e84-111">*pVal* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94e84-111">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94e84-112">[**ITMedia**](itmedia.md)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="94e84-112">Pointer to the [**ITMedia**](itmedia.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="94e84-113">*pceltFetched* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="94e84-113">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94e84-114">實際提供專案數目的指標。</span><span class="sxs-lookup"><span data-stu-id="94e84-114">Pointer to the number of elements actually supplied.</span></span> <span data-ttu-id="94e84-115">如果 *celt* 是1，則可能為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="94e84-115">May be **NULL** if *celt* is one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94e84-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="94e84-116">Return value</span></span>

<span data-ttu-id="94e84-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="94e84-117">This method can return one of these values.</span></span>



| <span data-ttu-id="94e84-118">值</span><span class="sxs-lookup"><span data-stu-id="94e84-118">Value</span></span>                                                                                     | <span data-ttu-id="94e84-119">意義</span><span class="sxs-lookup"><span data-stu-id="94e84-119">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="94e84-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="94e84-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="94e84-121">方法傳回 *celt* 元素數目。</span><span class="sxs-lookup"><span data-stu-id="94e84-121">Method returned *celt* number of elements.</span></span><br/>         |
| <dl> <span data-ttu-id="94e84-122"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="94e84-122"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="94e84-123">剩餘的元素數目小於 *celt*。</span><span class="sxs-lookup"><span data-stu-id="94e84-123">Number of elements remaining was less than *celt*.</span></span><br/> |
| <dl> <span data-ttu-id="94e84-124"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="94e84-124"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="94e84-125">*PVal* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="94e84-125">The *pVal* parameter is not a valid pointer.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="94e84-126">備註</span><span class="sxs-lookup"><span data-stu-id="94e84-126">Remarks</span></span>

<span data-ttu-id="94e84-127">TAPI 會呼叫 **IEnumMedia：： Next** 所傳回的 [**ITMedia**](itmedia.md)介面上的 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="94e84-127">TAPI calls the **AddRef** method on the [**ITMedia**](itmedia.md) interface returned by **IEnumMedia::Next**.</span></span> <span data-ttu-id="94e84-128">應用程式必須在 **ITMedia** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="94e84-128">The application must call **Release** on the **ITMedia** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="94e84-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="94e84-129">Requirements</span></span>



| <span data-ttu-id="94e84-130">需求</span><span class="sxs-lookup"><span data-stu-id="94e84-130">Requirement</span></span> | <span data-ttu-id="94e84-131">值</span><span class="sxs-lookup"><span data-stu-id="94e84-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94e84-132">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="94e84-132">TAPI version</span></span><br/> | <span data-ttu-id="94e84-133">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="94e84-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="94e84-134">標頭</span><span class="sxs-lookup"><span data-stu-id="94e84-134">Header</span></span><br/>       | <dl> <span data-ttu-id="94e84-135"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="94e84-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="94e84-136">程式庫</span><span class="sxs-lookup"><span data-stu-id="94e84-136">Library</span></span><br/>      | <dl> <span data-ttu-id="94e84-137"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="94e84-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="94e84-138">DLL</span><span class="sxs-lookup"><span data-stu-id="94e84-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="94e84-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94e84-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e84-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94e84-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e84-141">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="94e84-141">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




