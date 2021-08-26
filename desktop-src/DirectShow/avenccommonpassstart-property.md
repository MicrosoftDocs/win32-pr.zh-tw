---
description: 啟動第一次編碼傳遞。
ms.assetid: a062be3f-7806-4f1c-b98e-2c9ed31f010c
title: 'AVEncCommonPassStart 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7830537e6345d43927c7009e0e3ec9148505217818e981d7354a100a4ff2d68e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000138"
---
# <a name="avenccommonpassstart-property"></a>AVEncCommonPassStart 屬性

啟動第一次編碼傳遞。

此屬性是唯寫的。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncCommonPassStart**

## <a name="property-value"></a>屬性值

這個屬性的值是要開始的編碼傳遞。 若要取得支援值的範圍，請查詢編碼器的 [**AVEncCommonMultipassMode**](avenccommonmultipassmode-property.md) 屬性。

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

 

 




