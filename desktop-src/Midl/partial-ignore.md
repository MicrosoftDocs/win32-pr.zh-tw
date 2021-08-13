---
title: partial_ignore 屬性
description: ACF 屬性 \ partial \_ ignore \ 會定義特殊版本的 \ unique \ 指標，以提供選擇性的 out 語義。
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore 屬性 MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac751e5b3bdb4a93c003e170333af8956048c9793630419fff0857d61f8c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641971"
---
# <a name="partial_ignore-attribute"></a>部分 \_ 忽略屬性

ACF 屬性 **\[ 部分 \_ 忽略 \]** 會定義提供選擇性 out 語義之 **\[ 唯一 \]** 指標的特殊版本。

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>備註

建立函式時，通常會允許使用者指定非 **Null** 指標給選擇性的傳回資料，通常稱為選擇性的輸出指標。 使用者所指向的記憶體通常不需要初始化。 這項技術代表透過 RPC 使用函式時的問題。

如果選擇性-out 指標有效，但指向未初始化的資料，RPC 會嘗試封送處理該資料並將其傳送至伺服器，這可能會導致封送處理失敗並中止呼叫。 即使封送處理成功，可能會有大量無用的資料傳送到伺服器。

這些問題的解決方式是將指標標示為 **\[ in、out、unique、 \_ partial \] ignore**。 所有四個屬性都必須存在。 當用戶端上的 **\[ 部分 \_ 忽略 \]** 指標封送處理時，傳送至伺服器的唯一資料就是顯示指標是否為 **Null** 的指示器。 如果指標為非 **Null**，則伺服器端常式會接收以零初始化之記憶體區塊的有效指標。 如果指標為 **null**，則伺服器端常式會收到 **null** 指標。

在這種情況下，指標的大小上限必須在編譯時期或根據輸入參數妥善定義，因為伺服器需要配置空間給所指向的記憶體位置。 例如，簡單 **\[ 字串 \]** 指標沒有定義完善的大小，因為字串是以 Null 字元隱含地結束。 在此情況下，藉由新增 **\[ 大小 \_ 為 \]** 屬性來指定字串大小上限，會達到定義完善的大小需求。

## <a name="examples"></a>範例

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**獨特**](unique.md)
</dt> </dl>

 

 




