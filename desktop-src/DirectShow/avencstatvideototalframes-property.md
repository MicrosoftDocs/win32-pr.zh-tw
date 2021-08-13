---
description: 傳回編碼器收到的影片框架數目。
ms.assetid: 3de49105-3c74-4a52-9cac-465b4abfcbf5
title: 'AVEncStatVideoTotalFrames 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 461708e9006db183992cf550bf7f98eeaeacbfe16c100675ab4992b54f0768d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663439"
---
# <a name="avencstatvideototalframes-property"></a>AVEncStatVideoTotalFrames 屬性

傳回編碼器收到的影片框架數目。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncStatVideoTotalFrames**

## <a name="remarks"></a>備註

編碼完成之後，就可以使用這個屬性。

這個屬性的值是傳送至編碼器的畫面格總數，包括已卸載的框架。 若要取得編碼的框架數目，請閱讀 [**AVEncStatVideoCodedFrames**](avencstatvideocodedframes-property.md) 屬性。

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

 

 




