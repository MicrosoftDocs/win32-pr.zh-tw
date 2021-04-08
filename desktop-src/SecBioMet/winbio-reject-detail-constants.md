---
title: 'WINBIO_REJECT_DETAIL 常數 (Winbio \_ 類型 .h) '
description: 指定生物特徵辨識指紋捕捉或辨識程式未成功的原因。
ms.assetid: b1ae4e65-9e53-42dd-99ba-1910b72688dd
topic_type:
- apiref
api_name:
- WINBIO_FP_TOO_HIGH
- WINBIO_FP_TOO_LOW
- WINBIO_FP_TOO_LEFT
- WINBIO_FP_TOO_RIGHT
- WINBIO_FP_TOO_FAST
- WINBIO_FP_TOO_SLOW
- WINBIO_FP_POOR_QUALITY
- WINBIO_FP_TOO_SKEWED
- WINBIO_FP_TOO_SHORT
- WINBIO_FP_MERGE_FAILURE
- WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK
- WINBIO_REJECT_DETAIL_POSITION_MASK
- WINBIO_REJECT_DETAIL_REASON_MASK
- WINBIO_IRIS_POOR_QUALITY
- WINBIO_IRIS_TOO_BRIGHT
- WINBIO_IRIS_TOO_DARK
- WINBIO_IRIS_SPOOF_DETECTED
- WINBIO_IRIS_TOO_SKEWED
- WINBIO_IRIS_TOO_CLOSED
- WINBIO_IRIS_GLARE
- WINBIO_IRIS_DIRTY_LENS
- WINBIO_IRIS_POOR_FOCUS
- WINBIO_IRIS_WRONG_ORIENTATION
- WINBIO_IRIS_TOO_HIGH
- WINBIO_IRIS_TOO_LOW
- WINBIO_IRIS_TOO_LEFT
- WINBIO_IRIS_TOO_RIGHT
- WINBIO_IRIS_TOO_NEAR
- WINBIO_IRIS_TOO_FAR
- WINBIO_FACE_POOR_QUALITY
- WINBIO_FACE_TOO_BRIGHT
- WINBIO_FACE_TOO_DARK
- WINBIO_FACE_SPOOF_DETECTED
- WINBIO_FACE_AMBIGUOUS_TARGET
- WINBIO_FACE_EYES_OCCLUDED
- WINBIO_FACE_WRONG_ORIENTATION
- WINBIO_FACE_TOO_HIGH
- WINBIO_FACE_TOO_LOW
- WINBIO_FACE_TOO_LEFT
- WINBIO_FACE_TOO_RIGHT
- WINBIO_FACE_TOO_NEAR
- WINBIO_FACE_TOO_FAR
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d23dcf568e5ed25fb5081283a421b1c0dbb07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686608"
---
# <a name="winbio_reject_detail-constants"></a>WINBIO \_ 拒絕 \_ 詳細資料常數

您可以使用下列常數來指定生物特徵辨識指紋捕捉或辨識程式未成功的原因。



