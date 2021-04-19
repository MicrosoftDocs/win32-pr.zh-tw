---
title: 'WINBIO_BIOMETRIC_TYPE 常數 (Winbio \_ 類型 .h) '
description: 美國國家標準與技術資訊局所定義的標準生物特徵辨識類型 (NISTIR) 6529-A，亦稱為一般生物特徵辨識交換格式架構 (CBEFF) Patron 格式 A。
ms.assetid: DCBDB5F9-FF81-44C1-B439-2B8C02483212
topic_type:
- apiref
api_name:
- WINBIO_STANDARD_TYPE_MASK
- WINBIO_NO_TYPE_AVAILABLE
- WINBIO_TYPE_MULTIPLE
- WINBIO_TYPE_FACIAL_FEATURES
- WINBIO_TYPE_VOICE
- WINBIO_TYPE_FINGERPRINT
- WINBIO_TYPE_IRIS
- WINBIO_TYPE_RETINA
- WINBIO_TYPE_HAND_GEOMETRY
- WINBIO_TYPE_SIGNATURE_DYNAMICS
- WINBIO_TYPE_KEYSTROKE_DYNAMICS
- WINBIO_TYPE_LIP_MOVEMENT
- WINBIO_TYPE_THERMAL_FACE_IMAGE
- WINBIO_TYPE_THERMAL_HAND_IMAGE
- WINBIO_TYPE_GAIT
- WINBIO_TYPE_SCENT
- WINBIO_TYPE_DNA
- WINBIO_TYPE_EAR_SHAPE
- WINBIO_TYPE_FINGER_GEOMETRY
- WINBIO_TYPE_PALM_PRINT
- WINBIO_TYPE_VEIN_PATTERN
- WINBIO_TYPE_FOOT_PRINT
- WINBIO_TYPE_OTHER
- WINBIO_TYPE_PASSWORD
- WINBIO_TYPE_ANY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d2ab5c41a3c2af26312c97a67d1179b50fd759
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969976"
---
# <a name="winbio_biometric_type-constants"></a><span data-ttu-id="74f6f-103">WINBIO \_ 生物特徵辨識 \_ 類型常數</span><span class="sxs-lookup"><span data-stu-id="74f6f-103">WINBIO\_BIOMETRIC\_TYPE Constants</span></span>

<span data-ttu-id="74f6f-104">下列常數代表國家/地區協會標準和技術資訊所定義的標準生物特徵辨識類型 (NISTIR) 6529-A，亦稱為一般生物特徵辨識交換格式架構 (CBEFF) Patron 格式 A。目前只支援 **WINBIO \_ 類型 \_ 指紋** 。</span><span class="sxs-lookup"><span data-stu-id="74f6f-104">The following constants represent the standard biometric types defined by National Institute of Standards and Technology Information (NISTIR) 6529-A, otherwise known as the Common Biometric Exchange Formats Framework (CBEFF) Patron Format A. Only **WINBIO\_TYPE\_FINGERPRINT** is currently supported.</span></span>



