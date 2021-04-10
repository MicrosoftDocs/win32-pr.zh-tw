---
title: 'BITS_JOB_PROPERTY_VALUE 結構 (>deliveryoptimization .h) '
description: BITS_JOB_PROPERTY_VALUE 聯集會根據 BITS_JOB_PROPERTY_ID 列舉值，提供 DO 作業的屬性值。
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- BITS_JOB_PROPERTY_VALUE 結構
- BITS_JOB_PROPERTY_VALUE 結構
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103662"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="218b9-105">BITS_JOB_PROPERTY_VALUE 結構</span><span class="sxs-lookup"><span data-stu-id="218b9-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="218b9-106">**BITS_JOB_PROPERTY_VALUE** 聯集會根據 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md)列舉值，提供 DO 作業的屬性值。</span><span class="sxs-lookup"><span data-stu-id="218b9-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="218b9-107">語法</span><span class="sxs-lookup"><span data-stu-id="218b9-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="218b9-108">成員</span><span class="sxs-lookup"><span data-stu-id="218b9-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="218b9-109">**Dword**</span><span class="sxs-lookup"><span data-stu-id="218b9-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="218b9-110">使用列舉屬性識別碼 **BITS_JOB_PROPERTY_ID_COST_FLAGS** 時，會傳回這個值，並套用為 DO 作業的 [傳輸原則](https://www.bing.com/search?q=transfer+policy) 。</span><span class="sxs-lookup"><span data-stu-id="218b9-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="218b9-111">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="218b9-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="218b9-112">使用列舉屬性識別碼 **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** 時，會傳回這個值，並表示要向 DO 作業註冊的回呼物件的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="218b9-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="218b9-113">**啟用**</span><span class="sxs-lookup"><span data-stu-id="218b9-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="218b9-114">不支援。</span><span class="sxs-lookup"><span data-stu-id="218b9-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="218b9-115">**Uint64**</span><span class="sxs-lookup"><span data-stu-id="218b9-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="218b9-116">不支援。</span><span class="sxs-lookup"><span data-stu-id="218b9-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="218b9-117">**Target**</span><span class="sxs-lookup"><span data-stu-id="218b9-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="218b9-118">不支援。</span><span class="sxs-lookup"><span data-stu-id="218b9-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="218b9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="218b9-119">Requirements</span></span>



| <span data-ttu-id="218b9-120">需求</span><span class="sxs-lookup"><span data-stu-id="218b9-120">Requirement</span></span> | <span data-ttu-id="218b9-121">值</span><span class="sxs-lookup"><span data-stu-id="218b9-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="218b9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="218b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="218b9-123">Windows 10， \[ 僅限1709版桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="218b9-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="218b9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="218b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="218b9-125">僅限 Windows Server，版本 1709 \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="218b9-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="218b9-126">標頭</span><span class="sxs-lookup"><span data-stu-id="218b9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="218b9-127"><dt>>deliveryoptimization。h</dt></span><span class="sxs-lookup"><span data-stu-id="218b9-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="218b9-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="218b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218b9-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="218b9-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="218b9-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="218b9-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





