---
description: 不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將浮點值載入至 XMVECTOR 類型的實例。
ms.assetid: bafaa59f-fd1b-e252-cbbd-903df796fde0
title: 'XMVECTORF32 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1a39de246e3e0e4ab9a96197dbe4a286cb6ecabe327d60e5c506795af79dd11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739778"
---
# <a name="xmvectorf32-data-type"></a>XMVECTORF32 資料類型

不透明的可移植型別，可支援使用 C/c + + 初始化運算式語法，將浮點值載入至 [**XMVECTOR**](xmvector-data-type.md) 類型的實例。


```C++
typedef XMVECTORF32 vectorf32;
```



## <a name="remarks"></a>備註

如需在 c + + 中進行程式設計時可使用的其他功能（例如，如函式和運算子）的清單， `XMVECTORF32` 請參閱 [XMVECTORF32 延伸](ovw-xmvectorf32-extensions.md)模組。

**XMVECTORF32**、 [**XMVECTORU32**](xmvectoru32-data-type.md)、 [**XMVECTORI32**](xmvectori32-data-type.md)和 [**XMVECTORU8**](xmvectoru8-data-type.md)結構是以機制的形式提供，可從不同的常數資料類型建立 [**XMVECTOR**](xmvector-data-type.md) ， (浮點數、不帶正負號整數、整數和位元組) 使用初始化運算式。

這是支援 [**XMVECTOR**](xmvector-data-type.md)的必要動作，因為它本身不支援初始化運算式，因為可攜性和優化原因。

例如：


```
XMVECTOR data;
XMVECTORF32 floatingVector = { 0.f, 0.f, 0.1f, 1.f };
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

[**XMVECTORI32 資料類型**](xmvectori32-data-type.md)
</dt> <dt>

[**XMVECTOR 資料類型**](xmvector-data-type.md)
</dt> <dt>

[**XMVECTORU32 資料類型**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8 資料類型**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTORF32 資料類型**](xmvectorf32-data-type.md)
</dt> </dl>

 

 




