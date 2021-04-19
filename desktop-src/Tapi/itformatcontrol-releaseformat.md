---
description: ReleaseFormat 方法會釋放與格式相關聯的結構。
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'ITFormatControl：： ReleaseFormat 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984113"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="862a8-103">ITFormatControl：： ReleaseFormat 方法</span><span class="sxs-lookup"><span data-stu-id="862a8-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="862a8-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="862a8-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="862a8-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="862a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="862a8-106">**ReleaseFormat** 方法會釋放與格式相關聯的結構。</span><span class="sxs-lookup"><span data-stu-id="862a8-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="862a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="862a8-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="862a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="862a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="862a8-109">*pMediaType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="862a8-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="862a8-110">終端機格式的 **AM \_ 媒體 \_ 類型** 描述元指標。</span><span class="sxs-lookup"><span data-stu-id="862a8-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="862a8-111">如需 **\_ 媒體 \_ 類型** 的詳細資訊，請參閱 DirectX 檔。</span><span class="sxs-lookup"><span data-stu-id="862a8-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="862a8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="862a8-112">Return value</span></span>

<span data-ttu-id="862a8-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="862a8-113">This method can return one of these values.</span></span>



| <span data-ttu-id="862a8-114">傳回碼</span><span class="sxs-lookup"><span data-stu-id="862a8-114">Return code</span></span>                                                                                   | <span data-ttu-id="862a8-115">Description</span><span class="sxs-lookup"><span data-stu-id="862a8-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="862a8-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="862a8-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="862a8-117">方法成功。</span><span class="sxs-lookup"><span data-stu-id="862a8-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="862a8-118"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="862a8-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="862a8-119">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="862a8-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="862a8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="862a8-120">Requirements</span></span>



| <span data-ttu-id="862a8-121">需求</span><span class="sxs-lookup"><span data-stu-id="862a8-121">Requirement</span></span> | <span data-ttu-id="862a8-122">值</span><span class="sxs-lookup"><span data-stu-id="862a8-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="862a8-123">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="862a8-123">TAPI version</span></span><br/> | <span data-ttu-id="862a8-124">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="862a8-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="862a8-125">標頭</span><span class="sxs-lookup"><span data-stu-id="862a8-125">Header</span></span><br/>       | <dl> <span data-ttu-id="862a8-126"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="862a8-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="862a8-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="862a8-127">Library</span></span><br/>      | <dl> <span data-ttu-id="862a8-128"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="862a8-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="862a8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="862a8-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="862a8-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="862a8-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="862a8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="862a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="862a8-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="862a8-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




