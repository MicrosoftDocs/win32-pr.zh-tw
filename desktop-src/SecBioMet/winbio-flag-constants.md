---
title: 'WINBIO_FLAG 常數 (Winbio \_ 類型 .h) '
description: 指定新會話的生物特徵辨識單位設定和存取特性。
ms.assetid: 82b57023-6c27-433d-bf13-f136f501fc60
topic_type:
- apiref
api_name:
- WINBIO_FLAG_DEFAULT
- WINBIO_FLAG_BASIC
- WINBIO_FLAG_ADVANCED
- WINBIO_FLAG_RAW
- WINBIO_FLAG_MAINTENANCE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ed632b5f15cc3d6a7ac6b0c6c70a2b3431b73db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384114"
---
# <a name="winbio_flag-constants"></a><span data-ttu-id="a7b6e-103">WINBIO \_ 旗標常數</span><span class="sxs-lookup"><span data-stu-id="a7b6e-103">WINBIO\_FLAG Constants</span></span>

<span data-ttu-id="a7b6e-104">下列常數可以用在 [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) 函式中，以指定新會話的生物特徵辨識單位設定和存取特性。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-104">The following constants can be used in the [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) function to specify biometric unit configuration and access characteristics for the new session.</span></span>



| <span data-ttu-id="a7b6e-105">常數</span><span class="sxs-lookup"><span data-stu-id="a7b6e-105">Constant</span></span>                                                                                                                                                                                     | <span data-ttu-id="a7b6e-106">描述</span><span class="sxs-lookup"><span data-stu-id="a7b6e-106">Description</span></span>                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FLAG_DEFAULT"></span><span id="winbio_flag_default"></span><dl> <span data-ttu-id="a7b6e-107"><dt>**WINBIO \_ 旗標 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b6e-107"><dt>**WINBIO\_FLAG\_DEFAULT**</dt></span></span> </dl>             | <span data-ttu-id="a7b6e-108">感應器設定旗標。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-108">Sensor configuration flag.</span></span> <span data-ttu-id="a7b6e-109">生物識別單位的運作方式是在安裝期間指定。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-109">The biometric units operate in the manner specified during installation.</span></span><br/>                                                                           |
| <span id="WINBIO_FLAG_BASIC"></span><span id="winbio_flag_basic"></span><dl> <span data-ttu-id="a7b6e-110"><dt>**WINBIO \_ 旗標 \_ 基本**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b6e-110"><dt>**WINBIO\_FLAG\_BASIC**</dt></span></span> </dl>                   | <span data-ttu-id="a7b6e-111">感應器設定旗標。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-111">Sensor configuration flag.</span></span> <span data-ttu-id="a7b6e-112">生物識別單位只會以基本的擷取裝置運作。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-112">The biometric units operate only as basic capture devices.</span></span><br/>                                                                                         |
| <span id="WINBIO_FLAG_ADVANCED"></span><span id="winbio_flag_advanced"></span><dl> <span data-ttu-id="a7b6e-113"><dt>**WINBIO \_ 旗標 \_ ADVANCED**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b6e-113"><dt>**WINBIO\_FLAG\_ADVANCED**</dt></span></span> </dl>          | <span data-ttu-id="a7b6e-114">感應器設定旗標。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-114">Sensor configuration flag.</span></span> <span data-ttu-id="a7b6e-115">生物識別單位使用內部處理和儲存功能。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-115">The biometric units use internal processing and storage capabilities.</span></span><br/>                                                                              |
| <span id="WINBIO_FLAG_RAW"></span><span id="winbio_flag_raw"></span><dl> <span data-ttu-id="a7b6e-116"><dt>**WINBIO \_ 旗標 \_ 原始**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b6e-116"><dt>**WINBIO\_FLAG\_RAW**</dt></span></span> </dl>                         | <span data-ttu-id="a7b6e-117">所需的存取旗標。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-117">Desired access flag.</span></span> <span data-ttu-id="a7b6e-118">用戶端應用程式會使用 [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)來捕捉原始的生物特徵辨識資料。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-118">The client application captures raw biometric data using [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span><br/>                                             |
| <span id="WINBIO_FLAG_MAINTENANCE"></span><span id="winbio_flag_maintenance"></span><dl> <span data-ttu-id="a7b6e-119"><dt>**WINBIO \_ 旗標 \_ 維護**</dt></span><span class="sxs-lookup"><span data-stu-id="a7b6e-119"><dt>**WINBIO\_FLAG\_MAINTENANCE**</dt></span></span> </dl> | <span data-ttu-id="a7b6e-120">所需的存取旗標。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-120">Desired access flag.</span></span> <span data-ttu-id="a7b6e-121">用戶端會呼叫 [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)，以在生物特徵辨識單位上執行廠商定義的控制作業。</span><span class="sxs-lookup"><span data-stu-id="a7b6e-121">The client performs vendor-defined control operations on a biometric unit by calling [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a7b6e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="a7b6e-122">Requirements</span></span>



| <span data-ttu-id="a7b6e-123">需求</span><span class="sxs-lookup"><span data-stu-id="a7b6e-123">Requirement</span></span> | <span data-ttu-id="a7b6e-124">值</span><span class="sxs-lookup"><span data-stu-id="a7b6e-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7b6e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a7b6e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a7b6e-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7b6e-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a7b6e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a7b6e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a7b6e-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a7b6e-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a7b6e-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a7b6e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7b6e-130"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a7b6e-130"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7b6e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a7b6e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7b6e-132">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="a7b6e-132">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





