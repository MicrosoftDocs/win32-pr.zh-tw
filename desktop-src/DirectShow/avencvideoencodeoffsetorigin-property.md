---
description: 指定裁剪矩形的左邊和左上角（如果影片已裁剪）。
ms.assetid: 8ce8b3b8-dd91-41e1-a4ba-b0c2d9d0edd2
title: 'AVEncVideoEncodeOffsetOrigin 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7db4d685942b8c21f2d5047003f2172c54b1d50d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108985"
---
# <a name="avencvideoencodeoffsetorigin-property"></a>AVEncVideoEncodeOffsetOrigin 屬性

指定裁剪矩形的左邊和左上角（如果影片已裁剪）。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoEncodeOffsetOrigin**

## <a name="property-value"></a>屬性值

值的上層16位包含輸入框架左邊緣的位移（以圖元為單位）。 較低的16個位包含輸入框架上邊緣的位移（以圖元為單位）。

## <a name="remarks"></a>備註

應用程式可以設定此屬性來裁剪輸入影片。 您可以使用 [**AVEncVideoEncodeDimension**](avencvideoencodedimension-property.md) 屬性來指定裁剪矩形的寬度和高度。

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

 

 




