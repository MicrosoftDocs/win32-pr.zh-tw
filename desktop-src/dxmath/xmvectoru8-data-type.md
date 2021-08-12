---
description: 不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint8 \_ t 值載入 XMVECTOR 類型的實例。
ms.assetid: ab73ac2c-f178-1bb9-910d-9eef5fc6f5df
title: 'XMVECTORU8 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff3c335df3e74bc58776883b15d724c65d558bad30fc37e0e28547102260301a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118276194"
---
# <a name="xmvectoru8-data-type"></a>XMVECTORU8 資料類型

不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將 uint8 \_ t 值載入 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。


```C++
typedef XMVECTORU8 vectoru8;
```



## <a name="remarks"></a>備註

如需使用 c + + 進行程式設計時可使用 XMVECTORU8 的其他功能（例如，如函式和運算子）的清單，請參閱 [XMVECTORU8 擴充](ovw-xmvectoru8-extensions.md)功能。

[**XMVECTORF32**](xmvectorf32-data-type.md)、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 [**XMVECTORI32**](xmvectori32-data-type.md)和 **XMVECTORU8** 結構是以機制的形式提供，可從不同的常數資料類型建立 [**XMVECTOR**](xmvector-data-type.md) ， (浮點數、不帶正負號整數、整數和位元組) 使用初始化運算式。

這是支援 [**XMVECTOR**](xmvector-data-type.md)的必要動作，因為它本身不支援初始化運算式，因為可攜性和優化原因。

例如：

``` syntax
XMVECTOR data;
XMVECTORU8  byteVector = { (uint8_t)  1,(uint8_t) 16,(uint8_t)101,(uint8_t) 62,
                           (uint8_t)  4,(uint8_t)  0,(uint8_t)  2,(uint8_t) 99,
                           (uint8_t)  9,(uint8_t) 18,(uint8_t)  0,(uint8_t)  0,
                           (uint8_t)100,(uint8_t) 51,(uint8_t) 23,(uint8_t)117};

data = floatingVector;
```

**命名空間**：使用 DirectX

### <a name="platform-requirements"></a>平台需求

Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。 支援 Win32 傳統型應用程式、Windows 儲存應用程式，以及 Windows Phone 8 個應用程式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>DirectXMath。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectXMath 程式庫類型](ovw-xnamath-reference-types.md)
</dt> <dt>

[**XMVECTOR 資料類型**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORF32 資料類型**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORI32 資料類型**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTORU32 資料類型**](xmvectoru32-data-type.md)
</dt> <dt>

[XMVECTORU8 延伸模組](ovw-xmvectoru8-extensions.md)
</dt> </dl>

 

 




