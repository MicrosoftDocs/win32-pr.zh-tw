---
title: 'WINBIO_BIR_HEADER 結構 (Winbio \_ 類型 .h) '
description: 包含 (BIR) 的生物特徵辨識資訊記錄標頭。
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103698"
---
# <a name="winbio_bir_header-structure"></a><span data-ttu-id="82b51-104">WINBIO \_ BIR \_ 標頭結構</span><span class="sxs-lookup"><span data-stu-id="82b51-104">WINBIO\_BIR\_HEADER structure</span></span>

<span data-ttu-id="82b51-105">**WINBIO \_ BIR \_ 標頭** 結構包含生物特徵辨識資訊記錄的標頭 (BIR) 。</span><span class="sxs-lookup"><span data-stu-id="82b51-105">The **WINBIO\_BIR\_HEADER** structure contains the header of a biometric information record (BIR).</span></span>

## <a name="syntax"></a><span data-ttu-id="82b51-106">語法</span><span class="sxs-lookup"><span data-stu-id="82b51-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a><span data-ttu-id="82b51-107">成員</span><span class="sxs-lookup"><span data-stu-id="82b51-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="82b51-108">**ValidFields**</span><span class="sxs-lookup"><span data-stu-id="82b51-108">**ValidFields**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-109">位元遮罩，指定此結構中的哪些欄位有效。</span><span class="sxs-lookup"><span data-stu-id="82b51-109">Bitmask that specifies which fields in this structure are valid.</span></span> <span data-ttu-id="82b51-110">如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 欄位常數**](winbio-bir-field-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="82b51-110">For more information, see [**WINBIO\_BIR\_FIELD Constants**](winbio-bir-field-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b51-111">**HeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="82b51-111">**HeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-112">指定標頭版本的 **WINBIO \_ BIR \_ 版本** 常數。</span><span class="sxs-lookup"><span data-stu-id="82b51-112">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="82b51-113">版本號碼是8位的值，其中的前四個位指定主要號碼，而低四個位則指定次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="82b51-113">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="82b51-114">目前，這必須是 WINBIO \_ CBEFF \_ 標頭 \_ 版本 (0x11) 。</span><span class="sxs-lookup"><span data-stu-id="82b51-114">Currently this must be WINBIO\_CBEFF\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="82b51-115">**PatronHeaderVersion**</span><span class="sxs-lookup"><span data-stu-id="82b51-115">**PatronHeaderVersion**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-116">指定標頭版本的 **WINBIO \_ BIR \_ 版本** 常數。</span><span class="sxs-lookup"><span data-stu-id="82b51-116">A **WINBIO\_BIR\_VERSION** constant that specifies the header version.</span></span> <span data-ttu-id="82b51-117">版本號碼是8位的值，其中的前四個位指定主要號碼，而低四個位則指定次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="82b51-117">Version numbers are 8-bit values where the upper four bits specify the major number and the low four bits specify the minor version number.</span></span> <span data-ttu-id="82b51-118">目前，這必須是 WINBIO \_ PATRON \_ 標頭 \_ 版本 (0x11) 。</span><span class="sxs-lookup"><span data-stu-id="82b51-118">Currently this must be WINBIO\_PATRON\_HEADER\_VERSION (0x11).</span></span>

</dd> <dt>

<span data-ttu-id="82b51-119">**DataFlags**</span><span class="sxs-lookup"><span data-stu-id="82b51-119">**DataFlags**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-120">值，指定標頭資料的格式。</span><span class="sxs-lookup"><span data-stu-id="82b51-120">A value that specifies the format of the header data.</span></span> <span data-ttu-id="82b51-121">這可以是下列安全性和處理層級旗標的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="82b51-121">This can be a bitwise **OR** of the following security and processing level flags.</span></span> <span data-ttu-id="82b51-122">如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 資料 \_ 旗標常數**](winbio-bir-data-flags-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="82b51-122">For more information, see [**WINBIO\_BIR\_DATA\_FLAGS Constants**](winbio-bir-data-flags-constants.md).</span></span>



