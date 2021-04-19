---
description: 不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法將整數值載入至 XMVECTOR 類型的實例。
ms.assetid: 6564030e-b6e9-0c4f-4e2a-4132e4264c94
title: 'XMVECTORI32 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ac36caf97a62037223840e9220876f1c7a1f09a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995505"
---
# <a name="xmvectori32-data-type"></a>XMVECTORI32 資料類型

不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法將整數值載入至 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。


```C++
typedef XMVECTORI32 vectori32;
```



## <a name="remarks"></a>備註

如需在 c + + 中進行程式設計時可使用的其他功能（例如，如函式和運算子）的清單， `XMVECTORI32` 請參閱 [XMVECTORI32 延伸](ovw-xmvectori32-extensions.md)模組。

[**XMVECTORF32**](xmvectorf32-data-type.md)、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 **XMVECTORI32** 和 [**XMVECTORU8**](xmvectoru8-data-type.md)結構是以機制的形式提供，可從不同的常數資料類型建立 [**XMVECTOR**](xmvector-data-type.md) ， (浮點數、不帶正負號整數、整數和位元組) 使用初始化運算式。

這是支援 [**XMVECTOR**](xmvector-data-type.md)的必要動作，因為它本身不支援初始化運算式，因為可攜性和優化原因。

例如：


```
XMVECTOR data;
XMVECTORI32 intVector = { -1, 5, 33, 0 };
data = intVector;
```



**命名空間**：使用 DirectX

### <a name="platform-requirements"></a>平台需求

Microsoft Visual Studio 2010 或 Microsoft Visual Studio 2012 搭配 Windows 8 的 Windows SDK。 Win32 桌面應用程式、Windows Store 應用程式和 Windows Phone 8 應用程式均可支援。

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

[**XMVECTORU32 資料類型**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8 資料類型**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTORI32 資料類型**](xmvectori32-data-type.md)
</dt> </dl>

 

 




