---
description: 指定編碼期間要跳過的欄位數目。
ms.assetid: 82f2a2c1-52ff-410d-b5da-b2419c0adfe3
title: 'AVEncVideoNoOfFieldsToSkip 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 708ef409fb907520d6a582599da2050a1353636c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846131"
---
# <a name="avencvideonooffieldstoskip-property"></a>AVEncVideoNoOfFieldsToSkip 屬性

指定編碼期間要跳過的欄位數目。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT64** (**VT \_ UI8**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoNoOfFieldsToSkip**

## <a name="remarks"></a>備註

若為漸進式影片，請將此屬性設定為要略過的畫面格數目的兩倍。

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

 

 




