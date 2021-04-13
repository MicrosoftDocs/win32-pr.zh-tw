---
description: 用來識別空間音訊元資料格式的解碼器定義 GUID，會通知中繼資料物件類型的下游元件，該型別會輸出該解碼器。
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: 'MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193016"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>MF \_ MT \_ 空間 \_ 音訊 \_ 物件 \_ 中繼資料 \_ 格式 \_ 識別碼屬性

用來識別空間音訊元資料格式的解碼器定義 GUID，會通知中繼資料物件類型的下游元件，該型別會輸出該解碼器。

## <a name="data-type"></a>資料類型

**GUID**

## <a name="remarks"></a>備註

使用 [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) 介面寫入具有指定格式的中繼資料 blob，並使用 [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) 介面進行讀取。 中繼資料 blob 對媒體基礎管線和元件而言是不透明的。 屬性會套用至空間音訊媒體類型。 如果下游元件不支援 GUID 指定的元資料格式，則元件應該拒絕輸入媒體類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 
