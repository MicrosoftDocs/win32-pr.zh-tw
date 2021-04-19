---
description: Skip 方法會略過列舉順序中的下一個指定元素數目。
ms.assetid: e4d9c95d-1b68-4af6-beb2-2014074e5089
title: 'IEnumTime：： Skip 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebd157afc51f52a8453c38f8a14702476c46eb9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001117"
---
# <a name="ienumtimeskip-method"></a><span data-ttu-id="c3ab7-103">IEnumTime：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="c3ab7-103">IEnumTime::Skip method</span></span>

<span data-ttu-id="c3ab7-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="c3ab7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c3ab7-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="c3ab7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c3ab7-106">**Skip** 方法會略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="c3ab7-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3ab7-107">語法</span><span class="sxs-lookup"><span data-stu-id="c3ab7-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="c3ab7-108">參數</span><span class="sxs-lookup"><span data-stu-id="c3ab7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3ab7-109">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c3ab7-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3ab7-110">要略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c3ab7-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3ab7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c3ab7-111">Return value</span></span>

<span data-ttu-id="c3ab7-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="c3ab7-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c3ab7-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c3ab7-113">Return code</span></span>                                                                             | <span data-ttu-id="c3ab7-114">Description</span><span class="sxs-lookup"><span data-stu-id="c3ab7-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="c3ab7-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab7-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="c3ab7-116">略過的元素數目 *celt*。</span><span class="sxs-lookup"><span data-stu-id="c3ab7-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="c3ab7-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab7-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="c3ab7-118">未 *celt* 略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="c3ab7-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c3ab7-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c3ab7-119">Requirements</span></span>



| <span data-ttu-id="c3ab7-120">需求</span><span class="sxs-lookup"><span data-stu-id="c3ab7-120">Requirement</span></span> | <span data-ttu-id="c3ab7-121">值</span><span class="sxs-lookup"><span data-stu-id="c3ab7-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c3ab7-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="c3ab7-122">TAPI version</span></span><br/> | <span data-ttu-id="c3ab7-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c3ab7-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c3ab7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c3ab7-124">Header</span></span><br/>       | <dl> <span data-ttu-id="c3ab7-125"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab7-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c3ab7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="c3ab7-126">Library</span></span><br/>      | <dl> <span data-ttu-id="c3ab7-127"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab7-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c3ab7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="c3ab7-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="c3ab7-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c3ab7-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3ab7-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3ab7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3ab7-131">**IEnumTime**</span><span class="sxs-lookup"><span data-stu-id="c3ab7-131">**IEnumTime**</span></span>](ienumtime.md)
</dt> </dl>

 

 




