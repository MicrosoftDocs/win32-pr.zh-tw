---
description: 指定已編碼影片的寬度和高度（如果影片已裁剪）。
ms.assetid: d6217250-63ff-4dff-a357-ff4aaa764695
title: 'AVEncVideoEncodeDimension 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d99a0c14cbb3f67f7aa1c634a59c5f4cb9184dcd861bc8f14023c4afcebcefa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159317"
---
# <a name="avencvideoencodedimension-property"></a>AVEncVideoEncodeDimension 屬性

指定已編碼影片的寬度和高度（如果影片已裁剪）。

這是可讀寫的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoEncodeDimension**

## <a name="property-value"></a>屬性值

值的上層16位包含寬度（以圖元為單位），而較低的16個位包含高度（以圖元為單位）。

## <a name="remarks"></a>備註

應用程式可以設定此屬性來裁剪輸入影片。 指定的大小必須小於輸入影片框架的大小。 您可以使用 [**AVEncVideoEncodeOffsetOrigin**](avencvideoencodeoffsetorigin-property.md) 屬性來指定裁剪矩形的左邊和頂端角落。

編碼器可將此屬性作為功能傳回。

這個屬性也會與 h.264 [UVC 1.5 攝影機編碼器](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)一起使用。

針對 UVC 1.5 攝影機編碼器，不支援 [AVEncVideoEncodeOffsetOrigin](avencvideoencodeoffsetorigin-property.md) 。

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

 

