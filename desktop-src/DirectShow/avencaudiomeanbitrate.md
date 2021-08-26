---
description: 指定編碼音訊串流的平均位元速率，以每秒位數為單位。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。
ms.assetid: 9513ad64-2de9-497d-86ce-46cfdf87e0f8
title: 'AVEncAudioMeanBitRate 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7b0d1ad6cfde3aee4ec9c747feb8d692c3917332808e40e3d5f76e3d01ce21
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079468"
---
# <a name="avencaudiomeanbitrate-property"></a>AVEncAudioMeanBitRate 屬性

指定編碼音訊串流的平均位元速率，以每秒位數為單位。 這個屬性只適用于常數的位元速率 (CBR) 和變數位元速率 (VBR) 編碼模式。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonMeanBitRate**

## <a name="property-value"></a>屬性值

編碼器可以將此屬性實作為列舉集或線性範圍。

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

 

 




