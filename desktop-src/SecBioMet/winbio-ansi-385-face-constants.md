---
title: 'WINBIO_ANSI_385_FACE 常數 (Winbio \_ 類型 .h) '
description: 指定臉部辨識的正面臉部影像類型。
ms.assetid: 16D21E40-C158-4674-80D0-AE9494124B96
topic_type:
- apiref
api_name:
- WINBIO_ANSI_385_FACE_TYPE_UNKNOWN
- WINBIO_ANSI_385_FACE_FRONTAL_FULL
- WINBIO_ANSI_385_FACE_FRONTAL_TOKEN
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afa6bc6ba28de799795a049dde3ab98ebdb4c78
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105413"
---
# <a name="winbio_ansi_385_face-constants"></a>WINBIO \_ ANSI \_ 385 \_ 臉部常數

下列常數是 **WINBIO \_ 生物特徵 \_ 子** 型別值，可用來指定 ANSI INCITS 385-2004 所定義的兩種正面臉部影像：「資料交換的臉部辨識格式」：完整解析度和低解析度。 在實務上，生物特徵辨識架構只會使用完整的解析度影像進行臉部辨識。



| 常數/值                                                                                                                                                                                                                                                                          | Description                                                |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------|
| <span id="WINBIO_ANSI_385_FACE_TYPE_UNKNOWN"></span><span id="winbio_ansi_385_face_type_unknown"></span><dl> <dt>**WINBIO \_ANSI \_ 385 \_ 臉部 \_ 類型 \_ 未知**</dt> <dt>0</dt> </dl>    | 正面臉部影像類型未知。<br/>         |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_FULL"></span><span id="winbio_ansi_385_face_frontal_full"></span><dl> <dt>**WINBIO \_ANSI \_ 385 \_ 臉部 \_ 正面 \_ FULL**</dt> <dt>1</dt> </dl>    | 正面臉部影像類型為完整解析度。<br/> |
| <span id="WINBIO_ANSI_385_FACE_FRONTAL_TOKEN"></span><span id="winbio_ansi_385_face_frontal_token"></span><dl> <dt>**WINBIO \_ANSI \_ 385 \_ 臉部 \_ 正面 \_ 權杖**</dt> <dt>2</dt> </dl> | 正面臉部影像類型為低解析度。<br/>  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



 

 





