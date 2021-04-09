---
title: 'WINBIO_BIR_PURPOSE 常數 (Winbio \_ 類型 .h) '
description: 指定 (BIR) 預定或適用的生物特徵辨識資訊記錄用途。
ms.assetid: AAFD3203-4D3D-43B5-A833-1258E1E281D3
topic_type:
- apiref
api_name:
- WINBIO_NO_PURPOSE_AVAILABLE
- WINBIO_PURPOSE_VERIFY
- WINBIO_PURPOSE_IDENTIFY
- WINBIO_PURPOSE_ENROLL
- WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION
- WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION
- WINBIO_PURPOSE_AUDIT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5a662a5ae045d3afc631f93cdf296508dabccf9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934432"
---
# <a name="winbio_bir_purpose-constants"></a><span data-ttu-id="5a842-103">WINBIO \_ BIR \_ 用途常數</span><span class="sxs-lookup"><span data-stu-id="5a842-103">WINBIO\_BIR\_PURPOSE Constants</span></span>

<span data-ttu-id="5a842-104">[**WINBIO \_ BIR \_ 標頭**](winbio-bir-header.md)結構的 **目的** 成員會使用下列旗標，來指定要將生物特徵辨識資訊記錄 (BIR) 預定或適用的用途。</span><span class="sxs-lookup"><span data-stu-id="5a842-104">The following flags are used by the **Purpose** member of the [**WINBIO\_BIR\_HEADER**](winbio-bir-header.md) structure to specify the purpose for which the biometric information record (BIR) is intended or for which it is suitable.</span></span>



| <span data-ttu-id="5a842-105">常數</span><span class="sxs-lookup"><span data-stu-id="5a842-105">Constant</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="5a842-106">描述</span><span class="sxs-lookup"><span data-stu-id="5a842-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_PURPOSE_AVAILABLE"></span><span id="winbio_no_purpose_available"></span><dl> <span data-ttu-id="5a842-107"><dt>**WINBIO \_ 沒有 \_ 任何 \_ 可用的用途**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-107"><dt>**WINBIO\_NO\_PURPOSE\_AVAILABLE**</dt></span></span> </dl>                                         | <span data-ttu-id="5a842-108">未指定任何用途。</span><span class="sxs-lookup"><span data-stu-id="5a842-108">No purpose is specified.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="WINBIO_PURPOSE_VERIFY"></span><span id="winbio_purpose_verify"></span><dl> <span data-ttu-id="5a842-109"><dt>**WINBIO \_ 用途 \_ 驗證**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-109"><dt>**WINBIO\_PURPOSE\_VERIFY**</dt></span></span> </dl>                                                            | <span data-ttu-id="5a842-110">驗證使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="5a842-110">Verify the identity of a user.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_IDENTIFY"></span><span id="winbio_purpose_identify"></span><dl> <span data-ttu-id="5a842-111"><dt>**WINBIO \_ 目的 \_ 識別**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-111"><dt>**WINBIO\_PURPOSE\_IDENTIFY**</dt></span></span> </dl>                                                      | <span data-ttu-id="5a842-112">識別使用者。</span><span class="sxs-lookup"><span data-stu-id="5a842-112">Identify a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="WINBIO_PURPOSE_ENROLL"></span><span id="winbio_purpose_enroll"></span><dl> <span data-ttu-id="5a842-113"><dt>**WINBIO \_ 目的 \_ 註冊**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-113"><dt>**WINBIO\_PURPOSE\_ENROLL**</dt></span></span> </dl>                                                            | <span data-ttu-id="5a842-114">註冊使用者。</span><span class="sxs-lookup"><span data-stu-id="5a842-114">Enroll a user.</span></span><br/>                                                                                                                                                                                                                                                                                                                   |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_VERIFICATION"></span><span id="winbio_purpose_enroll_for_verification"></span><dl> <span data-ttu-id="5a842-115"><dt>**WINBIO \_ 目的 \_ 註冊 \_ 以進行 \_ 驗證**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-115"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_VERIFICATION**</dt></span></span> </dl>       | <span data-ttu-id="5a842-116">捕捉生物特徵辨識範例，並判斷範例是否對應到指定的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="5a842-116">Capture a biometric sample and determine whether the sample corresponds to the specified user identity.</span></span><br/>                                                                                                                                                                                                                          |
| <span id="WINBIO_PURPOSE_ENROLL_FOR_IDENTIFICATION"></span><span id="winbio_purpose_enroll_for_identification"></span><dl> <span data-ttu-id="5a842-117"><dt>**WINBIO \_ 目的 \_ 註冊 \_ 以供 \_ 識別**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-117"><dt>**WINBIO\_PURPOSE\_ENROLL\_FOR\_IDENTIFICATION**</dt></span></span> </dl> | <span data-ttu-id="5a842-118">捕捉生物特徵辨識範例，並判斷它是否符合現有的生物特徵辨識範本。</span><span class="sxs-lookup"><span data-stu-id="5a842-118">Capture a biometric sample and determine whether it matches an existing biometric template.</span></span><br/>                                                                                                                                                                                                                                      |
| <span id="WINBIO_PURPOSE_AUDIT"></span><span id="winbio_purpose_audit"></span><dl> <span data-ttu-id="5a842-119"><dt>**WINBIO \_ 目的 \_ 審核**</dt></span><span class="sxs-lookup"><span data-stu-id="5a842-119"><dt>**WINBIO\_PURPOSE\_AUDIT**</dt></span></span> </dl>                                                               | <span data-ttu-id="5a842-120">可以用來記錄或顯示的額外資訊。</span><span class="sxs-lookup"><span data-stu-id="5a842-120">Extra information that can be used for logging or for display.</span></span> <span data-ttu-id="5a842-121">所有函數的輸入都會忽略此值。</span><span class="sxs-lookup"><span data-stu-id="5a842-121">This value is ignored on input by all functions.</span></span> <span data-ttu-id="5a842-122">在輸出中，它只有在可辨識設備支援的情況下才可使用，而且您會在 [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)函數的 *Flags* 參數中指定 **\_ RAW WINBIO 資料 \_ 旗 \_** 標。</span><span class="sxs-lookup"><span data-stu-id="5a842-122">On output, it will only be available if supported by the biometric unit and you specify **WINBIO\_DATA\_FLAG\_RAW** in the *Flags* parameter of the [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample) function.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5a842-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a842-123">Requirements</span></span>



| <span data-ttu-id="5a842-124">需求</span><span class="sxs-lookup"><span data-stu-id="5a842-124">Requirement</span></span> | <span data-ttu-id="5a842-125">值</span><span class="sxs-lookup"><span data-stu-id="5a842-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a842-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a842-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5a842-127">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a842-127">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="5a842-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a842-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5a842-129">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a842-129">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="5a842-130">標頭</span><span class="sxs-lookup"><span data-stu-id="5a842-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a842-131"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="5a842-131"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a842-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a842-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a842-133">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="5a842-133">Client Application Constants</span></span>](client-application-constants.md)
</dt> <dt>

[<span data-ttu-id="5a842-134">**WINBIO \_ BIR \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="5a842-134">**WINBIO\_BIR\_HEADER**</span></span>](winbio-bir-header.md)
</dt> </dl>

 

 





