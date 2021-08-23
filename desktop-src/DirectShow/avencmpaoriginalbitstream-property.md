---
description: 指定 MPEG-2 音訊資料流程中原始位的預設設定。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 62b56868-684f-4f28-90da-dac19cb07946
title: 'AVEncMPAOriginalBitstream 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46d39b34339e25d08b138fd1c55a64e8a84d6cf4b4db302cbab1e5f50b8ccebc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689738"
---
# <a name="avencmpaoriginalbitstream-property"></a>AVEncMPAOriginalBitstream 屬性

指定 MPEG-2 音訊資料流程中原始位的預設設定。 這個屬性會套用至 MPEG 音訊編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPAOriginalBitstream**

## <a name="property-value"></a>屬性值

這個屬性可以具有下列值。



| 值          | 描述          |
|----------------|----------------------|
| VARIANT \_ FALSE | 原始位為 off。 |
| VARIANT \_ TRUE  | 原始位為開啟。  |



 

## <a name="remarks"></a>備註

編碼器可能會根據輸入資料流程的內容來覆寫此設定。

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

 

 




