---
title: /cstruct_out 參數
description: /Cstruct_out 參數會修改 COM 介面的 C 定義，此介面會傳回結構，以符合 c + + 實施者所提供的 ABI。
keywords:
- /cstruct_out switch MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844507"
---
# <a name="cstruct_out-switch"></a>/cstruct \_ out 參數

此參數會修改 COM 介面的 C 定義，這個介面會傳回結構以符合 c + + 實施者所提供的 ABI。

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

某些介面定義 (特別 `d3d12.idl` 是) 包含傳回 `__stdcall` 結構的方法。 MSVC 中的 C 和 c + + Abi 會因其實作為這類函式的方式而有所不同：

* C 會將它們視為一般函式，將隱藏 `this` 指標作為第一個參數。 編譯器會套用小型結構優化，以允許小於8個位元組的結構 (或更大的值（如果所有值都是在暫存器中傳回的浮點數) ）。 只有較大的結構會升級為使用隱藏的參數和呼叫端配置的傳回值。
* C + + 會將它們視為成員函式。 編譯器 *一律* 會藉由將隱藏的參數插入 (呼叫端配置的傳回值指標，) 做為指標之後的第二個參數 `this` 。 它也會傳回相同的指標做為其傳回值。

此參數會強制產生的標頭中介面的 C 定義，假設實作者使用 c + +，而 C 程式碼則應該改為明確地使用 c + + ABI。 這表示函式包含傳回值指標的隱藏參數，並會直接傳回該指標，而不是直接傳回結構。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>
