---
description: 將物件宣告為挑選任何常數，以避免在 DirectXMath 程式庫的多個位置中，將該物件的重複重載用於 (和宣告) 。
ms.assetid: FDE5C004-9E8E-4890-8FDC-987C1569D8E5
title: XMGLOBALCONST 宏
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6675b17138fca66e293321a9d848262a8bffc94e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998084"
---
# <a name="xmglobalconst-macro"></a>XMGLOBALCONST 宏

將物件宣告為 *挑選任何* 常數，以避免在 DirectXMath 程式庫的多個位置中，將該物件的重複重載用於 (和宣告) 。

## <a name="syntax"></a>語法

``` syntax
#define XMGLOBALCONST  extern const __declspec(selectany)
```

## <a name="remarks"></a>備註

使用 XMGLOBALCONST 允許全域常數的規格。 這有助於減少應用程式資料區段的大小、避免重複的物件建立和損毀，並減少載入和儲存作業。

## <a name="requirements"></a>規格需求

**標頭：** 在 DirectXMath 中宣告。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[DirectXMath 程式庫宏](ovw-xnamath-reference-macros.md)
</dt> <dt>

[DirectXMath 程式庫中的全域常數](pg-xnamath-internals.md)
</dt> <dt>

[selectany](/previous-versions/visualstudio/visual-studio-6.0/aa273550(v=vs.60))
</dt> <dt>

[declspec](/previous-versions/visualstudio/visual-studio-6.0/aa273692(v=vs.60))
</dt> </dl>

 

 
