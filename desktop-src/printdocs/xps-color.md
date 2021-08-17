---
description: 描述單一色彩值的結構。
ms.assetid: 710f3ef1-bbc3-416d-9faf-aa4a716007c2
title: 'XPS_COLOR (Xpsobjectmodel) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f771bcbb516352b2ef689060c11003808d434be8059d16af78fe8db646c97000
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971147"
---
# <a name="xps_color"></a>XPS \_ 色彩

描述單一色彩值的結構。

``` syntax
typedef union switch (XPS_COLOR_TYPE colorType) value
{
    case XPS_COLOR_TYPE_SRGB:
        struct {
            byte alpha, red, green, blue;
        } sRGB;
    case XPS_COLOR_TYPE_SCRGB:
        struct {
            FLOAT alpha, red, green, blue;
        } scRGB;
    case XPS_COLOR_TYPE_CONTEXT:
        struct {
            byte channelCount;
            FLOAT channels[9];
        } context;
} XPS_COLOR;
```

## <a name="remarks"></a>備註

結構的格式取決於 *colorType* 的值。

<dl>

[**XPS \_ 色彩 \_ 類型 \_ SRGB**](/previous-versions/windows/desktop/dd372944(v=vs.85))  
[**XPS \_ 色彩 \_ 類型 \_ SCRGB**](/previous-versions/windows/desktop/dd372943(v=vs.85))  
[**XPS \_ 色彩 \_ 類型 \_ 內容**](/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color)  
</dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]<br/>                          |
| 最低支援的伺服器<br/> | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 標頭<br/>                   | <dl> <dt>Xpsobjectmodel。h</dt> </dl>                                              |
| IDL<br/>                      | <dl> <dt>XpsObjectModel .idl</dt> </dl>                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

