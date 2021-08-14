---
title: 名稱語法
description: 遠端程序呼叫 (RPC) 和名稱語法。
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f63c86e6fe9283855e886014787fe36361bfbcdea3bc53e4078bbb43d193293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927817"
---
# <a name="name-syntax"></a>名稱語法

Microsoft RPC 接受符合下列語法的名稱：

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="name"></span><span id="NAME"></span>名字
</dt> <dd>

指定可包含任何字元的識別碼，除分隔斜線 (/) 字元以外。

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>domainname
</dt> <dd>

指定網域的名稱。

</dd> </dl>

選取名稱-語法類型的參數，以及指定名稱的字串，會提供給許多名稱服務介面 (NSI) RPC 函數。

Microsoft RPC 只支援一個名稱語法類型，如常數 RPC \_ C \_ NS \_ 語法 DCE 所指定 \_ 。 這個常數定義在標頭檔 RPCNSI 中。

RPC \_ C NS 語法 DCE 指定的名稱語法 \_ \_ \_ 是憑證 \_ DCE Cell Directory 服務 (cd) 名稱語法的延伸模組。 指定功能變數名稱的能力代表該語法的延伸。 只要整個字串小於256個字元，就能以斜線字元分隔的名稱沒有絕對限制。

斜線可讓您指定名稱的邏輯結構，但不會對應至物件本身中的邏輯結構。

 

 




