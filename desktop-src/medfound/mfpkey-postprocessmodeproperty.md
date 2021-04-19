---
description: 指定此解碼器的後置處理模式。
ms.assetid: c6dab7f6-4a3e-45bb-b81c-5f4c39f9e954
title: 'MFPKEY_POSTPROCESSMODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4002deae63f1bdaea09ca31dd95bfec1cb594fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001631"
---
# <a name="mfpkey_postprocessmode-property"></a>MFPKEY \_ POSTPROCESSMODE 屬性

指定此解碼器的後置處理模式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

**g \_ wszWMVCForcePostProcessMode**

## <a name="data-type"></a>資料類型

**VT \_ I4**

## <a name="remarks"></a>備註

將此屬性設定為下列其中一個值。



| 值 | 意義                                                                                |
|-------|----------------------------------------------------------------------------------------|
| -1    | 此解碼器會根據可用的 CPU 資源，以更自我調整的方式設定後置處理模式。 |
| 0     | 此解碼器不會執行任何後置處理。                                               |
| 1     | 否則解碼器會執行快速 deblocking。                                                 |
| 2     | 此解碼器會執行完整 deblocking。                                                  |
| 3     | 此解碼器會執行快速的 deblocking 和 deringing。                                    |
| 4     | 此解碼器會執行完整的 deblocking 和 deringing。                                    |



 

因為這個屬性的值是從0到4，所以解碼複雜性、CPU 資源的使用和圖片品質都會增加。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------|
| 用戶端<br/> | Windows Vista 或 Windows 7<br/>                                                   |
| 標頭<br/> | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 