| <span data-ttu-id="74f6f-105">常數</span><span class="sxs-lookup"><span data-stu-id="74f6f-105">Constant</span></span>                                                                                                                                                                                                            | <span data-ttu-id="74f6f-106">描述</span><span class="sxs-lookup"><span data-stu-id="74f6f-106">Description</span></span>                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <span data-ttu-id="74f6f-107"><dt>**WINBIO \_ 標準 \_ 類型 \_ 遮罩**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-107"><dt>**WINBIO\_STANDARD\_TYPE\_MASK**</dt></span></span> </dl>                 | <span data-ttu-id="74f6f-108">指定一組支援的生物特徵辨識因素的位元遮罩。</span><span class="sxs-lookup"><span data-stu-id="74f6f-108">Bitmask that specifies the supported set of biometric factors.</span></span><br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <span data-ttu-id="74f6f-109"><dt>**WINBIO \_ 沒有 \_ 任何 \_ 可用的類型**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-109"><dt>**WINBIO\_NO\_TYPE\_AVAILABLE**</dt></span></span> </dl>                    | <span data-ttu-id="74f6f-110">沒有任何生物特徵辨識類型可供使用。</span><span class="sxs-lookup"><span data-stu-id="74f6f-110">No biometric type is available.</span></span><br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <span data-ttu-id="74f6f-111"><dt>**WINBIO \_ 類型 \_ 多個**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-111"><dt>**WINBIO\_TYPE\_MULTIPLE**</dt></span></span> </dl>                                 | <span data-ttu-id="74f6f-112">已指定多個類型。</span><span class="sxs-lookup"><span data-stu-id="74f6f-112">Multiple types are specified.</span></span><br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <span data-ttu-id="74f6f-113"><dt>**WINBIO \_ 型別臉部 \_ \_ 特徵**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-113"><dt>**WINBIO\_TYPE\_FACIAL\_FEATURES**</dt></span></span> </dl>           | <span data-ttu-id="74f6f-114">臉部特徵可用來決定個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-114">Facial features are used to determine the identity of an individual.</span></span><br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <span data-ttu-id="74f6f-115"><dt>**WINBIO \_ 類型 \_ VOICE**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-115"><dt>**WINBIO\_TYPE\_VOICE**</dt></span></span> </dl>                                          | <span data-ttu-id="74f6f-116">個人的語音中的頻率和音量模式可用來決定個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-116">Frequency and volume patterns in the voice of an individual are used to determine the identity of an individual.</span></span><br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <span data-ttu-id="74f6f-117"><dt>**WINBIO \_ 類型 \_ 指紋**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-117"><dt>**WINBIO\_TYPE\_FINGERPRINT**</dt></span></span> </dl>                        | <span data-ttu-id="74f6f-118">指紋模式可用來決定個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-118">Fingerprint patterns are used to determine the identity of an individual.</span></span><br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <span data-ttu-id="74f6f-119"><dt>**WINBIO \_ 類型 \_ 鳶尾花**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-119"><dt>**WINBIO\_TYPE\_IRIS**</dt></span></span> </dl>                                             | <span data-ttu-id="74f6f-120">鳶尾花模式可用來決定個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-120">Iris patterns are used to determine the identity of an individual.</span></span> <span data-ttu-id="74f6f-121">從 Windows 10 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="74f6f-121">This value is supported starting in Windows 10.</span></span><br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <span data-ttu-id="74f6f-122"><dt>**WINBIO \_ 類型 \_ RETINA**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-122"><dt>**WINBIO\_TYPE\_RETINA**</dt></span></span> </dl>                                       | <span data-ttu-id="74f6f-123">Retina 中的同樣地模式可用來決定個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-123">Vein patterns in the retina are used to determine the identity of an individual.</span></span><br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <span data-ttu-id="74f6f-124"><dt>**WINBIO \_ 型別 \_ 手 \_ 幾何**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-124"><dt>**WINBIO\_TYPE\_HAND\_GEOMETRY**</dt></span></span> </dl>                 | <span data-ttu-id="74f6f-125">個人的形狀是用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-125">The shape of a hand of an individual is used to determine the identity of an individual.</span></span><br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <span data-ttu-id="74f6f-126"><dt>**WINBIO \_ 類型 \_ 簽名 \_ 動態**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-126"><dt>**WINBIO\_TYPE\_SIGNATURE\_DYNAMICS**</dt></span></span> </dl>  | <span data-ttu-id="74f6f-127">個人在簽署其名稱時使用的強制模式，會用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-127">The patterns of force that the individual uses when they sign their name are used to determine the identity of an individual.</span></span><br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <span data-ttu-id="74f6f-128"><dt>**WINBIO \_ 類型 \_ 擊鍵 \_ 動態**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-128"><dt>**WINBIO\_TYPE\_KEYSTROKE\_DYNAMICS**</dt></span></span> </dl>  | <span data-ttu-id="74f6f-129">依個人輸入的速度和錯誤模式，會用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-129">The speed and error patterns in typing by an individual are used to determine the identity of an individual.</span></span><br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <span data-ttu-id="74f6f-130"><dt>**WINBIO \_ 類型 \_ LIP \_ 移動**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-130"><dt>**WINBIO\_TYPE\_LIP\_MOVEMENT**</dt></span></span> </dl>                    | <span data-ttu-id="74f6f-131">當使用者說話時，所發生之個人的 lip 變更會用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-131">The changes in the lips of an individual that occur when they speak are used to determine the identity of an individual.</span></span><br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <span data-ttu-id="74f6f-132"><dt>**WINBIO \_ 類型 \_ 熱 \_ 臉部 \_ 影像**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-132"><dt>**WINBIO\_TYPE\_THERMAL\_FACE\_IMAGE**</dt></span></span> </dl> | <span data-ttu-id="74f6f-133">使用個人的溫度模式來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-133">The temperature patterns in the face of an individual are used to determine the identity of an individual.</span></span><br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <span data-ttu-id="74f6f-134"><dt>**WINBIO \_ 型別 \_ 熱 \_ 手 \_ 影像**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-134"><dt>**WINBIO\_TYPE\_THERMAL\_HAND\_IMAGE**</dt></span></span> </dl> | <span data-ttu-id="74f6f-135">個人的溫度模式會用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-135">The temperature patterns in the hand of an individual are used to determine the identity of an individual.</span></span><br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <span data-ttu-id="74f6f-136"><dt>**WINBIO \_ 類型 \_ GAIT**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-136"><dt>**WINBIO\_TYPE\_GAIT**</dt></span></span> </dl>                                             | <span data-ttu-id="74f6f-137">當個別的逐步解說用來判斷個人的身分識別時，所發生的移動模式。</span><span class="sxs-lookup"><span data-stu-id="74f6f-137">The patterns of movement that occur when the individual walks are used to determine the identity of an individual.</span></span><br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <span data-ttu-id="74f6f-138"><dt>**WINBIO \_ 類型 \_ 氣味**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-138"><dt>**WINBIO\_TYPE\_SCENT**</dt></span></span> </dl>                                          | <span data-ttu-id="74f6f-139">個人的氣味是用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-139">The scent of an individual is used to determine the identity of an individual.</span></span><br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <span data-ttu-id="74f6f-140"><dt>**WINBIO \_ 型別 \_ DNA**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-140"><dt>**WINBIO\_TYPE\_DNA**</dt></span></span> </dl>                                                | <span data-ttu-id="74f6f-141">Deoxyribonucleic acid (DNA) 順序可用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-141">Deoxyribonucleic acid (DNA) sequences are used to determine the identity of an individual.</span></span><br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <span data-ttu-id="74f6f-142"><dt>**WINBIO \_ 型別 \_ EAR \_ 圖形**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-142"><dt>**WINBIO\_TYPE\_EAR\_SHAPE**</dt></span></span> </dl>                             | <span data-ttu-id="74f6f-143">個別的 ear 圖形用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-143">The shape of an ear of the individual is used to determine the identity of an individual.</span></span><br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <span data-ttu-id="74f6f-144"><dt>**WINBIO \_ 類型的 \_ 指標 \_ 幾何**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-144"><dt>**WINBIO\_TYPE\_FINGER\_GEOMETRY**</dt></span></span> </dl>           | <span data-ttu-id="74f6f-145">個人的手指形狀是用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-145">The shapes of the fingers of an individual are used to determine the identity of an individual.</span></span><br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <span data-ttu-id="74f6f-146"><dt>**WINBIO \_ 類型 \_ 掌 \_ 印**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-146"><dt>**WINBIO\_TYPE\_PALM\_PRINT**</dt></span></span> </dl>                          | <span data-ttu-id="74f6f-147">手掌的形狀是用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-147">The shape of the palm is used to determine the identity of an individual.</span></span><br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <span data-ttu-id="74f6f-148"><dt>**WINBIO \_ 類型 \_ 同樣地 \_ 模式**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-148"><dt>**WINBIO\_TYPE\_VEIN\_PATTERN**</dt></span></span> </dl>                    | <span data-ttu-id="74f6f-149">在 veins 的面板底下的模式會用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-149">Patterns in the veins underneath the skin of the hand of an individual are used to determine the identity of an individual.</span></span><br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <span data-ttu-id="74f6f-150"><dt>**WINBIO \_ 類型 \_ 腳 \_ 列印**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-150"><dt>**WINBIO\_TYPE\_FOOT\_PRINT**</dt></span></span> </dl>                          | <span data-ttu-id="74f6f-151">英尺的形狀是用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-151">The shape of the foot is used to determine the identity of an individual.</span></span><br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <span data-ttu-id="74f6f-152"><dt>**WINBIO \_ \_ 其他類型**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-152"><dt>**WINBIO\_TYPE\_OTHER**</dt></span></span> </dl>                                          | <span data-ttu-id="74f6f-153">目前的常數不會定義支援的生物特徵辨識資料。</span><span class="sxs-lookup"><span data-stu-id="74f6f-153">The supported biometric data is not defined by the current constants.</span></span><br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <span data-ttu-id="74f6f-154"><dt>**WINBIO \_ 類型 \_ 密碼**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-154"><dt>**WINBIO\_TYPE\_PASSWORD**</dt></span></span> </dl>                                 | <span data-ttu-id="74f6f-155">密碼資料會用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-155">Password data is used to determine the identity of an individual.</span></span><br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <span data-ttu-id="74f6f-156"><dt>**WINBIO \_ 類型 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-156"><dt>**WINBIO\_TYPE\_ANY**</dt></span></span> </dl>                                                | <span data-ttu-id="74f6f-157">任何資料類型都是用來判斷個人的身分識別。</span><span class="sxs-lookup"><span data-stu-id="74f6f-157">Any type of data is used to determine the identity of an individual.</span></span><br/>                                                          |



## <a name="requirements"></a><span data-ttu-id="74f6f-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="74f6f-158">Requirements</span></span>



| <span data-ttu-id="74f6f-159">需求</span><span class="sxs-lookup"><span data-stu-id="74f6f-159">Requirement</span></span> | <span data-ttu-id="74f6f-160">值</span><span class="sxs-lookup"><span data-stu-id="74f6f-160">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74f6f-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="74f6f-161">Minimum supported client</span></span><br/> | <span data-ttu-id="74f6f-162">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74f6f-162">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="74f6f-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="74f6f-163">Minimum supported server</span></span><br/> | <span data-ttu-id="74f6f-164">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="74f6f-164">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                  |
| <span data-ttu-id="74f6f-165">標頭</span><span class="sxs-lookup"><span data-stu-id="74f6f-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="74f6f-166"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="74f6f-166"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74f6f-167">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74f6f-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74f6f-168">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="74f6f-168">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





