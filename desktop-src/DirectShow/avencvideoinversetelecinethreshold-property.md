---
description: 設定編碼器將「影片」欄位視為多餘的閾值。
ms.assetid: db6c2f0e-f451-4d2d-984f-b507083e8358
title: 'AVEncVideoInverseTelecineThreshold 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3427a8ff1491277c2e36640560acf728c0ef7208
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687507"
---
# <a name="avencvideoinversetelecinethreshold-property"></a>AVEncVideoInverseTelecineThreshold 屬性

設定編碼器將「影片」欄位視為多餘的閾值。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoInverseTelecineThreshold**

## <a name="property-value"></a>屬性值

這個屬性的值具有下列範圍。



| 值 | 描述                                                    |
|-------|----------------------------------------------------------------|
| 0     | 編碼器較不可能將影片欄位視為多餘。 |
| 100   | 編碼器更可能將影片欄位視為多餘的。 |



 

## <a name="remarks"></a>備註

如果編碼器正在使用類比影片來源執行反向電視電影，請設定此屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 專業版傳統型 \[ 應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop 應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




