---
title: /client 參數
description: /Client 參數會指示 MIDL 編譯器產生 RPC 介面的用戶端 C 來源檔案。
ms.assetid: bce5af72-2201-4b42-9348-cb97f08b7fdf
keywords:
- /client 參數 MIDL
topic_type:
- apiref
api_name:
- /client
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbf7e17e1893b918d926cd94a93eb8b1c372ee75
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312962"
---
# <a name="client-switch"></a>/client 參數

**/Client** 參數會指示 MIDL 編譯器產生 RPC 介面的用戶端 C 來源檔案。

``` syntax
midl /client { stub | none }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub * * * *


</dt> <dd>

產生用戶端檔案。

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>無 * * * *


</dt> <dd>

不會產生任何用戶端檔案。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

未指定 **/client** 參數時，MIDL 編譯器會產生用戶端存根檔案。 此參數不會影響 OLE 介面。

**/Client** 參數優先于 [**/cstub**](-cstub.md)參數。

## <a name="examples"></a>範例

**midl/client 無檔案名 .idl**

**midl/client stub 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/server**](-server.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




