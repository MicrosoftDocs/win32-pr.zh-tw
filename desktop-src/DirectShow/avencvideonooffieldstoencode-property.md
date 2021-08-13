---
description: 指定要編碼的欄位數目。
ms.assetid: 5848493c-1f8e-4fe2-8261-dfdc8f61b265
title: 'AVEncVideoNoOfFieldsToEncode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 525deb0bbacf90eaffe2946ab569e419a68774f42390d6d2c85a355f2f390a7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119274978"
---
# <a name="avencvideonooffieldstoencode-property"></a>AVEncVideoNoOfFieldsToEncode 屬性

指定要編碼的欄位數目。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoNoOfFieldsToEncode**

## <a name="remarks"></a>備註

若為漸進式影片，請將此屬性設定為要編碼的畫面格數目的兩倍。

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

 

 




