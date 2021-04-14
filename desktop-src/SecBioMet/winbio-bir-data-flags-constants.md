---
title: 'WINBIO_BIR_DATA_FLAGS 常數 (Winbio \_ 類型 .h) '
description: 指定資料的條件。
ms.assetid: F6F7F68A-3294-4AF8-A1A7-C6A869A2CC3C
topic_type:
- apiref
api_name:
- WINBIO_DATA_FLAG_PRIVACY
- WINBIO_DATA_FLAG_INTEGRITY
- WINBIO_DATA_FLAG_SIGNED
- WINBIO_DATA_FLAG_RAW
- WINBIO_DATA_FLAG_INTERMEDIATE
- WINBIO_DATA_FLAG_PROCESSED
- WINBIO_DATA_FLAG_OPTION_MASK_PRESENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8195cf17040c35b9e42f8977b36c5ddc6f2ea33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385262"
---
# <a name="winbio_bir_data_flags-constants"></a><span data-ttu-id="e2a24-103">WINBIO \_ BIR \_ 資料 \_ 旗標常數</span><span class="sxs-lookup"><span data-stu-id="e2a24-103">WINBIO\_BIR\_DATA\_FLAGS Constants</span></span>

<span data-ttu-id="e2a24-104">[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **DataFlags** 成員會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="e2a24-104">The following constants are used by the **DataFlags** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure.</span></span>



| <span data-ttu-id="e2a24-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="e2a24-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="e2a24-106">Description</span><span class="sxs-lookup"><span data-stu-id="e2a24-106">Description</span></span>                                                                                                                                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <span data-ttu-id="e2a24-107"><dt>**WINBIO \_資料 \_ 旗標 \_ 隱私權**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-107"><dt>**WINBIO\_DATA\_FLAG\_PRIVACY**</dt> <dt>0x02</dt></span></span> </dl>                                       | <span data-ttu-id="e2a24-108">資料已加密。</span><span class="sxs-lookup"><span data-stu-id="e2a24-108">The data is encrypted.</span></span><br/>                                                                                                                                                                                 |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <span data-ttu-id="e2a24-109"><dt>**WINBIO \_資料 \_ 旗標 \_ 完整性**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-109"><dt>**WINBIO\_DATA\_FLAG\_INTEGRITY**</dt> <dt>0x01</dt></span></span> </dl>                                 | <span data-ttu-id="e2a24-110">資料會經過數位簽署，或由 (MAC) 的訊息驗證代碼保護。</span><span class="sxs-lookup"><span data-stu-id="e2a24-110">The data is digitally signed or is protected by a message authentication code (MAC).</span></span><br/>                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <span data-ttu-id="e2a24-111"><dt>**WINBIO \_資料 \_ 旗標 \_ 已簽署**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-111"><dt>**WINBIO\_DATA\_FLAG\_SIGNED**</dt> <dt>0x04</dt></span></span> </dl>                                          | <span data-ttu-id="e2a24-112">如果設定此旗標和 **WINBIO \_ 資料旗標 \_ \_ 完整性** 旗標，則會簽署資料。</span><span class="sxs-lookup"><span data-stu-id="e2a24-112">If this flag and the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag are set, the data is signed.</span></span> <span data-ttu-id="e2a24-113">如果未設定此旗標，但已設定 **WINBIO \_ 資料 \_ 旗標 \_ 完整性** 旗標，則會計算資料的 MAC。</span><span class="sxs-lookup"><span data-stu-id="e2a24-113">If this flag is not set but the **WINBIO\_DATA\_FLAG\_INTEGRITY** flag is set, a MAC is computed on the data.</span></span><br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <span data-ttu-id="e2a24-114"><dt>**WINBIO \_資料 \_ 旗標 \_ 原始**</dt> <dt>0x20</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-114"><dt>**WINBIO\_DATA\_FLAG\_RAW**</dt> <dt>0x20</dt></span></span> </dl>                                                   | <span data-ttu-id="e2a24-115">資料的格式與捕捉的格式一樣。</span><span class="sxs-lookup"><span data-stu-id="e2a24-115">The data is in the format with which it was captured.</span></span><br/>                                                                                                                                                  |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <span data-ttu-id="e2a24-116"><dt>**WINBIO \_資料 \_ 旗標 \_ 中繼**</dt> <dt>0x40</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-116"><dt>**WINBIO\_DATA\_FLAG\_INTERMEDIATE**</dt> <dt>0x40</dt></span></span> </dl>                        | <span data-ttu-id="e2a24-117">資料不是原始資料，但尚未完全處理。</span><span class="sxs-lookup"><span data-stu-id="e2a24-117">The data is not raw but has not been completely processed.</span></span><br/>                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <span data-ttu-id="e2a24-118"><dt>**WINBIO \_已 \_ \_ 處理的資料旗**</dt>標 <dt>0x80</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-118"><dt>**WINBIO\_DATA\_FLAG\_PROCESSED**</dt> <dt>0x80</dt></span></span> </dl>                                 | <span data-ttu-id="e2a24-119">已處理資料。</span><span class="sxs-lookup"><span data-stu-id="e2a24-119">The data has been processed.</span></span><br/>                                                                                                                                                                           |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <span data-ttu-id="e2a24-120"><dt>**WINBIO \_資料 \_ 旗標 \_ 選項 \_ 遮罩 \_ 存在**</dt> <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-120"><dt>**WINBIO\_DATA\_FLAG\_OPTION\_MASK\_PRESENT**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="e2a24-121">旗標遮罩。</span><span class="sxs-lookup"><span data-stu-id="e2a24-121">The flag mask.</span></span> <span data-ttu-id="e2a24-122">此值一律為一個 (1) 。</span><span class="sxs-lookup"><span data-stu-id="e2a24-122">This value is always one (1).</span></span><br/>                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="e2a24-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2a24-123">Requirements</span></span>



| <span data-ttu-id="e2a24-124">需求</span><span class="sxs-lookup"><span data-stu-id="e2a24-124">Requirement</span></span> | <span data-ttu-id="e2a24-125">值</span><span class="sxs-lookup"><span data-stu-id="e2a24-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a24-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2a24-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e2a24-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2a24-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="e2a24-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2a24-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e2a24-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2a24-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e2a24-130">標頭</span><span class="sxs-lookup"><span data-stu-id="e2a24-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2a24-131"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="e2a24-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2a24-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2a24-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2a24-133">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="e2a24-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





