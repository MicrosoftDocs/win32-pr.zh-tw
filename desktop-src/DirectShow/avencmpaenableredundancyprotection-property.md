---
description: 指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。 這個屬性會套用至 MPEG 音訊編碼器。
ms.assetid: 55f0de8b-26dd-4d48-b7ed-2ddcef630227
title: 'AVEncMPAEnableRedundancyProtection 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b50e010b0b088e8817eca4dae1989cd6f623f55a9616c4449df62f115f98ff7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824108"
---
# <a name="avencmpaenableredundancyprotection-property"></a>AVEncMPAEnableRedundancyProtection 屬性

指定是否要將迴圈冗余檢查 (CRC) 新增至框架頁首。 這個屬性會套用至 MPEG 音訊編碼器。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**變異 \_BOOL** (**VT \_ bool**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncMPAEnableRedundancyProtection**

## <a name="property-value"></a>屬性值

這個屬性可以具有下列值。



| 值          | 描述                |
|----------------|----------------------------|
| VARIANT \_ FALSE | 請勿加入 CRC 總和檢查碼。 |
| VARIANT \_ TRUE  | 加入 CRC 總和檢查碼。        |



 

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

 

 




