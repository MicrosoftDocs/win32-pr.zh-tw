---
description: 傳回編碼音訊的每秒平均位數。
ms.assetid: c90c9247-825f-4602-bb16-809969703a98
title: 'AVEncStatAudioAverageBPS 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b43bf329d1d55b41c7849fee7855d322f3ab1622bca013ca5e96cfa4f519db
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999858"
---
# <a name="avencstataudioaveragebps-property"></a>AVEncStatAudioAverageBPS 屬性

傳回編碼音訊的每秒平均位數。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncStatAudioAverageBPS**

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

 

 




