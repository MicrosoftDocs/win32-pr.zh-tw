---
title: /D 參數
description: /D 參數會定義要傳遞給 C 預處理器的名稱和選擇性值，如同由 \ define 指示詞一樣。 命令列中可以使用多個/D 指示詞。
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D 參數 MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092398"
---
# <a name="d-switch"></a>/D 參數

**/D** 參數會定義要傳遞給 C 預處理器的名稱和選擇性的值，如同由 **\# 定義** 指示詞一樣。 命令列中可以使用多個 **/d** 指示詞。

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*name* 
</dt> <dd>

指定已定義的名稱，此名稱會在 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且未出現 [**/cpp \_ Opt**](-cpp-opt.md) 參數時傳遞給 C 預處理器。

</dd> <dt>

*definition* 
</dt> <dd>

指定與定義的名稱相關聯的值。

</dd> </dl>

## <a name="remarks"></a>備註

**/D** 參數和定義的名稱之間的空格是選擇性的。

當 [**/cpp \_ cmd**](-cpp-cmd.md) 參數存在且 [**/cpp \_ opt**](-cpp-opt.md) 參數不是時，MIDL 編譯器會串連 **/cpp \_ cmd** 參數所指定的字串與 [**/i**](-i.md)、 **/d** 和 [**/U**](-u.md) 選項，並使用這個串連的字串來叫用每個 IDL 和 ACF 原始程式檔的 C 預處理器。

當指定 MIDL 編譯器參數 [/no \_ cpp](-no-cpp-nocpp.md)或 [**/cpp \_ OPT**](-cpp-opt.md)時，會忽略 midl 編譯器參數 **/d** 。

## <a name="examples"></a>範例

**midl-DUNICODE filename .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[**/I**](-i.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ cpp**](-no-cpp-nocpp.md)
</dt> <dt>

[**U**](-u.md)
</dt> </dl>

 

 




