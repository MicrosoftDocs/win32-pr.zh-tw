---
description: Set 方法會設定指定之資料流程品質屬性的值。
ms.assetid: 57029d1c-ac63-45c0-9d07-43c7b46a27b1
title: 'ITStreamQualityControl：： Set 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61deed4d6edc9b08d7c11fcc8d44d8cf91e11f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998836"
---
# <a name="itstreamqualitycontrolset-method"></a><span data-ttu-id="695a8-103">ITStreamQualityControl：： Set 方法</span><span class="sxs-lookup"><span data-stu-id="695a8-103">ITStreamQualityControl::Set method</span></span>

<span data-ttu-id="695a8-104">\[ 在 Windows Vista、Windows Server 2008 和後續的作業系統版本中，無法使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="695a8-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="695a8-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="695a8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="695a8-106">**Set** 方法會設定指定之 [**資料流程品質屬性**](streamqualityproperty.md)的值。</span><span class="sxs-lookup"><span data-stu-id="695a8-106">The **Set** method sets the value of a given [**stream quality property**](streamqualityproperty.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="695a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="695a8-107">Syntax</span></span>


```C++
HRESULT Set(
  [in] StreamQualityProperty Property,
  [in] long                  lValue,
  [in] TAPIControlFlags      lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="695a8-108">參數</span><span class="sxs-lookup"><span data-stu-id="695a8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="695a8-109">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="695a8-109">*Property* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695a8-110">[**StreamQualityProperty**](streamqualityproperty.md)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="695a8-110">Member of the [**StreamQualityProperty**](streamqualityproperty.md) enum.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-111">*左* \[ 值在\]</span><span class="sxs-lookup"><span data-stu-id="695a8-111">*lValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695a8-112">輸入 *屬性* 所需的值。</span><span class="sxs-lookup"><span data-stu-id="695a8-112">Desired value for the input *Property*.</span></span>

</dd> <dt>

<span data-ttu-id="695a8-113">*lFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="695a8-113">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="695a8-114">[**TAPIControlFlags**](tapicontrolflags.md)列舉的值，指出要如何控制 *屬性* 值。</span><span class="sxs-lookup"><span data-stu-id="695a8-114">Value of the [**TAPIControlFlags**](tapicontrolflags.md) enum indicating how the *Property* value is to be controlled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="695a8-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="695a8-115">Return value</span></span>

<span data-ttu-id="695a8-116">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="695a8-116">This method can return one of these values.</span></span>



| <span data-ttu-id="695a8-117">值</span><span class="sxs-lookup"><span data-stu-id="695a8-117">Value</span></span>                                                                                         | <span data-ttu-id="695a8-118">意義</span><span class="sxs-lookup"><span data-stu-id="695a8-118">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="695a8-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="695a8-120">方法成功。</span><span class="sxs-lookup"><span data-stu-id="695a8-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="695a8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="695a8-122">記憶體不足，無法執行操作。</span><span class="sxs-lookup"><span data-stu-id="695a8-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="695a8-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="695a8-123">Requirements</span></span>



| <span data-ttu-id="695a8-124">需求</span><span class="sxs-lookup"><span data-stu-id="695a8-124">Requirement</span></span> | <span data-ttu-id="695a8-125">值</span><span class="sxs-lookup"><span data-stu-id="695a8-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="695a8-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="695a8-126">TAPI version</span></span><br/> | <span data-ttu-id="695a8-127">需要 TAPI 3。1</span><span class="sxs-lookup"><span data-stu-id="695a8-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="695a8-128">標頭</span><span class="sxs-lookup"><span data-stu-id="695a8-128">Header</span></span><br/>       | <dl> <span data-ttu-id="695a8-129"><dt>Ipmsp。h</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="695a8-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="695a8-130">Library</span></span><br/>      | <dl> <span data-ttu-id="695a8-131"><dt>Uuid</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="695a8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="695a8-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="695a8-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="695a8-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="695a8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="695a8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="695a8-135">**ITStreamQualityControl**</span><span class="sxs-lookup"><span data-stu-id="695a8-135">**ITStreamQualityControl**</span></span>](itstreamqualitycontrol.md)
</dt> <dt>

[<span data-ttu-id="695a8-136">**TAPIControlFlags**</span><span class="sxs-lookup"><span data-stu-id="695a8-136">**TAPIControlFlags**</span></span>](tapicontrolflags.md)
</dt> <dt>

[<span data-ttu-id="695a8-137">**StreamQualityProperty**</span><span class="sxs-lookup"><span data-stu-id="695a8-137">**StreamQualityProperty**</span></span>](streamqualityproperty.md)
</dt> </dl>

 

 




