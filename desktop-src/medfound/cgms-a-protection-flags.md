---
description: 指定複製產生管理系統的保護層級&\# 8212;類比 (CGMS-) 。
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: 'CGMS-保護旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386048"
---
# <a name="cgms-a-protection-flags"></a><span data-ttu-id="f46a6-103">CGMS-保護旗標</span><span class="sxs-lookup"><span data-stu-id="f46a6-103">CGMS-A Protection Flags</span></span>

<span data-ttu-id="f46a6-104">下表中的常數指定複製產生管理系統類比 (CGMS-A) 的保護層級。</span><span class="sxs-lookup"><span data-stu-id="f46a6-104">The constants in the following table specify the protection levels for Copy Generation Management System Analog (CGMS-A).</span></span>



| <span data-ttu-id="f46a6-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="f46a6-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="f46a6-106">Description</span><span class="sxs-lookup"><span data-stu-id="f46a6-106">Description</span></span>                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <span data-ttu-id="f46a6-107"><dt>**OPM \_CGMSA \_ OFF**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-107"><dt>**OPM\_CGMSA\_OFF**</dt> <dt>0x00</dt></span></span> </dl>                                                                                       | <span data-ttu-id="f46a6-108">CGMS-A 已停用。</span><span class="sxs-lookup"><span data-stu-id="f46a6-108">CGMS-A is disabled.</span></span> <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <span data-ttu-id="f46a6-109"><dt>**OPM \_CGMSA \_ \_ 免費複製**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-109"><dt>**OPM\_CGMSA\_COPY\_FREELY**</dt> <dt>0x01</dt></span></span> </dl>                                                              | <span data-ttu-id="f46a6-110">保護層級會自由複製。</span><span class="sxs-lookup"><span data-stu-id="f46a6-110">The protection level is Copy Freely.</span></span><br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <span data-ttu-id="f46a6-111"><dt>**OPM \_CGMSA \_ 複製 \_ 不再 \_**</dt>有 <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-111"><dt>**OPM\_CGMSA\_COPY\_NO\_MORE**</dt> <dt>0x02</dt></span></span> </dl>                                                          | <span data-ttu-id="f46a6-112">保護層級將不再複製。</span><span class="sxs-lookup"><span data-stu-id="f46a6-112">The protection level is Copy No More.</span></span> <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <span data-ttu-id="f46a6-113"><dt>**OPM \_CGMSA \_ 複製 \_ 一 \_ 代**</dt> <dt>0x03</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-113"><dt>**OPM\_CGMSA\_COPY\_ONE\_GENERATION**</dt> <dt>0x03</dt></span></span> </dl>                                     | <span data-ttu-id="f46a6-114">保護層級會複製1代。</span><span class="sxs-lookup"><span data-stu-id="f46a6-114">The protection level is Copy One Generation.</span></span> <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <span data-ttu-id="f46a6-115"><dt>**OPM \_CGMSA \_ 複製 \_ 永不**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-115"><dt>**OPM\_CGMSA\_COPY\_NEVER**</dt> <dt>0x04</dt></span></span> </dl>                                                                 | <span data-ttu-id="f46a6-116">保護層級為 [永遠複製]。</span><span class="sxs-lookup"><span data-stu-id="f46a6-116">The protection level is Copy Never.</span></span><br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <span data-ttu-id="f46a6-117"><dt>**OPM \_\_ \_ \_ 需要 CGMSA**</dt>重新發佈控制項 <dt>0x08</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-117"><dt>**OPM\_CGMSA\_REDISTRIBUTION\_CONTROL\_REQUIRED**</dt> <dt>0x08</dt></span></span> </dl> | <span data-ttu-id="f46a6-118">轉散發控制 (也稱為「 *廣播旗* 標」，) 是必要的。</span><span class="sxs-lookup"><span data-stu-id="f46a6-118">Redistribution control (also called the *broadcast flag*) is required.</span></span> <span data-ttu-id="f46a6-119">此旗標可以與其他旗標合併。</span><span class="sxs-lookup"><span data-stu-id="f46a6-119">This flag can be combined with the other flags.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f46a6-120">備註</span><span class="sxs-lookup"><span data-stu-id="f46a6-120">Remarks</span></span>

<span data-ttu-id="f46a6-121">這些旗標相當於認證輸出保護通訊協定中使用的 **COPP \_ CGMSA \_ 保護 \_ 層級** 列舉常數 (COPP) 。</span><span class="sxs-lookup"><span data-stu-id="f46a6-121">These flags are equivalent to the **COPP\_CGMSA\_Protection\_Level** enumeration constants used in the Certified Output Protection Protocol (COPP).</span></span>

## <a name="requirements"></a><span data-ttu-id="f46a6-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f46a6-122">Requirements</span></span>



| <span data-ttu-id="f46a6-123">需求</span><span class="sxs-lookup"><span data-stu-id="f46a6-123">Requirement</span></span> | <span data-ttu-id="f46a6-124">值</span><span class="sxs-lookup"><span data-stu-id="f46a6-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f46a6-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f46a6-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f46a6-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f46a6-126">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f46a6-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f46a6-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f46a6-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f46a6-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f46a6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f46a6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f46a6-130"><dt>Opmapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="f46a6-130"><dt>Opmapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f46a6-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f46a6-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46a6-132">媒體基礎常數</span><span class="sxs-lookup"><span data-stu-id="f46a6-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




