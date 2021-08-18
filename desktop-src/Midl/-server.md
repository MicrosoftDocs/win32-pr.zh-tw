---
title: /server 參數
description: /Server 參數會導向 MIDL 編譯器，以產生 RPC 介面的伺服器端 C 來源檔案。
ms.assetid: c5ca6a47-e8b0-4a13-ba73-2d35a9ac8240
keywords:
- /server 參數 MIDL
topic_type:
- apiref
api_name:
- /server
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bf634e9ce91e937ff1e43b9059d12181dc723695139001ec368109d6fdf4a3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067468"
---
# <a name="server-switch"></a>/server 參數

**/Server** 參數會導向 MIDL 編譯器，以產生 RPC 介面的伺服器端 C 來源檔案。

``` syntax
midl /server { stub | none }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="stub"></span><span id="STUB"></span>

<span id="stub"></span><span id="STUB"></span>stub * * * *


</dt> <dd>

產生伺服器端檔案。

</dd> <dt>

<span id="none"></span><span id="NONE"></span>

<span id="none"></span><span id="NONE"></span>無 * * * *


</dt> <dd>

不會產生伺服器端檔案。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

如果未指定 **/server** 參數，MIDL 編譯器會產生伺服器存根檔案。 此參數不會影響 OLE 介面。

[ **無** ] 選項不會產生任何檔案。

**/Server** 參數優先于 **/sstub** 參數。

## <a name="examples"></a>範例

**midl/server 無**

**midl/server 存根**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/client**](-client.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




