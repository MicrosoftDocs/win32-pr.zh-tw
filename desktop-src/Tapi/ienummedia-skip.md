---
description: Skip 方法會略過列舉順序中的下一個指定元素數目。
ms.assetid: 825972c9-5303-4c5a-9475-dc67c185af91
title: 'IEnumMedia：： Skip 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd950fd61ad6f6b2030b03d0d269854f86e3a02d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999721"
---
# <a name="ienummediaskip-method"></a><span data-ttu-id="eaf72-103">IEnumMedia：： Skip 方法</span><span class="sxs-lookup"><span data-stu-id="eaf72-103">IEnumMedia::Skip method</span></span>

<span data-ttu-id="eaf72-104">\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。</span><span class="sxs-lookup"><span data-stu-id="eaf72-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eaf72-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="eaf72-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eaf72-106">**Skip** 方法會略過列舉順序中的下一個指定元素數目。</span><span class="sxs-lookup"><span data-stu-id="eaf72-106">The **Skip** method skips over the next specified number of elements in the enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="eaf72-107">語法</span><span class="sxs-lookup"><span data-stu-id="eaf72-107">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="eaf72-108">參數</span><span class="sxs-lookup"><span data-stu-id="eaf72-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eaf72-109">*celt* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eaf72-109">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eaf72-110">要略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="eaf72-110">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eaf72-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="eaf72-111">Return value</span></span>

<span data-ttu-id="eaf72-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eaf72-112">This method can return one of these values.</span></span>



| <span data-ttu-id="eaf72-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="eaf72-113">Return code</span></span>                                                                             | <span data-ttu-id="eaf72-114">Description</span><span class="sxs-lookup"><span data-stu-id="eaf72-114">Description</span></span>                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="eaf72-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="eaf72-115"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="eaf72-116">略過的元素數目 *celt*。</span><span class="sxs-lookup"><span data-stu-id="eaf72-116">Number of elements skipped was *celt*.</span></span><br/>     |
| <dl> <span data-ttu-id="eaf72-117"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="eaf72-117"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="eaf72-118">未 *celt* 略過的元素數目。</span><span class="sxs-lookup"><span data-stu-id="eaf72-118">Number of elements skipped was not *celt*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eaf72-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="eaf72-119">Requirements</span></span>



| <span data-ttu-id="eaf72-120">需求</span><span class="sxs-lookup"><span data-stu-id="eaf72-120">Requirement</span></span> | <span data-ttu-id="eaf72-121">值</span><span class="sxs-lookup"><span data-stu-id="eaf72-121">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf72-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="eaf72-122">TAPI version</span></span><br/> | <span data-ttu-id="eaf72-123">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="eaf72-123">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="eaf72-124">標頭</span><span class="sxs-lookup"><span data-stu-id="eaf72-124">Header</span></span><br/>       | <dl> <span data-ttu-id="eaf72-125"><dt>Sdpblb。h</dt></span><span class="sxs-lookup"><span data-stu-id="eaf72-125"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="eaf72-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="eaf72-126">Library</span></span><br/>      | <dl> <span data-ttu-id="eaf72-127"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="eaf72-127"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="eaf72-128">DLL</span><span class="sxs-lookup"><span data-stu-id="eaf72-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="eaf72-129"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eaf72-129"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eaf72-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eaf72-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eaf72-131">**IEnumMedia**</span><span class="sxs-lookup"><span data-stu-id="eaf72-131">**IEnumMedia**</span></span>](ienummedia.md)
</dt> </dl>

 

 




