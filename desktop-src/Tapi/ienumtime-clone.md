---
description: Clone 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'IEnumTime：： Clone 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a030fcd90006047e35d9f661f2878dfbc42c112
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996263"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="19e02-103">IEnumTime：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="19e02-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="19e02-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="19e02-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="19e02-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="19e02-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="19e02-106">**Clone** 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。</span><span class="sxs-lookup"><span data-stu-id="19e02-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="19e02-107">語法</span><span class="sxs-lookup"><span data-stu-id="19e02-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="19e02-108">參數</span><span class="sxs-lookup"><span data-stu-id="19e02-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19e02-109">*ppEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19e02-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19e02-110">新 [**IEnumTime**](ienumtime.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="19e02-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19e02-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="19e02-111">Return value</span></span>

<span data-ttu-id="19e02-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="19e02-112">This method can return one of these values.</span></span>



| <span data-ttu-id="19e02-113">值</span><span class="sxs-lookup"><span data-stu-id="19e02-113">Value</span></span>                                                                                         | <span data-ttu-id="19e02-114">意義</span><span class="sxs-lookup"><span data-stu-id="19e02-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="19e02-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="19e02-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="19e02-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="19e02-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="19e02-118">*PpEnum* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="19e02-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="19e02-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="19e02-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="19e02-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="19e02-121"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="19e02-122">因不明原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="19e02-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="19e02-123">備註</span><span class="sxs-lookup"><span data-stu-id="19e02-123">Remarks</span></span>

<span data-ttu-id="19e02-124">TAPI 會在 **IEnumTime：： Clone** 所傳回的 [**IEnumTime**](ienumtime.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="19e02-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="19e02-125">應用程式必須在 **IEnumTime** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="19e02-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="19e02-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="19e02-126">Requirements</span></span>



| <span data-ttu-id="19e02-127">需求</span><span class="sxs-lookup"><span data-stu-id="19e02-127">Requirement</span></span> | <span data-ttu-id="19e02-128">值</span><span class="sxs-lookup"><span data-stu-id="19e02-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19e02-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="19e02-129">TAPI version</span></span><br/> | <span data-ttu-id="19e02-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="19e02-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="19e02-131">標頭</span><span class="sxs-lookup"><span data-stu-id="19e02-131">Header</span></span><br/>       | <dl> <span data-ttu-id="19e02-132"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="19e02-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="19e02-133">Library</span></span><br/>      | <dl> <span data-ttu-id="19e02-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="19e02-135">DLL</span><span class="sxs-lookup"><span data-stu-id="19e02-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="19e02-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19e02-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19e02-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19e02-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19e02-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="19e02-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




