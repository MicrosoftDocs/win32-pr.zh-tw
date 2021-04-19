---
description: 空間 \_ 音訊 \_ XXX 常數會定義與空間音效功能相關的值。
ms.assetid: F1A01BDB-0CC2-45ED-A423-8CC7F54D4E55
title: 'SPATIAL_AUDIO_XXX 常數 (SpatialAudioMetadata) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd2c92b970f69cf84e0744f21a41932a8851efed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001143"
---
# <a name="spatial_audio_xxx-constants"></a>空間 \_ 音訊 \_ XXX 常數

空間 \_ 音訊 \_ XXX 常數會定義與空間音效功能相關的值。



| 常數/值                                                                                                                                                                                                                                                                                       | Description                                                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPATIAL_AUDIO_POSITION"></span><span id="spatial_audio_position"></span><dl> <dt>**空間 \_音訊 \_ 位置**</dt> <dt>200</dt> </dl>                                                   | 標準的 Microsoft 定義空間音訊中繼資料命令，代表 [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) 所使用之標準模型中的接聽程式位置，其中接聽程式的標頭是座標處的位置， (0、0、0) （定義于計量區）。<br/> |
| <span id="SPATIAL_AUDIO_POSITION_BYTE_COUNT"></span><span id="spatial_audio_position_byte_count"></span><dl> <dt>**空間 \_音訊 \_ 位置 \_ 位元組 \_ 計數**</dt> <dt>sizeof (float) \* 3</dt> </dl> | 指定 **空間 \_ 音訊 \_ 位置** 值的大小。<br/>                                                                                                                                                                                                        |
| <span id="SPATIAL_AUDIO_STANDARD_COMMANDS_START"></span><span id="spatial_audio_standard_commands_start"></span><dl> <dt>**空間 \_音訊 \_ 標準 \_ 命令 \_ 開始**</dt> <dt>200</dt> </dl>    | 指定 Microsoft 保留空間音訊中繼資料命令範圍的開始。 自訂中繼資料命令僅限於命令識別碼 0-199。 命令 200-255 已保留供 Microsoft 使用。<br/>                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>SpatialAudioMetadata。h</dt> </dl> |



 

 




