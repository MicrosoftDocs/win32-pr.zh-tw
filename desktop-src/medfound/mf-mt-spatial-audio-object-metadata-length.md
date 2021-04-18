---
description: 值，指定解碼器將輸出的空間音訊中繼資料物件類型大小（以位元組為單位）。
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: 'MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193015"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>MF \_ MT \_ 空間 \_ 音訊 \_ 物件 \_ 中繼資料 \_ 長度屬性

值，指定解碼器將輸出的空間音訊中繼資料物件類型大小（以位元組為單位）。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

使用 [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) 介面寫入具有指定格式的中繼資料 blob，並使用 [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) 介面進行讀取。 中繼資料 blob 對媒體基礎管線和元件而言是不透明的。 屬性會套用至空間音訊媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 
