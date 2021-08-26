---
description: 傳回音頻內容中出現的最高音量層級。
ms.assetid: 1d9a6a22-bb82-45e1-80d2-88627c90340c
title: 'AVEncStatAudioPeakPCMValue 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 330f3eea62ce5f0232504786c63e87c233bd802f6d06fad6306f476f9d6b5361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999838"
---
# <a name="avencstataudiopeakpcmvalue-property"></a>AVEncStatAudioPeakPCMValue 屬性

傳回音頻內容中出現的最高音量層級。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncStatAudioPeakPCMValue**

## <a name="remarks"></a>備註

編碼完成之後，就可以使用這個屬性。

這個屬性只適用于以品質為基礎的變數位元速率 (VBR) 編碼

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

 

 




