---
description: ReOrderCapabilities 方法會為格式功能設定新的順序。
ms.assetid: 05785d64-a22f-411f-9fae-318828d30c52
title: 'ITFormatControl：： ReOrderCapabilities 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d6f7800e4a04dbd70c5b270778cd7eb0ff540b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987180"
---
# <a name="itformatcontrolreordercapabilities-method"></a><span data-ttu-id="a6cc3-103">ITFormatControl：： ReOrderCapabilities 方法</span><span class="sxs-lookup"><span data-stu-id="a6cc3-103">ITFormatControl::ReOrderCapabilities method</span></span>

<span data-ttu-id="a6cc3-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a6cc3-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="a6cc3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a6cc3-106">**ReOrderCapabilities** 方法會為格式功能設定新的順序。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-106">The **ReOrderCapabilities** method sets a new order for format capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6cc3-107">語法</span><span class="sxs-lookup"><span data-stu-id="a6cc3-107">Syntax</span></span>


```C++
HRESULT ReOrderCapabilities(
  [in] DWORD *pdwIndices,
  [in] BOOL  *pfEnabled,
  [in] BOOL  *pfPublicize,
  [in] DWORD dwNumIndices
);
```



## <a name="parameters"></a><span data-ttu-id="a6cc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6cc3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6cc3-109">*pdwIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6cc3-109">*pdwIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cc3-110">要重新排序之格式的索引。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-110">Index of the format being reordered.</span></span>

</dd> <dt>

<span data-ttu-id="a6cc3-111">*pfEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6cc3-111">*pfEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cc3-112">指出是否應該啟用或停用格式。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-112">Indicates whether the format should be enabled or disabled.</span></span>

</dd> <dt>

<span data-ttu-id="a6cc3-113">*pfPublicize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6cc3-113">*pfPublicize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cc3-114">指出是否應該將格式設為可用。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-114">Indicates whether the format should be made available.</span></span>

</dd> <dt>

<span data-ttu-id="a6cc3-115">*dwNumIndices* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a6cc3-115">*dwNumIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a6cc3-116">格式的新索引編號。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-116">New index number for the format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6cc3-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6cc3-117">Return value</span></span>

<span data-ttu-id="a6cc3-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-118">This method can return one of these values.</span></span>



| <span data-ttu-id="a6cc3-119">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a6cc3-119">Return code</span></span>                                                                                   | <span data-ttu-id="a6cc3-120">Description</span><span class="sxs-lookup"><span data-stu-id="a6cc3-120">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a6cc3-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cc3-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a6cc3-122">方法成功。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-122">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a6cc3-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a6cc3-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a6cc3-124">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-124">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a6cc3-125">備註</span><span class="sxs-lookup"><span data-stu-id="a6cc3-125">Remarks</span></span>

<span data-ttu-id="a6cc3-126">使用這個方法之前，必須先呼叫 [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="a6cc3-126">The [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) method must be called prior to using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6cc3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6cc3-127">Requirements</span></span>



| <span data-ttu-id="a6cc3-128">需求</span><span class="sxs-lookup"><span data-stu-id="a6cc3-128">Requirement</span></span> | <span data-ttu-id="a6cc3-129">值</span><span class="sxs-lookup"><span data-stu-id="a6cc3-129">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cc3-130">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="a6cc3-130">TAPI version</span></span><br/> | <span data-ttu-id="a6cc3-131">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="a6cc3-131">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="a6cc3-132">標頭</span><span class="sxs-lookup"><span data-stu-id="a6cc3-132">Header</span></span><br/>       | <dl> <span data-ttu-id="a6cc3-133"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6cc3-133"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a6cc3-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="a6cc3-134">Library</span></span><br/>      | <dl> <span data-ttu-id="a6cc3-135"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="a6cc3-135"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="a6cc3-136">DLL</span><span class="sxs-lookup"><span data-stu-id="a6cc3-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="a6cc3-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a6cc3-137"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6cc3-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a6cc3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cc3-139">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="a6cc3-139">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> <dt>

[<span data-ttu-id="a6cc3-140">**GetNumberOfCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a6cc3-140">**GetNumberOfCapabilities**</span></span>](itformatcontrol-getnumberofcapabilities.md)
</dt> </dl>

 

 