| <span data-ttu-id="82b51-123">值</span><span class="sxs-lookup"><span data-stu-id="82b51-123">Value</span></span>                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="82b51-124">意義</span><span class="sxs-lookup"><span data-stu-id="82b51-124">Meaning</span></span>                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="82b51-125"><dt>**WINBIO \_資料 \_ 旗標 \_ 隱私權**</dt> <dt> ( (UCHAR) 0x02)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-125"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>((UCHAR)0x02)</dt></span></span> </dl>                                       | <span data-ttu-id="82b51-126">資料已加密。</span><span class="sxs-lookup"><span data-stu-id="82b51-126">The data is encrypted.</span></span><br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="82b51-127"><dt>**WINBIO \_資料 \_ 旗標 \_ 完整性**</dt> <dt> ( (UCHAR) 0x01)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-127"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>((UCHAR)0x01)</dt></span></span> </dl>                                 | <span data-ttu-id="82b51-128">資料是由 (MAC) 的訊息驗證程式代碼進行數位簽署或保護。</span><span class="sxs-lookup"><span data-stu-id="82b51-128">The data is digitally signed or protected by a message authentication code (MAC).</span></span><br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="82b51-129"><dt>**WINBIO \_\_ \_ 簽署的資料旗**</dt>標 <dt> ( (UCHAR) 0x04)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-129"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>((UCHAR)0x04)</dt></span></span> </dl>                                          | <span data-ttu-id="82b51-130">如果設定此旗標和 **WINBIO \_ 資料旗標 \_ \_ 完整性** 旗標，則會簽署資料。</span><span class="sxs-lookup"><span data-stu-id="82b51-130">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="82b51-131">如果未設定此旗標，但已設定 **WINBIO \_ 資料 \_ 旗標 \_ 完整性** 旗標，則會計算資料的 MAC。</span><span class="sxs-lookup"><span data-stu-id="82b51-131">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed over the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="82b51-132"><dt>**WINBIO \_資料 \_ 旗標 \_ 原始**</dt> <dt> ( (UCHAR) 0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-132"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>((UCHAR)0x20)</dt></span></span> </dl>                                                   | <span data-ttu-id="82b51-133">資料的格式與捕捉的格式一樣。</span><span class="sxs-lookup"><span data-stu-id="82b51-133">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="82b51-134"><dt>**WINBIO \_資料 \_ 旗標 \_ 中繼**</dt> <dt> ( (UCHAR) 0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-134"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt></span></span> </dl>                        | <span data-ttu-id="82b51-135">資料不是原始資料，但尚未完全處理。</span><span class="sxs-lookup"><span data-stu-id="82b51-135">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="82b51-136"><dt>**WINBIO \_\_ \_**</dt> <dt> ( (UCHAR) 0X80)</dt>處理的資料旗標</span><span class="sxs-lookup"><span data-stu-id="82b51-136"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>((UCHAR)0x80)</dt></span></span> </dl>                                 | <span data-ttu-id="82b51-137">已處理資料。</span><span class="sxs-lookup"><span data-stu-id="82b51-137">The data has been processed.</span></span><br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="82b51-138"><dt>**WINBIO \_資料 \_ 旗標 \_ 選項 \_ 遮罩 \_ 存在**</dt> <dt> ( (UCHAR) 0x08)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-138"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>((UCHAR)0x08)</dt></span></span> </dl> | <span data-ttu-id="82b51-139">這個值一律是 1。</span><span class="sxs-lookup"><span data-stu-id="82b51-139">This value is always 1.</span></span><br/>                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="82b51-140">**型別**</span><span class="sxs-lookup"><span data-stu-id="82b51-140">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-141">WINBIO \_ 生物特徵辨識 \_ 類型值，指定生物特徵辨識資訊記錄中所參考的生物特徵辨識資料類型。</span><span class="sxs-lookup"><span data-stu-id="82b51-141">A WINBIO\_BIOMETRIC\_TYPE value that specifies the type of biometric data referenced in the biometric information record.</span></span> <span data-ttu-id="82b51-142">目前只支援 **WINBIO \_ 類型 \_ 指紋** 。</span><span class="sxs-lookup"><span data-stu-id="82b51-142">Currently only **WINBIO\_TYPE\_FINGERPRINT** is supported.</span></span> <span data-ttu-id="82b51-143">如需詳細資訊，請參閱 [**WINBIO \_ 生物特徵辨識 \_ 類型常數**](winbio-biometric-type-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="82b51-143">For more information, see [**WINBIO\_BIOMETRIC\_TYPE Constants**](winbio-biometric-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b51-144">**Subtype**</span><span class="sxs-lookup"><span data-stu-id="82b51-144">**Subtype**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-145">**WINBIO \_ 生物特徵辨識 \_ 子類型** 值，指定與生物特徵辨識資料相關聯的輔助因素。</span><span class="sxs-lookup"><span data-stu-id="82b51-145">A **WINBIO\_BIOMETRIC\_SUBTYPE** value that specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="82b51-146">如需詳細資訊，請參閱備註和 [**WINBIO \_ 生物特徵辨識 \_ 子類型常數**](winbio-biometric-subtype-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="82b51-146">For more information, see Remarks and [**WINBIO\_BIOMETRIC\_SUBTYPE Constants**](winbio-biometric-subtype-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="82b51-147">**目的**</span><span class="sxs-lookup"><span data-stu-id="82b51-147">**Purpose**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-148">**WINBIO \_ BIR \_ 目的** 遮罩，可指定資料的預期用途。</span><span class="sxs-lookup"><span data-stu-id="82b51-148">A **WINBIO\_BIR\_PURPOSE** mask that specifies the intended use of the data.</span></span> <span data-ttu-id="82b51-149">這可以是下列值的位 **or** 。</span><span class="sxs-lookup"><span data-stu-id="82b51-149">This can be a bitwise **OR** of the following values.</span></span> <span data-ttu-id="82b51-150">如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 用途常數**](winbio-bir-purpose-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="82b51-150">For more information, see [**WINBIO\_BIR\_PURPOSE Constants**](winbio-bir-purpose-constants.md).</span></span>

-   <span data-ttu-id="82b51-151">WINBIO \_ 用途 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="82b51-151">WINBIO\_PURPOSE\_VERIFY</span></span>
-   <span data-ttu-id="82b51-152">WINBIO \_ 目的 \_ 識別</span><span class="sxs-lookup"><span data-stu-id="82b51-152">WINBIO\_PURPOSE\_IDENTIFY</span></span>
-   <span data-ttu-id="82b51-153">WINBIO \_ 目的 \_ 註冊</span><span class="sxs-lookup"><span data-stu-id="82b51-153">WINBIO\_PURPOSE\_ENROLL</span></span>
-   <span data-ttu-id="82b51-154">WINBIO \_ 目的 \_ 註冊 \_ 以進行 \_ 驗證</span><span class="sxs-lookup"><span data-stu-id="82b51-154">WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION</span></span>
-   <span data-ttu-id="82b51-155">WINBIO \_ 目的 \_ 註冊 \_ 以供 \_ 識別</span><span class="sxs-lookup"><span data-stu-id="82b51-155">WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION</span></span>
-   <span data-ttu-id="82b51-156">WINBIO \_ 目的 \_ 審核</span><span class="sxs-lookup"><span data-stu-id="82b51-156">WINBIO\_PURPOSE\_AUDIT</span></span>

</dd> <dt>

<span data-ttu-id="82b51-157">**DataQuality**</span><span class="sxs-lookup"><span data-stu-id="82b51-157">**DataQuality**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-158">值，指定生物特徵辨識資訊記錄中生物特徵辨識資料的相對品質 (BIR) 。</span><span class="sxs-lookup"><span data-stu-id="82b51-158">A value that specifies the relative quality of the biometric data in the biometric information record (BIR).</span></span> <span data-ttu-id="82b51-159">這可以是從0到100或下列其中一個值的整數。</span><span class="sxs-lookup"><span data-stu-id="82b51-159">This can be an integer from 0 to 100 or one of the following values.</span></span> <span data-ttu-id="82b51-160">如需詳細資訊，請參閱 [**WINBIO \_ BIR \_ 品質常數**](winbio-bir-quality-constants.md)。</span><span class="sxs-lookup"><span data-stu-id="82b51-160">For more information, see [**WINBIO\_BIR\_QUALITY Constants**](winbio-bir-quality-constants.md).</span></span>



| <span data-ttu-id="82b51-161">值</span><span class="sxs-lookup"><span data-stu-id="82b51-161">Value</span></span>                                                                                                                                                                                                                                                                                                        | <span data-ttu-id="82b51-162">意義</span><span class="sxs-lookup"><span data-stu-id="82b51-162">Meaning</span></span>                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <span data-ttu-id="82b51-163"><dt>**WINBIO \_資料 \_ 品質 \_ 未 \_ 設定**</dt> <dt> ( (WINBIO \_ BIR \_ QUALITY) -1)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-163"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SET**</dt> <dt>((WINBIO\_BIR\_QUALITY)-1)</dt></span></span> </dl>                   | <span data-ttu-id="82b51-164">BIR 建立者支援品質度量，但未在 BIR 中設定任何值。</span><span class="sxs-lookup"><span data-stu-id="82b51-164">Quality measurements are supported by the BIR creator but no value is set in the BIR.</span></span><br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <span data-ttu-id="82b51-165"><dt>**WINBIO \_\_ \_ 不 \_ 支援的資料品質**</dt> <dt> ( (WINBIO \_ BIR \_ 品質) -2)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-165"><dt>**WINBIO\_DATA\_QUALITY\_NOT\_SUPPORTED**</dt> <dt>((WINBIO\_BIR\_QUALITY)-2)</dt></span></span> </dl> | <span data-ttu-id="82b51-166">BIR 建立者不支援品質度量。</span><span class="sxs-lookup"><span data-stu-id="82b51-166">Quality measurements are not supported by the BIR creator.</span></span><br/>                            |



 

</dd> <dt>

<span data-ttu-id="82b51-167">**CreationDate**</span><span class="sxs-lookup"><span data-stu-id="82b51-167">**CreationDate**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-168">BIR 建立的日期和時間，以國際標準時間 (格林威治平均時間) ）。</span><span class="sxs-lookup"><span data-stu-id="82b51-168">The date and time, in Coordinated Universal Time (Greenwich Mean Time), that the BIR was created.</span></span>

</dd> <dt>

<span data-ttu-id="82b51-169">**ValidityPeriod**</span><span class="sxs-lookup"><span data-stu-id="82b51-169">**ValidityPeriod**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-170">BIR 有效的期間。</span><span class="sxs-lookup"><span data-stu-id="82b51-170">The period for which the BIR is valid.</span></span>

<dl> <dt>

<span data-ttu-id="82b51-171">**BeginDate**</span><span class="sxs-lookup"><span data-stu-id="82b51-171">**BeginDate**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-172">有效期間開始的日期和時間（國際標準時間）。</span><span class="sxs-lookup"><span data-stu-id="82b51-172">The date and time, in Coordinated Universal Time, that the validity period starts.</span></span>

</dd> <dt>

<span data-ttu-id="82b51-173">**日期**</span><span class="sxs-lookup"><span data-stu-id="82b51-173">**EndDate**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-174">BIR 不再有效的日期和時間，以國際標準時間。</span><span class="sxs-lookup"><span data-stu-id="82b51-174">The date and time, in Coordinated Universal Time, at which the BIR ceases to be valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="82b51-175">**BiometricDataFormat**</span><span class="sxs-lookup"><span data-stu-id="82b51-175">**BiometricDataFormat**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-176">[**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)結構，可指定 [**WINBIO \_ BIR**](winbio-bir.md)結構中標準資料區塊的資料格式。</span><span class="sxs-lookup"><span data-stu-id="82b51-176">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the data format of the standard data block in the [**WINBIO\_BIR**](winbio-bir.md) structure.</span></span> <span data-ttu-id="82b51-177">**WINBIO \_ 註冊的 \_ 格式** 成員不可以是零。</span><span class="sxs-lookup"><span data-stu-id="82b51-177">The **WINBIO\_REGISTERED\_FORMAT** members cannot be zero.</span></span> <span data-ttu-id="82b51-178">您可以使用下列常數來簡化錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="82b51-178">You can use the following constants to simplify error checking.</span></span>



| <span data-ttu-id="82b51-179">值</span><span class="sxs-lookup"><span data-stu-id="82b51-179">Value</span></span>                                                                                                                                                                                                                                                                                      | <span data-ttu-id="82b51-180">意義</span><span class="sxs-lookup"><span data-stu-id="82b51-180">Meaning</span></span>                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <span data-ttu-id="82b51-181"><dt>**WINBIO \_沒有 \_ 格式 \_ 擁有者 \_ 可用**</dt> <dt> ( (USHORT) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-181"><dt>**WINBIO\_NO\_FORMAT\_OWNER\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl> | <span data-ttu-id="82b51-182">未指定 IBIA (國際生物特徵辨識產業關聯) 指派的擁有者值。</span><span class="sxs-lookup"><span data-stu-id="82b51-182">No IBIA (International Biometric Industry Association) assigned owner value has been specified.</span></span><br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <span data-ttu-id="82b51-183"><dt>**WINBIO \_沒有 \_ 格式 \_ 類型 \_ 可用**</dt> <dt> ( (USHORT) 0)</dt></span><span class="sxs-lookup"><span data-stu-id="82b51-183"><dt>**WINBIO\_NO\_FORMAT\_TYPE\_AVAILABLE**</dt> <dt>((USHORT)0)</dt></span></span> </dl>    | <span data-ttu-id="82b51-184">未指定任何格式類型。</span><span class="sxs-lookup"><span data-stu-id="82b51-184">No format type has been specified.</span></span><br/>                                                              |



 

</dd> <dt>

<span data-ttu-id="82b51-185">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="82b51-185">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="82b51-186">[**WINBIO \_ 註冊的 \_ 格式**](winbio-registered-format.md)結構，指定在 BIR 中產生標準資料區塊之元件的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="82b51-186">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that specifies the product ID of the component that generated the standard data block in the BIR.</span></span> <span data-ttu-id="82b51-187">**WINBIO \_ 註冊的 \_ 格式** 成員可以是零。</span><span class="sxs-lookup"><span data-stu-id="82b51-187">The **WINBIO\_REGISTERED\_FORMAT** members can be zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82b51-188">備註</span><span class="sxs-lookup"><span data-stu-id="82b51-188">Remarks</span></span>

<span data-ttu-id="82b51-189">*子類型* 參數指定與生物特徵辨識資料相關聯的輔助因素。</span><span class="sxs-lookup"><span data-stu-id="82b51-189">The *Subtype* parameter specifies the sub-factor associated with the biometric data.</span></span> <span data-ttu-id="82b51-190">目前，Windows 生物特徵辨識架構 (WBF) 只支援指紋捕捉，並使用下列常數來表示子類型資訊：</span><span class="sxs-lookup"><span data-stu-id="82b51-190">Currently, the Windows Biometric Framework (WBF) supports only fingerprint capture and uses the following constants to represent sub-type information:</span></span>

-   <span data-ttu-id="82b51-191">WINBIO \_ ANSI \_ 381 \_ POS \_ 不明</span><span class="sxs-lookup"><span data-stu-id="82b51-191">WINBIO\_ANSI\_381\_POS\_UNKNOWN</span></span>
-   <span data-ttu-id="82b51-192">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB</span><span class="sxs-lookup"><span data-stu-id="82b51-192">WINBIO\_ANSI\_381\_POS\_RH\_THUMB</span></span>
-   <span data-ttu-id="82b51-193">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 食指 \_</span><span class="sxs-lookup"><span data-stu-id="82b51-193">WINBIO\_ANSI\_381\_POS\_RH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="82b51-194">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 中間 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-194">WINBIO\_ANSI\_381\_POS\_RH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="82b51-195">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 環形 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-195">WINBIO\_ANSI\_381\_POS\_RH\_RING\_FINGER</span></span>
-   <span data-ttu-id="82b51-196">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 小 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-196">WINBIO\_ANSI\_381\_POS\_RH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="82b51-197">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 經驗</span><span class="sxs-lookup"><span data-stu-id="82b51-197">WINBIO\_ANSI\_381\_POS\_LH\_THUMB</span></span>
-   <span data-ttu-id="82b51-198">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 索引 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-198">WINBIO\_ANSI\_381\_POS\_LH\_INDEX\_FINGER</span></span>
-   <span data-ttu-id="82b51-199">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 中間 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-199">WINBIO\_ANSI\_381\_POS\_LH\_MIDDLE\_FINGER</span></span>
-   <span data-ttu-id="82b51-200">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 環形 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-200">WINBIO\_ANSI\_381\_POS\_LH\_RING\_FINGER</span></span>
-   <span data-ttu-id="82b51-201">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 小 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-201">WINBIO\_ANSI\_381\_POS\_LH\_LITTLE\_FINGER</span></span>
-   <span data-ttu-id="82b51-202">WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ 四 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-202">WINBIO\_ANSI\_381\_POS\_RH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="82b51-203">WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ 四 \_ 手指</span><span class="sxs-lookup"><span data-stu-id="82b51-203">WINBIO\_ANSI\_381\_POS\_LH\_FOUR\_FINGERS</span></span>
-   <span data-ttu-id="82b51-204">WINBIO \_ ANSI \_ 381 \_ POS \_ 雙 \_ 拇指</span><span class="sxs-lookup"><span data-stu-id="82b51-204">WINBIO\_ANSI\_381\_POS\_TWO\_THUMBS</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="82b51-205">請勿嘗試驗證為 *子類型* 參數值提供的值。</span><span class="sxs-lookup"><span data-stu-id="82b51-205">Do not attempt to validate the value supplied for the *Subtype* parameter value.</span></span> <span data-ttu-id="82b51-206">Windows 生物識別服務會先驗證提供的值，再將其傳遞至您的實作為。</span><span class="sxs-lookup"><span data-stu-id="82b51-206">The Windows Biometrics Service will validate the supplied value before passing it through to your implementation.</span></span> <span data-ttu-id="82b51-207">如果值為 **WINBIO \_ 子類型 \_ NO \_ INFORMATION** 或 **WINBIO \_ 子類型 \_ ANY**，則在適當的位置驗證。</span><span class="sxs-lookup"><span data-stu-id="82b51-207">If the value is **WINBIO\_SUBTYPE\_NO\_INFORMATION** or **WINBIO\_SUBTYPE\_ANY**, then validate where appropriate.</span></span>

 

<span data-ttu-id="82b51-208">如果有任何一個位被判斷提示，表示 **WINBIO \_ BIR \_ 標頭** 結構的格式不正確。</span><span class="sxs-lookup"><span data-stu-id="82b51-208">If any of the following bits are asserted, the **WINBIO\_BIR\_HEADER** structure is not correctly formed.</span></span>


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a><span data-ttu-id="82b51-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="82b51-209">Requirements</span></span>



| <span data-ttu-id="82b51-210">需求</span><span class="sxs-lookup"><span data-stu-id="82b51-210">Requirement</span></span> | <span data-ttu-id="82b51-211">值</span><span class="sxs-lookup"><span data-stu-id="82b51-211">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82b51-212">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82b51-212">Minimum supported client</span></span><br/> | <span data-ttu-id="82b51-213">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b51-213">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="82b51-214">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82b51-214">Minimum supported server</span></span><br/> | <span data-ttu-id="82b51-215">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="82b51-215">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="82b51-216">標頭</span><span class="sxs-lookup"><span data-stu-id="82b51-216">Header</span></span><br/>                   | <dl> <span data-ttu-id="82b51-217"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="82b51-217"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82b51-218">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82b51-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82b51-219">用戶端應用程式結構</span><span class="sxs-lookup"><span data-stu-id="82b51-219">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="82b51-220">**WINBIO \_ 生物特徵辨識 \_ 子類型常數**</span><span class="sxs-lookup"><span data-stu-id="82b51-220">**WINBIO\_BIOMETRIC\_SUBTYPE Constants**</span></span>](winbio-biometric-subtype-constants.md)
</dt> <dt>

[<span data-ttu-id="82b51-221">**WINBIO \_ BIR**</span><span class="sxs-lookup"><span data-stu-id="82b51-221">**WINBIO\_BIR**</span></span>](winbio-bir.md)
</dt> <dt>

[<span data-ttu-id="82b51-222">**WINBIO \_ BIR \_ 資料 \_ 旗標常數**</span><span class="sxs-lookup"><span data-stu-id="82b51-222">**WINBIO\_BIR\_DATA\_FLAGS Constants**</span></span>](winbio-bir-data-flags-constants.md)
</dt> <dt>

[<span data-ttu-id="82b51-223">**WINBIO \_ BIR \_ 欄位常數**</span><span class="sxs-lookup"><span data-stu-id="82b51-223">**WINBIO\_BIR\_FIELD Constants**</span></span>](winbio-bir-field-constants.md)
</dt> <dt>

[<span data-ttu-id="82b51-224">**WINBIO \_ BIR \_ 用途常數**</span><span class="sxs-lookup"><span data-stu-id="82b51-224">**WINBIO\_BIR\_PURPOSE Constants**</span></span>](winbio-bir-purpose-constants.md)
</dt> <dt>

[<span data-ttu-id="82b51-225">**WINBIO \_ BIR \_ 品質常數**</span><span class="sxs-lookup"><span data-stu-id="82b51-225">**WINBIO\_BIR\_QUALITY Constants**</span></span>](winbio-bir-quality-constants.md)
</dt> <dt>

[<span data-ttu-id="82b51-226">**WINBIO \_ BIR \_ 版本常數**</span><span class="sxs-lookup"><span data-stu-id="82b51-226">**WINBIO\_BIR\_VERSION Constants**</span></span>](winbio-bir-version-constants.md)
</dt> </dl>

 

 





