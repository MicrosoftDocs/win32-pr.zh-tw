---
description: 啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的音量均衡。
ms.assetid: f02b187f-1bcb-47b3-8ac2-018ed30491c6
title: 'AVDSPLoudnessEqualization 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61696b51996d6fe57cf15372d511704e2dad482f0a5e99eb165795f56256656a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052828"
---
# <a name="avdsploudnessequalization-property"></a>AVDSPLoudnessEqualization 屬性

啟用或停用音訊解碼器或數位訊號處理器 (DSP) 的音量均衡。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDSPLoudnessEqualization**

## <a name="property-value"></a>屬性值

這個屬性的值是 [**eAVDSPLoudnessEqualization**](/windows/desktop/api/codecapi/ne-codecapi-eavdsploudnessequalization) 列舉的成員。

## <a name="remarks"></a>備註

音量均衡是一種 DSP 程式，可在音訊串流變更時維持一致的磁片區層級。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




