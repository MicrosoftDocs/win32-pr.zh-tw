---
title: 'WINBIO_BIR_FIELD 常數 (Winbio \_ 類型 .h) '
description: 指定位元遮罩。
ms.assetid: D8D12BCF-FEB3-4E02-B751-9F3AE5048BC1
topic_type:
- apiref
api_name:
- WINBIO_BIR_FIELD_SUBHEAD_COUNT
- WINBIO_BIR_FIELD_PRODUCT_ID
- WINBIO_BIR_FIELD_PATRON_ID
- WINBIO_BIR_FIELD_INDEX
- WINBIO_BIR_FIELD_CREATION_DATE
- WINBIO_BIR_FIELD_VALIDITY_PERIOD
- WINBIO_BIR_FIELD_BIOMETRIC_TYPE
- WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE
- WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION
- WINBIO_BIR_FIELD_PATRON_HEADER_VERSION
- WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE
- WINBIO_BIR_FIELD_BIOMETRIC_CONDITION
- WINBIO_BIR_FIELD_QUALITY
- WINBIO_BIR_FIELD_CREATOR
- WINBIO_BIR_FIELD_CHALLENGE
- WINBIO_BIR_FIELD_PAYLOAD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 104710f1686f13227fbe65782c2baf9c13149650
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317268"
---
# <a name="winbio_bir_field-constants"></a><span data-ttu-id="65b02-103">WINBIO \_ BIR \_ 欄位常數</span><span class="sxs-lookup"><span data-stu-id="65b02-103">WINBIO\_BIR\_FIELD Constants</span></span>

