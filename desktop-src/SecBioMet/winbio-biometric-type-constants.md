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
# <a name="winbio_biometric_type-constants"></a>WINBIO \_ 生物特徵辨識 \_ 類型常數

下列常數代表國家/地區協會標準和技術資訊所定義的標準生物特徵辨識類型 (NISTIR) 6529-A，亦稱為一般生物特徵辨識交換格式架構 (CBEFF) Patron 格式 A。目前只支援 **WINBIO \_ 類型 \_ 指紋** 。



| 常數                                                                                                                                                                                                            | 描述                                                                                                                              |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_STANDARD_TYPE_MASK"></span><span id="winbio_standard_type_mask"></span><dl> <dt>**WINBIO \_ 標準 \_ 類型 \_ 遮罩**</dt> </dl>                 | 指定一組支援的生物特徵辨識因素的位元遮罩。<br/>                                                                |
| <span id="WINBIO_NO_TYPE_AVAILABLE"></span><span id="winbio_no_type_available"></span><dl> <dt>**WINBIO \_ 沒有 \_ 任何 \_ 可用的類型**</dt> </dl>                    | 沒有任何生物特徵辨識類型可供使用。<br/>                                                                                               |
| <span id="WINBIO_TYPE_MULTIPLE"></span><span id="winbio_type_multiple"></span><dl> <dt>**WINBIO \_ 類型 \_ 多個**</dt> </dl>                                 | 已指定多個類型。<br/>                                                                                                 |
| <span id="WINBIO_TYPE_FACIAL_FEATURES"></span><span id="winbio_type_facial_features"></span><dl> <dt>**WINBIO \_ 型別臉部 \_ \_ 特徵**</dt> </dl>           | 臉部特徵可用來決定個人的身分識別。<br/>                                                          |
| <span id="WINBIO_TYPE_VOICE"></span><span id="winbio_type_voice"></span><dl> <dt>**WINBIO \_ 類型 \_ VOICE**</dt> </dl>                                          | 個人的語音中的頻率和音量模式可用來決定個人的身分識別。<br/>              |
| <span id="WINBIO_TYPE_FINGERPRINT"></span><span id="winbio_type_fingerprint"></span><dl> <dt>**WINBIO \_ 類型 \_ 指紋**</dt> </dl>                        | 指紋模式可用來決定個人的身分識別。<br/>                                                     |
| <span id="WINBIO_TYPE_IRIS"></span><span id="winbio_type_iris"></span><dl> <dt>**WINBIO \_ 類型 \_ 鳶尾花**</dt> </dl>                                             | 鳶尾花模式可用來決定個人的身分識別。 從 Windows 10 開始支援此值。<br/>            |
| <span id="WINBIO_TYPE_RETINA"></span><span id="winbio_type_retina"></span><dl> <dt>**WINBIO \_ 類型 \_ RETINA**</dt> </dl>                                       | Retina 中的同樣地模式可用來決定個人的身分識別。<br/>                                              |
| <span id="WINBIO_TYPE_HAND_GEOMETRY"></span><span id="winbio_type_hand_geometry"></span><dl> <dt>**WINBIO \_ 型別 \_ 手 \_ 幾何**</dt> </dl>                 | 個人的形狀是用來判斷個人的身分識別。<br/>                                      |
| <span id="WINBIO_TYPE_SIGNATURE_DYNAMICS"></span><span id="winbio_type_signature_dynamics"></span><dl> <dt>**WINBIO \_ 類型 \_ 簽名 \_ 動態**</dt> </dl>  | 個人在簽署其名稱時使用的強制模式，會用來判斷個人的身分識別。<br/> |
| <span id="WINBIO_TYPE_KEYSTROKE_DYNAMICS"></span><span id="winbio_type_keystroke_dynamics"></span><dl> <dt>**WINBIO \_ 類型 \_ 擊鍵 \_ 動態**</dt> </dl>  | 依個人輸入的速度和錯誤模式，會用來判斷個人的身分識別。<br/>                  |
| <span id="WINBIO_TYPE_LIP_MOVEMENT"></span><span id="winbio_type_lip_movement"></span><dl> <dt>**WINBIO \_ 類型 \_ LIP \_ 移動**</dt> </dl>                    | 當使用者說話時，所發生之個人的 lip 變更會用來判斷個人的身分識別。<br/>      |
| <span id="WINBIO_TYPE_THERMAL_FACE_IMAGE"></span><span id="winbio_type_thermal_face_image"></span><dl> <dt>**WINBIO \_ 類型 \_ 熱 \_ 臉部 \_ 影像**</dt> </dl> | 使用個人的溫度模式來判斷個人的身分識別。<br/>                    |
| <span id="WINBIO_TYPE_THERMAL_HAND_IMAGE"></span><span id="winbio_type_thermal_hand_image"></span><dl> <dt>**WINBIO \_ 型別 \_ 熱 \_ 手 \_ 影像**</dt> </dl> | 個人的溫度模式會用來判斷個人的身分識別。<br/>                    |
| <span id="WINBIO_TYPE_GAIT"></span><span id="winbio_type_gait"></span><dl> <dt>**WINBIO \_ 類型 \_ GAIT**</dt> </dl>                                             | 當個別的逐步解說用來判斷個人的身分識別時，所發生的移動模式。<br/>            |
| <span id="WINBIO_TYPE_SCENT"></span><span id="winbio_type_scent"></span><dl> <dt>**WINBIO \_ 類型 \_ 氣味**</dt> </dl>                                          | 個人的氣味是用來判斷個人的身分識別。<br/>                                                |
| <span id="WINBIO_TYPE_DNA"></span><span id="winbio_type_dna"></span><dl> <dt>**WINBIO \_ 型別 \_ DNA**</dt> </dl>                                                | Deoxyribonucleic acid (DNA) 順序可用來判斷個人的身分識別。<br/>                                    |
| <span id="WINBIO_TYPE_EAR_SHAPE"></span><span id="winbio_type_ear_shape"></span><dl> <dt>**WINBIO \_ 型別 \_ EAR \_ 圖形**</dt> </dl>                             | 個別的 ear 圖形用來判斷個人的身分識別。<br/>                                     |
| <span id="WINBIO_TYPE_FINGER_GEOMETRY"></span><span id="winbio_type_finger_geometry"></span><dl> <dt>**WINBIO \_ 類型的 \_ 指標 \_ 幾何**</dt> </dl>           | 個人的手指形狀是用來判斷個人的身分識別。<br/>                               |
| <span id="WINBIO_TYPE_PALM_PRINT"></span><span id="winbio_type_palm_print"></span><dl> <dt>**WINBIO \_ 類型 \_ 掌 \_ 印**</dt> </dl>                          | 手掌的形狀是用來判斷個人的身分識別。<br/>                                                     |
| <span id="WINBIO_TYPE_VEIN_PATTERN"></span><span id="winbio_type_vein_pattern"></span><dl> <dt>**WINBIO \_ 類型 \_ 同樣地 \_ 模式**</dt> </dl>                    | 在 veins 的面板底下的模式會用來判斷個人的身分識別。<br/>   |
| <span id="WINBIO_TYPE_FOOT_PRINT"></span><span id="winbio_type_foot_print"></span><dl> <dt>**WINBIO \_ 類型 \_ 腳 \_ 列印**</dt> </dl>                          | 英尺的形狀是用來判斷個人的身分識別。<br/>                                                     |
| <span id="WINBIO_TYPE_OTHER"></span><span id="winbio_type_other"></span><dl> <dt>**WINBIO \_ \_ 其他類型**</dt> </dl>                                          | 目前的常數不會定義支援的生物特徵辨識資料。<br/>                                                         |
| <span id="WINBIO_TYPE_PASSWORD"></span><span id="winbio_type_password"></span><dl> <dt>**WINBIO \_ 類型 \_ 密碼**</dt> </dl>                                 | 密碼資料會用來判斷個人的身分識別。<br/>                                                             |
| <span id="WINBIO_TYPE_ANY"></span><span id="winbio_type_any"></span><dl> <dt>**WINBIO \_ 類型 \_**</dt> </dl>                                                | 任何資料類型都是用來判斷個人的身分識別。<br/>                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                                                                               |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                                                                                  |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





