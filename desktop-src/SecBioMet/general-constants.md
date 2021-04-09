---
title: '一般常數 (Winbio \_ 類型 .h) '
description: 指定最大 SID 長度、控制碼、識別碼、最大字串長度，以及最大範例緩衝區大小。
ms.assetid: 62e87bd8-a708-4d00-aaa8-9cac8e3736a7
topic_type:
- apiref
api_name:
- SECURITY_MAX_SID_SIZE
- WINBIO_UNIT_ID
- WINBIO_SESSION_HANDLE
- WINBIO_FRAMEWORK_HANDLE
- WINBIO_UUID
- WINBIO_STRING
- WINBIO_MAX_STRING_LEN
- WINBIO_MAX_SAMPLE_BUFFER_SIZE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5e35aa4c2cc676935cfb80fdec8729daf64d5f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934373"
---
# <a name="general-constants-winbio_typesh"></a><span data-ttu-id="2f9e1-103">一般常數 (Winbio \_ 類型 .h) </span><span class="sxs-lookup"><span data-stu-id="2f9e1-103">General Constants (Winbio\_types.h)</span></span>

<span data-ttu-id="2f9e1-104">整個 Windows 生物特徵辨識架構都會使用下列常數。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-104">The following constants are used throughout the Windows Biometric Framework.</span></span>



| <span data-ttu-id="2f9e1-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="2f9e1-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="2f9e1-106">Description</span><span class="sxs-lookup"><span data-stu-id="2f9e1-106">Description</span></span>                                                                                 |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| <span id="SECURITY_MAX_SID_SIZE"></span><span id="security_max_sid_size"></span><dl> <span data-ttu-id="2f9e1-107"><dt>**安全性 \_ 最大 \_ SID \_ 大小**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-107"><dt>**SECURITY\_MAX\_SID\_SIZE**</dt></span></span> </dl>                                                                                          | <span data-ttu-id="2f9e1-108">安全識別碼 (SID) 值的最大長度。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-108">The maximum length of a security identifier (SID) value.</span></span> <span data-ttu-id="2f9e1-109">目前這是68。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-109">Currently this is 68.</span></span><br/>   |
| <span id="WINBIO_UNIT_ID"></span><span id="winbio_unit_id"></span><dl> <span data-ttu-id="2f9e1-110"><dt>**WINBIO \_ 單位 \_ 識別碼**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-110"><dt>**WINBIO\_UNIT\_ID**</dt></span></span> </dl>                                                                                                                | <span data-ttu-id="2f9e1-111">生物識別單位的識別碼。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-111">ID number of a biometric unit.</span></span><br/>                                                   |
| <span id="WINBIO_SESSION_HANDLE"></span><span id="winbio_session_handle"></span><dl> <span data-ttu-id="2f9e1-112"><dt>**WINBIO \_ 會話 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-112"><dt>**WINBIO\_SESSION\_HANDLE**</dt></span></span> </dl>                                                                                           | <span data-ttu-id="2f9e1-113">不帶正負號的長整數，其中包含開啟生物特徵辨識會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-113">An unsigned long integer that contains the handle for an open biometric session.</span></span><br/> |
| <span id="WINBIO_FRAMEWORK_HANDLE"></span><span id="winbio_framework_handle"></span><dl> <span data-ttu-id="2f9e1-114"><dt>**WINBIO \_ 架構 \_ 控制碼**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-114"><dt>**WINBIO\_FRAMEWORK\_HANDLE**</dt></span></span> </dl>                                                                                     | <span data-ttu-id="2f9e1-115">不帶正負號的長整數，其中包含開啟架構會話的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-115">An unsigned long integer that contains the handle for an open framework session.</span></span><br/> |
| <span id="WINBIO_UUID"></span><span id="winbio_uuid"></span><dl> <span data-ttu-id="2f9e1-116"><dt>**WINBIO \_ UUID**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-116"><dt>**WINBIO\_UUID**</dt></span></span> </dl>                                                                                                                          | <span data-ttu-id="2f9e1-117">GUID。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-117">A GUID.</span></span><br/>                                                                          |
| <span id="WINBIO_STRING"></span><span id="winbio_string"></span><dl> <span data-ttu-id="2f9e1-118"><dt>**WINBIO \_ 字串**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-118"><dt>**WINBIO\_STRING**</dt></span></span> </dl>                                                                                                                    | <span data-ttu-id="2f9e1-119">位元組陣列，其中包含以 null 終止的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-119">A byte array that contains a null-terminated Unicode string.</span></span><br/>                     |
| <span id="WINBIO_MAX_STRING_LEN_"></span><span id="winbio_max_string_len_"></span><dl> <span data-ttu-id="2f9e1-120"><dt>**WINBIO \_最大 \_ 字串 \_ 長度**</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-120"><dt>**WINBIO\_MAX\_STRING\_LEN** </dt></span></span> </dl>                                                                                       | <span data-ttu-id="2f9e1-121">**WINBIO \_ 字串** 值的最大長度。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-121">The maximum length of a **WINBIO\_STRING** value.</span></span> <span data-ttu-id="2f9e1-122">目前這是256。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-122">Currently this is 256.</span></span><br/>         |
| <span id="WINBIO_MAX_SAMPLE_BUFFER_SIZE"></span><span id="winbio_max_sample_buffer_size"></span><dl> <span data-ttu-id="2f9e1-123"><dt>**WINBIO \_最大 \_ 範例 \_ 緩衝區 \_ 大小**</dt> <dt>0x7fffffff</dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-123"><dt>**WINBIO\_MAX\_SAMPLE\_BUFFER\_SIZE**</dt> <dt>0x7FFFFFFF</dt></span></span> </dl> | <span data-ttu-id="2f9e1-124">單一生物特徵辨識資料捕捉中的最大位元組數目。</span><span class="sxs-lookup"><span data-stu-id="2f9e1-124">The maximum number of bytes in a single biometric data capture.</span></span><br/>                  |



## <a name="requirements"></a><span data-ttu-id="2f9e1-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f9e1-125">Requirements</span></span>



| <span data-ttu-id="2f9e1-126">需求</span><span class="sxs-lookup"><span data-stu-id="2f9e1-126">Requirement</span></span> | <span data-ttu-id="2f9e1-127">值</span><span class="sxs-lookup"><span data-stu-id="2f9e1-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f9e1-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2f9e1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2f9e1-129">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f9e1-129">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="2f9e1-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2f9e1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2f9e1-131">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2f9e1-131">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="2f9e1-132">標頭</span><span class="sxs-lookup"><span data-stu-id="2f9e1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f9e1-133"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="2f9e1-133"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f9e1-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f9e1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f9e1-135">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="2f9e1-135">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





