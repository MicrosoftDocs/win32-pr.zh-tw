---
description: 以 \_ 16 位浮點數組成的 uint16 t 的別名，其中包含正負號位、5位偏誤的指數和10位尾數。
ms.assetid: E84E0EBA-5C34-41AA-84DB-7A65EBDCAD15
title: '半資料類型 (DirectXPackedVector .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a59b7288324ae5935a23e67a35f402ab6041da55073915d812b39096cab30733
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985038"
---
# <a name="half-data-type"></a>半資料類型

以16位浮點數組成的 **uint16 \_ t** 的別名，其中包含正負號位、5位偏誤的指數和10位尾數。


```C++
typedef uint16_t HALF;
```



## <a name="remarks"></a>備註

半資料類型相當於 IEEE 754 binary16 格式。

半 \_ 分鐘 = 6.10352 e-5f

半 \_ MAX = 65504 f。

如需一半資料類型的詳細資訊，請參閱 [半精確度浮點數格式](https://en.wikipedia.org/wiki/Half_precision_floating-point_format)。

**命名空間**：使用 DirectX：:P ackedvector

### <a name="platform-requirements"></a>平台需求

Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。 支援 Win32 傳統型應用程式、Windows 儲存應用程式，以及 Windows Phone 8 個應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|--------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DirectXPackedVector。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectXMath 程式庫類型](ovw-xnamath-reference-types.md)
</dt> </dl>

 

 




