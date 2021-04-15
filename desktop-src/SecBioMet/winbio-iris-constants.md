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
# <a name="winbio_iris-constants"></a>WINBIO \_ 鳶尾花常數

下列常數是 **WINBIO \_ 生物特徵 \_ 子類型** 值，可用來指定超過 ANSI INCITS 379-2004 的鳶尾花辨識類型：「鳶尾花影像交換格式」，這不會定義任何左/右眼睛值：



| 常數/值                                                                                                                                                                                                                                                                   | Description                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_IRIS_TYPE_UNKNOWN_"></span><span id="winbio_iris_type_unknown_"></span><dl> <dt> **WINBIO \_ 鳶尾花 \_ 類型 \_ 未知**</dt> <dt>0</dt> </dl>                       | 鳶尾花類型未知。 <br/>                                                                                                                                 |
| <span id="WINBIO_IRIS_LEFT_EYE_"></span><span id="winbio_iris_left_eye_"></span><dl> <dt> **WINBIO \_ 鳶尾花 \_ 左方 \_ 眼睛**</dt> <dt>0xF5</dt> </dl>                               | 鳶尾花類型是最左邊的眼睛。 <br/>                                                                                                                            |
| <span id="WINBIO_IRIS_RIGHT_EYE_"></span><span id="winbio_iris_right_eye_"></span><dl> <dt> **WINBIO \_ 鳶尾花 \_ RIGHT \_ 眼睛**</dt> <dt>0xF6</dt> </dl>                            | 鳶尾花型別是正確的眼睛。 <br/>                                                                                                                           |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_01"></span><span id="winbio_iris_unspecified_pos_01"></span><dl> <dt>**WINBIO \_鳶尾花 \_ 未指定的 \_ POS \_ 01**</dt> <dt>0xF7</dt> </dl>    | 當只有一眼時，與使用者第一個範本相關聯的子類型是相機框架，無法判斷是否為使用者的左邊或右邊。<br/>  |
| <span id="WINBIO_IRIS_UNSPECIFIED_POS_02_"></span><span id="winbio_iris_unspecified_pos_02_"></span><dl> <dt> **WINBIO \_ 鳶尾花 \_ 未指定的 \_ POS \_ 02**</dt> <dt>0xF8</dt> </dl> | 當只有一眼時，與使用者第二個範本相關聯的子類型是相機框架，無法判斷是否為使用者的左邊或右邊。<br/> |
| <span id="WINBIO_IRIS_BOTH_EYES_"></span><span id="winbio_iris_both_eyes_"></span><dl> <dt> **WINBIO \_ 鳶尾花 \_ 兩種 \_ 眼睛**</dt> <dt>0xF9</dt> </dl>                             | 鳶尾花類型都是眼睛。 <br/>                                                                                                                               |
| <span id="WINBIO_IRIS_EITHER_EYE_"></span><span id="winbio_iris_either_eye_"></span><dl> <dt> **WINBIO \_ 鳶尾花 \_ \_**</dt> <dt>0xFA</dt> </dl>                          | 鳶尾花類型可以是眼睛。 <br/>                                                                                                                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



 

 





