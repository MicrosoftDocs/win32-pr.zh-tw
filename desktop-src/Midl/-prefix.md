---
title: /prefix 參數
description: /Prefix 參數會指示 MIDL 編譯器將前置詞字串新增至用戶端和/或伺服器 stub 常式名稱。
ms.assetid: 5530e972-08bf-4cca-9bb4-9631db824bdb
keywords:
- /prefix 參數 MIDL
topic_type:
- apiref
api_name:
- /prefix
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79885a57f257fe2648a27fd67a014421b2c1c13a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104507625"
---
# <a name="prefix-switch"></a>/prefix 參數

**/Prefix** 參數會指示 MIDL 編譯器將前置詞字串新增至用戶端和/或伺服器 stub 常式名稱。 這可以用來允許單一程式同時是相同介面的用戶端和伺服器，而不會讓用戶端和伺服器端常式名稱彼此衝突。

``` syntax
midl /prefix { client | cstub | server | sstub | switch | all }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="client"></span><span id="CLIENT"></span>

<span id="client"></span><span id="CLIENT"></span>用戶端 * * * *


</dt> <dd>

只會影響用戶端存根常式名稱。

</dd> <dt>

<span id="cstub"></span><span id="CSTUB"></span>

<span id="cstub"></span><span id="CSTUB"></span>cstub * * * *


</dt> <dd>

與 *用戶端* 相同。 只會影響用戶端存根常式名稱。

</dd> <dt>

<span id="server"></span><span id="SERVER"></span>

<span id="server"></span><span id="SERVER"></span>伺服器 * * * *


</dt> <dd>

只會影響伺服器 stub 常式所呼叫的常式名稱。

</dd> <dt>

<span id="sstub"></span><span id="SSTUB"></span>

<span id="sstub"></span><span id="SSTUB"></span>sstub * * * *


</dt> <dd>

與 *伺服器* 相同。 只會影響伺服器 stub 常式所呼叫的常式名稱。

</dd> <dt>

<span id="switch"></span><span id="SWITCH"></span>

<span id="switch"></span><span id="SWITCH"></span>切換 * * * *


</dt> <dd>

會影響新增至標頭檔的額外原型。

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span id="all"></span><span id="ALL"></span>全部 * * * *


</dt> <dd>

會影響用戶端和伺服器 stub 常式名稱。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

如果用戶端常式的前置詞與伺服器端常式的前置詞不同，則產生的標頭檔會有用戶端常式原型和伺服器端常式原型。

當單一標頭檔會與多個 MIDL 編譯器執行的存根搭配使用時， **/prefix** 參數會很有用。 這會在標頭檔中強制執行其他常式原型。

在所有情況下，用戶端、伺服器和交換器前置詞都會覆寫所有前置詞。

## <a name="examples"></a>範例

**midl/prefix 用戶端 "c \_ " 伺服器 "s \_ "**

**midl/prefix 所有 "moo \_ "**

**midl/prefix 用戶端 "吠 \_ "**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




