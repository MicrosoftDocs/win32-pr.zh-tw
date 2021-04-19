---
description: GetCurrentFormat 方法會抓取目前資料流程的媒體格式。
ms.assetid: 02d1b3b5-3639-4864-9b72-623bf94acf69
title: 'ITFormatControl：： GetCurrentFormat 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1b711b539ea9a92af6bd345c5a1f48b212b640b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993396"
---
# <a name="itformatcontrolgetcurrentformat-method"></a><span data-ttu-id="ce62f-103">ITFormatControl：： GetCurrentFormat 方法</span><span class="sxs-lookup"><span data-stu-id="ce62f-103">ITFormatControl::GetCurrentFormat method</span></span>

<span data-ttu-id="ce62f-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="ce62f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ce62f-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="ce62f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ce62f-106">**GetCurrentFormat** 方法會抓取目前資料流程的媒體格式。</span><span class="sxs-lookup"><span data-stu-id="ce62f-106">The **GetCurrentFormat** method retrieves the media format of the current stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce62f-107">語法</span><span class="sxs-lookup"><span data-stu-id="ce62f-107">Syntax</span></span>


```C++
HRESULT GetCurrentFormat(
  [out] AM_MEDIA_TYPE **ppMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="ce62f-108">參數</span><span class="sxs-lookup"><span data-stu-id="ce62f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce62f-109">*ppMediaType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ce62f-109">*ppMediaType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ce62f-110">終端機格式的 **AM \_ 媒體 \_ 類型** 描述元指標。</span><span class="sxs-lookup"><span data-stu-id="ce62f-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="ce62f-111">如需 **\_ 媒體 \_ 類型** 的詳細資訊，請參閱 DirectX 檔。</span><span class="sxs-lookup"><span data-stu-id="ce62f-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce62f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce62f-112">Return value</span></span>

<span data-ttu-id="ce62f-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ce62f-113">This method can return one of these values.</span></span>



| <span data-ttu-id="ce62f-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ce62f-114">Return code</span></span>                                                                                   | <span data-ttu-id="ce62f-115">Description</span><span class="sxs-lookup"><span data-stu-id="ce62f-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="ce62f-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ce62f-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ce62f-117">方法成功。</span><span class="sxs-lookup"><span data-stu-id="ce62f-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ce62f-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ce62f-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ce62f-119">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="ce62f-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ce62f-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce62f-120">Requirements</span></span>



| <span data-ttu-id="ce62f-121">需求</span><span class="sxs-lookup"><span data-stu-id="ce62f-121">Requirement</span></span> | <span data-ttu-id="ce62f-122">值</span><span class="sxs-lookup"><span data-stu-id="ce62f-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ce62f-123">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ce62f-123">TAPI version</span></span><br/> | <span data-ttu-id="ce62f-124">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="ce62f-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="ce62f-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ce62f-125">Header</span></span><br/>       | <dl> <span data-ttu-id="ce62f-126"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce62f-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce62f-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="ce62f-127">Library</span></span><br/>      | <dl> <span data-ttu-id="ce62f-128"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="ce62f-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="ce62f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ce62f-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="ce62f-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce62f-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce62f-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce62f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce62f-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="ce62f-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