<span data-ttu-id="65b02-104">下列常數可用來為 [**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **ValidFields** 成員建立位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="65b02-104">The following constants are used to create a bitmask for the **ValidFields** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="65b02-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="65b02-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="65b02-106">Description</span><span class="sxs-lookup"><span data-stu-id="65b02-106">Description</span></span>                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_BIR_FIELD_SUBHEAD_COUNT"></span><span id="winbio_bir_field_subhead_count"></span><dl> <span data-ttu-id="65b02-107"><dt>**WINBIO \_BIR \_ FIELD \_ .subhead \_ COUNT**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-107"><dt>**WINBIO\_BIR\_FIELD\_SUBHEAD\_COUNT**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="65b02-108">為了符合 NISTIR 6529-A，常見的生物特徵辨識 Exchange 格式架構 (CBEFF) Patron 格式 A，但不會使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-108">Provided for conformity with NISTIR 6529-A, the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A, but not used.</span></span><br/> |
| <span id="WINBIO_BIR_FIELD_PRODUCT_ID"></span><span id="winbio_bir_field_product_id"></span><dl> <span data-ttu-id="65b02-109"><dt>**WINBIO \_BIR \_ 欄位 \_ 產品 \_ 識別碼**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-109"><dt>**WINBIO\_BIR\_FIELD\_PRODUCT\_ID**</dt> <dt>0x0002</dt></span></span> </dl>                                   | <span data-ttu-id="65b02-110">**ProductId** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-110">The **ProductId** member is valid.</span></span><br/>                                                                                                 |
| <span id="WINBIO_BIR_FIELD_PATRON_ID"></span><span id="winbio_bir_field_patron_id"></span><dl> <span data-ttu-id="65b02-111"><dt>**WINBIO \_BIR \_ 欄位 \_ PATRON \_ 識別碼**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-111"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_ID**</dt> <dt>0x0004</dt></span></span> </dl>                                      | <span data-ttu-id="65b02-112">為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-112">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_INDEX"></span><span id="winbio_bir_field_index"></span><dl> <span data-ttu-id="65b02-113"><dt>**WINBIO \_BIR \_ 欄位 \_ 索引**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-113"><dt>**WINBIO\_BIR\_FIELD\_INDEX**</dt> <dt>0x0008</dt></span></span> </dl>                                                   | <span data-ttu-id="65b02-114">為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-114">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CREATION_DATE"></span><span id="winbio_bir_field_creation_date"></span><dl> <span data-ttu-id="65b02-115"><dt>**WINBIO \_BIR \_ 欄位 \_ 建立 \_ 日期**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-115"><dt>**WINBIO\_BIR\_FIELD\_CREATION\_DATE**</dt> <dt>0x0010</dt></span></span> </dl>                          | <span data-ttu-id="65b02-116">**CreationDate** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-116">The **CreationDate** member is valid.</span></span><br/>                                                                                              |
| <span id="WINBIO_BIR_FIELD_VALIDITY_PERIOD"></span><span id="winbio_bir_field_validity_period"></span><dl> <span data-ttu-id="65b02-117"><dt>**WINBIO \_BIR \_ 欄位 \_ 有效 \_ 期間**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-117"><dt>**WINBIO\_BIR\_FIELD\_VALIDITY\_PERIOD**</dt> <dt>0x0020</dt></span></span> </dl>                    | <span data-ttu-id="65b02-118">**ValidityPeriod** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-118">The **ValidityPeriod** member is valid.</span></span><br/>                                                                                            |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_TYPE"></span><span id="winbio_bir_field_biometric_type"></span><dl> <span data-ttu-id="65b02-119"><dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 類型**</dt> <dt>0x0040</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-119"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_TYPE**</dt> <dt>0x0040</dt></span></span> </dl>                       | <span data-ttu-id="65b02-120">**類型** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-120">The **Type** member is valid.</span></span><br/>                                                                                                      |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_SUBTYPE"></span><span id="winbio_bir_field_biometric_subtype"></span><dl> <span data-ttu-id="65b02-121"><dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 子類型**</dt> <dt>0x0080</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-121"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_SUBTYPE**</dt> <dt>0x0080</dt></span></span> </dl>              | <span data-ttu-id="65b02-122">**子類型** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-122">The **Subtype** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_CBEFF_HEADER_VERSION"></span><span id="winbio_bir_field_cbeff_header_version"></span><dl> <span data-ttu-id="65b02-123"><dt>**WINBIO \_BIR \_ 欄位 \_ CBEFF \_ 標頭 \_ 版本**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-123"><dt>**WINBIO\_BIR\_FIELD\_CBEFF\_HEADER\_VERSION**</dt> <dt>0x0100</dt></span></span> </dl>    | <span data-ttu-id="65b02-124">**HeaderVersion** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-124">The **HeaderVersion** member is valid.</span></span><br/>                                                                                             |
| <span id="WINBIO_BIR_FIELD_PATRON_HEADER_VERSION"></span><span id="winbio_bir_field_patron_header_version"></span><dl> <span data-ttu-id="65b02-125"><dt>**WINBIO \_BIR \_ 欄位 \_ PATRON \_ 標頭 \_ 版本**</dt> <dt>0x0200</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-125"><dt>**WINBIO\_BIR\_FIELD\_PATRON\_HEADER\_VERSION**</dt> <dt>0x0200</dt></span></span> </dl> | <span data-ttu-id="65b02-126">**PatronHeaderVersion** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-126">The **PatronHeaderVersion** member is valid.</span></span><br/>                                                                                       |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_PURPOSE"></span><span id="winbio_bir_field_biometric_purpose"></span><dl> <span data-ttu-id="65b02-127"><dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 用途**</dt> <dt>0x0400</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-127"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_PURPOSE**</dt> <dt>0x0400</dt></span></span> </dl>              | <span data-ttu-id="65b02-128">**目的** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-128">The **Purpose** member is valid.</span></span><br/>                                                                                                   |
| <span id="WINBIO_BIR_FIELD_BIOMETRIC_CONDITION"></span><span id="winbio_bir_field_biometric_condition"></span><dl> <span data-ttu-id="65b02-129"><dt>**WINBIO \_BIR \_ 欄位 \_ 生物特徵辨識 \_ 條件**</dt> <dt>0x0800</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-129"><dt>**WINBIO\_BIR\_FIELD\_BIOMETRIC\_CONDITION**</dt> <dt>0x0800</dt></span></span> </dl>        | <span data-ttu-id="65b02-130">為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-130">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_QUALITY"></span><span id="winbio_bir_field_quality"></span><dl> <span data-ttu-id="65b02-131"><dt>**WINBIO \_BIR \_ 欄位 \_ 品質**</dt> <dt>0x1000</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-131"><dt>**WINBIO\_BIR\_FIELD\_QUALITY**</dt> <dt>0x1000</dt></span></span> </dl>                                             | <span data-ttu-id="65b02-132">**DataQuality** 成員有效。</span><span class="sxs-lookup"><span data-stu-id="65b02-132">The **DataQuality** member is valid.</span></span><br/>                                                                                               |
| <span id="WINBIO_BIR_FIELD_CREATOR"></span><span id="winbio_bir_field_creator"></span><dl> <span data-ttu-id="65b02-133"><dt>**WINBIO \_BIR \_ FIELD \_ CREATOR**</dt> <dt>0x2000</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-133"><dt>**WINBIO\_BIR\_FIELD\_CREATOR**</dt> <dt>0x2000</dt></span></span> </dl>                                             | <span data-ttu-id="65b02-134">為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-134">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_CHALLENGE"></span><span id="winbio_bir_field_challenge"></span><dl> <span data-ttu-id="65b02-135"><dt>**WINBIO \_BIR \_ 現場 \_ 挑戰**</dt> <dt>0x4000</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-135"><dt>**WINBIO\_BIR\_FIELD\_CHALLENGE**</dt> <dt>0x4000</dt></span></span> </dl>                                       | <span data-ttu-id="65b02-136">為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-136">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |
| <span id="WINBIO_BIR_FIELD_PAYLOAD"></span><span id="winbio_bir_field_payload"></span><dl> <span data-ttu-id="65b02-137"><dt>**WINBIO \_BIR \_ 欄位 \_**</dt>裝載 <dt>0x8000</dt></span><span class="sxs-lookup"><span data-stu-id="65b02-137"><dt>**WINBIO\_BIR\_FIELD\_PAYLOAD**</dt> <dt>0x8000</dt></span></span> </dl>                                             | <span data-ttu-id="65b02-138">為了符合 NISTIR 6529-A、CBEFF Patron 格式，但未使用。</span><span class="sxs-lookup"><span data-stu-id="65b02-138">Provided for conformity with NISTIR 6529-A, CBEFF Patron Format A, but not used.</span></span><br/>                                                   |



## <a name="requirements"></a><span data-ttu-id="65b02-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="65b02-139">Requirements</span></span>



| <span data-ttu-id="65b02-140">需求</span><span class="sxs-lookup"><span data-stu-id="65b02-140">Requirement</span></span> | <span data-ttu-id="65b02-141">值</span><span class="sxs-lookup"><span data-stu-id="65b02-141">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b02-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65b02-142">Minimum supported client</span></span><br/> | <span data-ttu-id="65b02-143">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65b02-143">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="65b02-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65b02-144">Minimum supported server</span></span><br/> | <span data-ttu-id="65b02-145">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65b02-145">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="65b02-146">標頭</span><span class="sxs-lookup"><span data-stu-id="65b02-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="65b02-147"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="65b02-147"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65b02-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65b02-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b02-149">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="65b02-149">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





