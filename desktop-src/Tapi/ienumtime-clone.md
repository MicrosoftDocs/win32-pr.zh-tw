---
description: IEnumTime：： Clone 方法： Clone 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。
ms.assetid: 0e9973de-d179-4a2d-a9bd-6d5f2523da52
title: 'IEnumTime：： Clone 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406dac1fad611ee5d3cb6c8b6ef32dfdb62cc963
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090736"
---
# <a name="ienumtimeclone-method"></a><span data-ttu-id="1f690-103">IEnumTime：： Clone 方法</span><span class="sxs-lookup"><span data-stu-id="1f690-103">IEnumTime::Clone method</span></span>

<span data-ttu-id="1f690-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="1f690-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1f690-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="1f690-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1f690-106">**Clone** 方法會建立另一個列舉值，其中包含與目前相同的列舉狀態。</span><span class="sxs-lookup"><span data-stu-id="1f690-106">The **Clone** method creates another enumerator that contains the same enumeration state as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f690-107">語法</span><span class="sxs-lookup"><span data-stu-id="1f690-107">Syntax</span></span>


```C++
HRESULT Clone(
  [out] IEnumTime **ppEnum
);
```



## <a name="parameters"></a><span data-ttu-id="1f690-108">參數</span><span class="sxs-lookup"><span data-stu-id="1f690-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f690-109">*ppEnum* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1f690-109">*ppEnum* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1f690-110">新 [**IEnumTime**](ienumtime.md) 物件的指標。</span><span class="sxs-lookup"><span data-stu-id="1f690-110">Pointer to the new [**IEnumTime**](ienumtime.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f690-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1f690-111">Return value</span></span>

<span data-ttu-id="1f690-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1f690-112">This method can return one of these values.</span></span>



| <span data-ttu-id="1f690-113">值</span><span class="sxs-lookup"><span data-stu-id="1f690-113">Value</span></span>                                                                                         | <span data-ttu-id="1f690-114">意義</span><span class="sxs-lookup"><span data-stu-id="1f690-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1f690-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1f690-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="1f690-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1f690-117"><dt>**E \_ 指標**</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1f690-118">*PpEnum* 參數不是有效的指標。</span><span class="sxs-lookup"><span data-stu-id="1f690-118">The *ppEnum* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="1f690-119"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1f690-120">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="1f690-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1f690-121"><dt>**E 未 \_ 預期**</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-121"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>  | <span data-ttu-id="1f690-122">因不明原因而失敗。</span><span class="sxs-lookup"><span data-stu-id="1f690-122">Failed for unknown reasons.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="1f690-123">備註</span><span class="sxs-lookup"><span data-stu-id="1f690-123">Remarks</span></span>

<span data-ttu-id="1f690-124">TAPI 會在 **IEnumTime：： Clone** 所傳回的 [**IEnumTime**](ienumtime.md)介面上呼叫 **AddRef** 方法。</span><span class="sxs-lookup"><span data-stu-id="1f690-124">TAPI calls the **AddRef** method on the [**IEnumTime**](ienumtime.md) interface returned by **IEnumTime::Clone**.</span></span> <span data-ttu-id="1f690-125">應用程式必須在 **IEnumTime** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。</span><span class="sxs-lookup"><span data-stu-id="1f690-125">The application must call **Release** on the **IEnumTime** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f690-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f690-126">Requirements</span></span>



| <span data-ttu-id="1f690-127">需求</span><span class="sxs-lookup"><span data-stu-id="1f690-127">Requirement</span></span> | <span data-ttu-id="1f690-128">值</span><span class="sxs-lookup"><span data-stu-id="1f690-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1f690-129">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="1f690-129">TAPI version</span></span><br/> | <span data-ttu-id="1f690-130">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1f690-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1f690-131">標頭</span><span class="sxs-lookup"><span data-stu-id="1f690-131">Header</span></span><br/>       | <dl> <span data-ttu-id="1f690-132"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-132"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f690-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="1f690-133">Library</span></span><br/>      | <dl> <span data-ttu-id="1f690-134"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1f690-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1f690-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="1f690-136"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f690-136"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f690-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f690-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f690-138">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="1f690-138">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




