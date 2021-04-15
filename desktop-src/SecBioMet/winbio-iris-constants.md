---
title: 'WINBIO_IRIS 常數 (Winbio \_ 類型 .h) '
description: 指定鳶尾花辨識的型別。
ms.assetid: B1A594E3-6DEA-4071-B40F-569B8094E801
topic_type:
- apiref
api_name:
- WINBIO_IRIS_TYPE_UNKNOWN
- WINBIO_IRIS_LEFT_EYE
- WINBIO_IRIS_RIGHT_EYE
- WINBIO_IRIS_UNSPECIFIED_POS_01
- WINBIO_IRIS_UNSPECIFIED_POS_02
- WINBIO_IRIS_BOTH_EYES
- WINBIO_IRIS_EITHER_EYE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61e65505b8ef55b0fdc2dc9d8f5312e24856602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465824"
---
# <a name="winbio_iris-constants"></a><span data-ttu-id="0fd6d-103">WINBIO \_ 鳶尾花常數</span><span class="sxs-lookup"><span data-stu-id="0fd6d-103">WINBIO\_IRIS Constants</span></span>

<span data-ttu-id="0fd6d-104">下列常數是 **WINBIO \_ 生物特徵 \_ 子類型** 值，可用來指定超過 ANSI INCITS 379-2004 的鳶尾花辨識類型：「鳶尾花影像交換格式」，這不會定義任何左/右眼睛值：</span><span class="sxs-lookup"><span data-stu-id="0fd6d-104">The following constants are **WINBIO\_BIOMETRIC\_SUBTYPE** values that can be used to specify the types for iris recognition beyond ANSI INCITS 379-2004: "Iris Image Interchange Format", which does not define any left/right eye values:</span></span>



| <span data-ttu-id="0fd6d-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="0fd6d-105">Constant/value</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="0fd6d-106">Description</span><span class="sxs-lookup"><span data-stu-id="0fd6d-106">Description</span></span>                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <span data-ttu-id="0fd6d-107"><dt> **WINBIO \_ 鳶尾花 \_ 類型 \_ 未知**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-107"><dt>**WINBIO\_IRIS\_TYPE\_UNKNOWN** </dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="0fd6d-108">鳶尾花類型未知。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-108">The iris type is unknown.</span></span> <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <span data-ttu-id="0fd6d-109"><dt> **WINBIO \_ 鳶尾花 \_ 左方 \_ 眼睛**</dt> <dt>0xF5</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-109"><dt>**WINBIO\_IRIS\_LEFT\_EYE** </dt> <dt>0xF5 </dt></span></span> </dl>                               | <span data-ttu-id="0fd6d-110">鳶尾花類型是最左邊的眼睛。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-110">The iris type is the left eye.</span></span> <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <span data-ttu-id="0fd6d-111"><dt> **WINBIO \_ 鳶尾花 \_ RIGHT \_ 眼睛**</dt> <dt>0xF6</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-111"><dt>**WINBIO\_IRIS\_RIGHT\_EYE** </dt> <dt>0xF6 </dt></span></span> </dl>                            | <span data-ttu-id="0fd6d-112">鳶尾花型別是正確的眼睛。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-112">The iris type is the right eye.</span></span> <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <span data-ttu-id="0fd6d-113"><dt>**WINBIO \_鳶尾花 \_ 未指定的 \_ POS \_ 01**</dt> <dt>0xF7</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-113"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_01**</dt> <dt>0xF7</dt></span></span> </dl>    | <span data-ttu-id="0fd6d-114">當只有一眼時，與使用者第一個範本相關聯的子類型是相機框架，無法判斷是否為使用者的左邊或右邊。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-114">Subtype associated with a user s first template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <span data-ttu-id="0fd6d-115"><dt> **WINBIO \_ 鳶尾花 \_ 未指定的 \_ POS \_ 02**</dt> <dt>0xF8</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-115"><dt>**WINBIO\_IRIS\_UNSPECIFIED\_POS\_02** </dt> <dt>0xF8</dt></span></span> </dl> | <span data-ttu-id="0fd6d-116">當只有一眼時，與使用者第二個範本相關聯的子類型是相機框架，無法判斷是否為使用者的左邊或右邊。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-116">Subtype associated with a user s second template when only one eye is camera frame and it cannot be determined whether it is the user s left or right eye.</span></span><br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <span data-ttu-id="0fd6d-117"><dt> **WINBIO \_ 鳶尾花 \_ 兩種 \_ 眼睛**</dt> <dt>0xF9</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-117"><dt>**WINBIO\_IRIS\_BOTH\_EYES** </dt> <dt>0xF9</dt></span></span> </dl>                             | <span data-ttu-id="0fd6d-118">鳶尾花類型都是眼睛。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-118">The iris type is both eyes.</span></span> <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <span data-ttu-id="0fd6d-119"><dt> **WINBIO \_ 鳶尾花 \_ \_**</dt> <dt>0xFA</dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-119"><dt>**WINBIO\_IRIS\_EITHER\_EYE** </dt> <dt>0xFA</dt></span></span> </dl>                          | <span data-ttu-id="0fd6d-120">鳶尾花類型可以是眼睛。</span><span class="sxs-lookup"><span data-stu-id="0fd6d-120">The iris type is either eye.</span></span> <br/>                                                                                                                              |



## <a name="requirements"></a><span data-ttu-id="0fd6d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="0fd6d-121">Requirements</span></span>



| <span data-ttu-id="0fd6d-122">需求</span><span class="sxs-lookup"><span data-stu-id="0fd6d-122">Requirement</span></span> | <span data-ttu-id="0fd6d-123">值</span><span class="sxs-lookup"><span data-stu-id="0fd6d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd6d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0fd6d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd6d-125">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fd6d-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="0fd6d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0fd6d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd6d-127">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0fd6d-127">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0fd6d-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0fd6d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd6d-129"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="0fd6d-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



 

 





