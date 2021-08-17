---
description: 用來代表 4 32 位浮點數或整陣列件向量的可移植型別，每個都能以最佳方式對齊，並對應至硬體向量暫存器。
ms.assetid: 1a044094-444d-e787-fa6a-76e88531aef1
title: 'XMVECTOR 資料類型 (DirectXMath .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0a65c7da346163c3cbfaab7c68982f56eb6c424b7f74a3ec01c754eb4104a5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094478"
---
# <a name="xmvector-data-type"></a>XMVECTOR 資料類型

用來代表 4 32 位浮點數或整陣列件向量的可移植型別，每個都能以最佳方式對齊，並對應至硬體向量暫存器。

## <a name="remarks"></a>備註

如需在 c + + 中進行程式設計時可使用的其他功能（例如，如函式和運算子）的清單， `XMVECTOR` 請參閱 [XMVECTOR 延伸](ovw-xmvector-extensions.md)模組。

在 DirectXMath 程式庫中，為了完全支援可攜性和優化，其 `XMVECTOR` 設計是不透明的型別。 的實際執行 `XMVECTOR` 相依于平臺。

一般情況下，程式碼不應該依賴任何特定平臺的特定執行方式的細節 `XMVECTOR` 。 平臺特定的執行具有下列特性：

-   它們不是可移植的。
-   它們可能會在版本之間變更。
-   Injudicious 使用的實作為詳細資料可能很理想。

開發人員應該使用 DirectXMath 程式庫的 [存取](ovw-xnamath-reference-functions-accessors.md)子、 [載入](ovw-xnamath-reference-functions-load.md)和 [儲存](ovw-xnamath-reference-functions-storage.md) 函式來取得和設定向量，以及使用 [DirectXMath 程式庫4d 向量函數](ovw-xnamath-reference-functions-vector4.md) 來操作它們。

針對需要如何在不同平臺上執行之詳細資訊的專案 `XMVECTOR` ，請參閱連結 [庫內部](pg-xnamath-internals.md)。

### <a name="compiler-aliases"></a>編譯器別名

DirectXMath .h 標頭檔會使用物件的別名 `XMVECTOR` ，特別是 **CXMVECTOR** 和 **FXMVECTOR**。 標頭會使用這些別名，以符合不同編譯器的最佳內嵌呼叫慣例。 大部分使用 DirectXMath 的專案，都足以將這些類型視為的確切別名 `XMVECTOR` 。

例如：


```
[CDATA[
typedef const XMVECTOR FXMVECTOR;
typedef const XMVECTOR CXMVECTOR;
]]
```



針對需要不同平臺如何處理其呼叫慣例之詳細資訊的專案，請參閱連結 [庫內部](pg-xnamath-internals.md)。

針對 XNAMATH 2.x， `XMVECTOR` 資料類型具有. x、. y、. z、. 和. w 元素成員，這通常會造成效能不佳。 使用 XM \_ STRICT \_ VECTOR4 型別可讓您加入宣告不透明資料類型的 DirectXMath 定義。

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

[**XMVECTORF32 資料類型**](xmvectorf32-data-type.md)
</dt> <dt>

[**XMVECTORU32 資料類型**](xmvectoru32-data-type.md)
</dt> <dt>

[**XMVECTORU8 資料類型**](xmvectoru8-data-type.md)
</dt> <dt>

[**XMVECTOR 資料類型**](xmvector-data-type.md)
</dt> </dl>

 

 