| 常數                                                                                                                                                                                                                                        | 描述                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_FP_TOO_HIGH"></span><span id="winbio_fp_too_high"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 高**</dt> </dl>                                                                  | 手指掃描在手指上開始過高。<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_LOW"></span><span id="winbio_fp_too_low"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 低**</dt> </dl>                                                                     | 手指掃描開始太低。<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_LEFT"></span><span id="winbio_fp_too_left"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 左邊**</dt> </dl>                                                                  | 在掃描期間，手指太久。<br/>                                                                                                                                                                                                                                           |
| <span id="WINBIO_FP_TOO_RIGHT"></span><span id="winbio_fp_too_right"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 右邊**</dt> </dl>                                                               | 在掃描期間，手指太遠。<br/>                                                                                                                                                                                                                                          |
| <span id="WINBIO_FP_TOO_FAST"></span><span id="winbio_fp_too_fast"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 快**</dt> </dl>                                                                  | 感應器上的手指撥動太快。<br/>                                                                                                                                                                                                                                       |
| <span id="WINBIO_FP_TOO_SLOW"></span><span id="winbio_fp_too_slow"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 慢**</dt> </dl>                                                                  | 感應器上的手指撥動太慢。<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_FP_POOR_QUALITY"></span><span id="winbio_fp_poor_quality"></span><dl> <dt>**WINBIO \_ FP \_ 品質不佳 \_**</dt> </dl>                                                      | 掃描品質太差。<br/>                                                                                                                                                                                                                                                         |
| <span id="WINBIO_FP_TOO_SKEWED"></span><span id="winbio_fp_too_skewed"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 扭曲**</dt> </dl>                                                            | 手指未直接通過感應器。<br/>                                                                                                                                                                                                                                    |
| <span id="WINBIO_FP_TOO_SHORT"></span><span id="winbio_fp_too_short"></span><dl> <dt>**WINBIO \_ FP \_ 太 \_ 短**</dt> </dl>                                                               | 未掃描過足夠的手指。<br/>                                                                                                                                                                                                                                                  |
| <span id="WINBIO_FP_MERGE_FAILURE"></span><span id="winbio_fp_merge_failure"></span><dl> <dt>**WINBIO \_ FP \_ 合併 \_ 失敗**</dt> </dl>                                                   | 指紋捕捉無法合併。<br/>                                                                                                                                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_ANTI_SPOOF_MASK____"></span><span id="winbio_reject_detail_anti_spoof_mask____"></span><dl> <dt>**WINBIO \_拒絕 \_ 詳細資料 \_ 反詐騙 \_ \_ 遮罩**</dt> </dl> | 此遮罩涵蓋「拒絕詳細資料」值的最高8個位，其中會指出活動證明的行為。 從 Windows 10 開始支援此值。<br/>                                                                                                                        |
| <span id="WINBIO_REJECT_DETAIL_POSITION_MASK______"></span><span id="winbio_reject_detail_position_mask______"></span><dl> <dt>**WINBIO \_拒絕 \_ 詳細資料 \_ 位置 \_ 遮罩**</dt> </dl>    | 此遮罩涵蓋專門用來放置錯誤的位數範圍。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                                         |
| <span id="WINBIO_REJECT_DETAIL_REASON_MASK"></span><span id="winbio_reject_detail_reason_mask"></span><dl> <dt>**WINBIO \_ 拒絕 \_ 詳細資料 \_ 原因 \_ 遮罩**</dt> </dl>                       | 此遮罩涵蓋拒絕的列舉原因所在的較低16位。 從 Windows 10 開始支援此值。<br/>                                                                                                                                           |
| <span id="WINBIO_IRIS_POOR_QUALITY"></span><span id="winbio_iris_poor_quality"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ \_ 品質不良**</dt> </dl>                                                | 這種情況會導致相機捕獲不良的影像。 指示使用者清除感應器，並再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                        |
| <span id="WINBIO_IRIS_TOO_BRIGHT"></span><span id="winbio_iris_too_bright"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 鮮**</dt> </dl>                                                      | 影像包含太多的環境光線以取得良好的相符項。 指示使用者確定它們不是另一個亮亮的來源。 從 Windows 10 開始支援此值。<br/>                                                                                        |
| <span id="WINBIO_IRIS_TOO_DARK"></span><span id="winbio_iris_too_dark"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 深**</dt> </dl>                                                            | 影像太深，無法取得良好的相符。 指示使用者確定其鳶尾花不會被新娘、深眼鏡或彩色連絡人等專案遮蓋。 從 Windows 10 開始支援此值。<br/>                                                                     |
| <span id="WINBIO_IRIS_SPOOF_DETECTED"></span><span id="winbio_iris_spoof_detected"></span><dl> <dt>**偵測 \_ 到 WINBIO 鳶尾花 \_ 欺騙 \_**</dt> </dl>                                          | 辨識元件認為鳶尾花不是即時的，而是來自重新執行的影片摘要、相片或立體 sculpture。 從 Windows 10 開始支援此值。<br/>                                                                                                   |
| <span id="WINBIO_IRIS_TOO_SKEWED"></span><span id="winbio_iris_too_skewed"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 扭曲**</dt> </dl>                                                      | 使用者不會直接在相機中尋找。 指示使用者直接查看相機，然後再掃描一次。 從 Windows 10 開始支援此值。<br/>                                                                                                                       |
| <span id="WINBIO_IRIS_TOO_CLOSED"></span><span id="winbio_iris_too_closed"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 關閉**</dt> </dl>                                                      | 使用者的 eyelids 會遮蔽鳶尾花。 指示使用者開啟其眼睛，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                          |
| <span id="WINBIO_IRIS_GLARE"></span><span id="winbio_iris_glare"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 防眩**</dt> </dl>                                                                      | 影像包含鏡頭防眩。 指示使用者移除其眼鏡，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                               |
| <span id="WINBIO_IRIS_DIRTY_LENS"></span><span id="winbio_iris_dirty_lens"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 中途 \_ 鏡頭**</dt> </dl>                                                      | 相機鏡頭已中途變更。 指示使用者清除鏡頭，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                         |
| <span id="WINBIO_IRIS_POOR_FOCUS"></span><span id="winbio_iris_poor_focus"></span><dl> <dt>**WINBIO \_ 鳶尾花不 \_ 佳 \_ 焦點**</dt> </dl>                                                      | 這個鳶尾花不是焦點。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                                                                             |
| <span id="WINBIO_IRIS_WRONG_ORIENTATION"></span><span id="winbio_iris_wrong_orientation"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 錯誤 \_ 方向**</dt> </dl>                                 | 相機方向與 [**WINBIO \_ 擴充 \_ 感應器 \_ 資訊**](winbio-extended-sensor-info.md) 結構指定的強制方向不相符。 指示使用者變更相機方向，並再次掃描。 從 Windows 10 開始支援此值。<br/> |
| <span id="WINBIO_IRIS_TOO_HIGH"></span><span id="winbio_iris_too_high"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 高**</dt> </dl>                                                            | 鳶尾花正在面對。 指示使用者稍微向下查詢，然後再掃描一次。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LOW"></span><span id="winbio_iris_too_low"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 低**</dt> </dl>                                                               | 鳶尾花朝下。 指示使用者查詢一點，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                     |
| <span id="WINBIO_IRIS_TOO_LEFT"></span><span id="winbio_iris_too_left"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 左邊**</dt> </dl>                                                            | 鳶尾花距離左方太遠。 指示使用者在右側尋找更多的許可權，然後再掃描一次。 從 Windows 10 開始支援此值。<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_RIGHT"></span><span id="winbio_iris_too_right"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 右邊**</dt> </dl>                                                         | 鳶尾花太遠到右邊。 指示使用者稍微向左看看，然後再掃描一次。 從 Windows 10 開始支援此值。<br/>                                                                                                                                  |
| <span id="WINBIO_IRIS_TOO_NEAR"></span><span id="winbio_iris_too_near"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 近**</dt> </dl>                                                            | 鳶尾花太接近相機。 指示使用者移動一些更遠的部分，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                   |
| <span id="WINBIO_IRIS_TOO_FAR"></span><span id="winbio_iris_too_far"></span><dl> <dt>**WINBIO \_ 鳶尾花 \_ 太 \_ 遠**</dt> </dl>                                                               | 鳶尾花距離相機太遠。 指示使用者移動一些較接近的部分，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                         |
| <span id="WINBIO_FACE_POOR_QUALITY"></span><span id="winbio_face_poor_quality"></span><dl> <dt>**WINBIO \_ 臉部 \_ \_ 品質不良**</dt> </dl>                                                | 這種情況會導致相機捕獲不良的影像。 指示使用者清除感應器，並再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                        |
| <span id="WINBIO_FACE_TOO_BRIGHT"></span><span id="winbio_face_too_bright"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 鮮**</dt> </dl>                                                      | 影像包含太多的環境光線以取得良好的相符項。 指示使用者確定它們不是另一個亮亮的來源。 從 Windows 10 開始支援此值。<br/>                                                                                        |
| <span id="WINBIO_FACE_TOO_DARK"></span><span id="winbio_face_too_dark"></span><dl> <dt>**WINBIO \_ 面 \_ 太 \_ 深**</dt> </dl>                                                            | 影像太深，無法取得良好的相符。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                                                             |
| <span id="WINBIO_FACE_SPOOF_DETECTED"></span><span id="winbio_face_spoof_detected"></span><dl> <dt>**偵測 \_ 到 WINBIO 臉部詐騙 \_ \_**</dt> </dl>                                          | 辨識元件認為臉部未上線，但來自重新播放的影片摘要、相片或立體 sculpture。 從 Windows 10 開始支援此值。<br/>                                                                                                   |
| <span id="WINBIO_FACE_AMBIGUOUS_TARGET"></span><span id="winbio_face_ambiguous_target"></span><dl> <dt>**WINBIO \_ 臉部不 \_ 明確的 \_ 目標**</dt> </dl>                                    | 攝影機框架中有兩個以上的臉部重迭。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                                                     |
| <span id="WINBIO_FACE_EYES_OCCLUDED"></span><span id="winbio_face_eyes_occluded"></span><dl> <dt>**WINBIO \_ 臉部 \_ 眼睛 \_ PIXELS OCCLUDED**</dt> </dl>                                             | 使用者的眼睛是 pixels occluded。 指示使用者確保其眼睛不會被專案（例如新娘、深眼鏡或彩色連絡人）遮蔽。 從 Windows 10 開始支援此值。<br/>                                                                                 |
| <span id="WINBIO_FACE_WRONG_ORIENTATION"></span><span id="winbio_face_wrong_orientation"></span><dl> <dt>**WINBIO \_ 面對 \_ 錯誤的 \_ 方向**</dt> </dl>                                 | 相機方向與 [**WINBIO \_ 擴充 \_ 感應器 \_ 資訊**](winbio-extended-sensor-info.md) 結構指定的強制方向不相符。 指示使用者變更相機方向，並再次掃描。 從 Windows 10 開始支援此值。<br/> |
| <span id="WINBIO_FACE_TOO_HIGH"></span><span id="winbio_face_too_high"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 高**</dt> </dl>                                                            | 臉部朝上。 指示使用者稍微向下查詢，然後再掃描一次。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LOW"></span><span id="winbio_face_too_low"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 低**</dt> </dl>                                                               | 臉部朝下。 指示使用者查詢一點，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                                     |
| <span id="WINBIO_FACE_TOO_LEFT"></span><span id="winbio_face_too_left"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 左方**</dt> </dl>                                                            | 臉部太遠左右。 指示使用者向右移動一點，然後再掃描一次。 從 Windows 10 開始支援此值。<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_RIGHT"></span><span id="winbio_face_too_right"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 右邊**</dt> </dl>                                                         | 臉部太遠不到右邊。 指示使用者向左移動一點，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                  |
| <span id="WINBIO_FACE_TOO_NEAR"></span><span id="winbio_face_too_near"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 近**</dt> </dl>                                                            | 臉部太接近相機。 指示使用者移動一些更遠的部分，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                   |
| <span id="WINBIO_FACE_TOO_FAR"></span><span id="winbio_face_too_far"></span><dl> <dt>**WINBIO \_ 臉部 \_ 太 \_ 遠**</dt> </dl>                                                               | 臉部離相機太遠。 指示使用者移動一些較接近的部分，然後再次掃描。 從 Windows 10 開始支援此值。<br/>                                                                                                                                         |



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

 

 





