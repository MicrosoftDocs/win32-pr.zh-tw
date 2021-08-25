---
title: /U 參數
description: /U 參數會藉由將名稱傳遞到 C 預處理器來移除任何先前的名稱定義，如同由取消定義的指示詞。
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U 參數 MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9eab33e5aff861c1afecaafa52e04964ef286c5835e0a6992a3d369210f8927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895768"
---
# <a name="u-switch"></a>/U 參數

**/U** 參數會藉由將名稱傳遞到 C 預處理器來移除任何先前的名稱定義，如同由未 **\# 定義** 的指示詞。

``` syntax
midl /U name
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*name* 
</dt> <dd>

指定要傳遞到 C 預處理器的定義的名稱，如同由未 **\# 定義** 的指示詞一樣。 名稱是由 C 預處理器預先定義，或由使用者先前定義。

</dd> </dl>

## <a name="remarks"></a>備註

命令列中可以使用多個 **/u** 指示詞。 **/U** 參數與未定義名稱之間的空格是選擇性的。

當 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且 [**/cpp \_ opt**](-cpp-opt.md) 參數不是時，MIDL 編譯器會串連/cpp cmd 參數所指定的字串 \_ 與 [**/i**](-i.md)、 [**/d**](-d.md)和 **/u** 選項，並使用這個串連的字串來叫用每個 IDL 和 ACF 原始程式檔的 C 預處理器。 當指定 MIDL 編譯器參數 **/no \_ cpp** 或 **/cpp \_ OPT** 時，會忽略 midl 編譯器參數 **/u** 。

## <a name="examples"></a>範例

**midl/UUNICODE 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/D**](-d.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> </dl>

 

 




