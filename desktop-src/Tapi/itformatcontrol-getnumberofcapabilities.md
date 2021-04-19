---
description: GetNumberOfCapabilities 方法會抓取與目前格式相關聯的功能數目。
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'ITFormatControl：： GetNumberOfCapabilities 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993395"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="228e5-103">ITFormatControl：： GetNumberOfCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="228e5-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="228e5-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="228e5-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="228e5-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="228e5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="228e5-106">**GetNumberOfCapabilities** 方法會抓取與目前格式相關聯的功能數目。</span><span class="sxs-lookup"><span data-stu-id="228e5-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="228e5-107">語法</span><span class="sxs-lookup"><span data-stu-id="228e5-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="228e5-108">參數</span><span class="sxs-lookup"><span data-stu-id="228e5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="228e5-109">*pdwCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="228e5-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="228e5-110">功能的計數。</span><span class="sxs-lookup"><span data-stu-id="228e5-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="228e5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="228e5-111">Return value</span></span>

<span data-ttu-id="228e5-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="228e5-112">This method can return one of these values.</span></span>



| <span data-ttu-id="228e5-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="228e5-113">Return code</span></span>                                                                                   | <span data-ttu-id="228e5-114">Description</span><span class="sxs-lookup"><span data-stu-id="228e5-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="228e5-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="228e5-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="228e5-116">方法成功。</span><span class="sxs-lookup"><span data-stu-id="228e5-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="228e5-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="228e5-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="228e5-118">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="228e5-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="228e5-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="228e5-119">Requirements</span></span>



| <span data-ttu-id="228e5-120">需求</span><span class="sxs-lookup"><span data-stu-id="228e5-120">Requirement</span></span> | <span data-ttu-id="228e5-121">值</span><span class="sxs-lookup"><span data-stu-id="228e5-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="228e5-122">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="228e5-122">TAPI version</span></span><br/> | <span data-ttu-id="228e5-123">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="228e5-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="228e5-124">標頭</span><span class="sxs-lookup"><span data-stu-id="228e5-124">Header</span></span><br/>       | <dl> <span data-ttu-id="228e5-125"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="228e5-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="228e5-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="228e5-126">Library</span></span><br/>      | <dl> <span data-ttu-id="228e5-127"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="228e5-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="228e5-128">DLL</span><span class="sxs-lookup"><span data-stu-id="228e5-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="228e5-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="228e5-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="228e5-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="228e5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="228e5-131">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="228e5-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




