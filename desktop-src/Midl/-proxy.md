---
title: /proxy 參數
description: /Proxy 參數會指定 COM 介面的介面 proxy 檔案名。
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- /proxy 參數 MIDL
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841472"
---
# <a name="proxy-switch"></a>/proxy 參數

**/Proxy** 參數會指定 COM 介面的介面 proxy 檔案名。

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*proxy \_ 檔案名 \_* 
</dt> <dd>

指定覆寫預設介面 proxy 檔案名的檔案名。 檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

指定的檔案名會取代將 \_ P. C 加入至 IDL 檔案名稱所取得的預設檔案名。 / [**Proxy**](proxy.md) 參數不會影響 RPC 介面。

如果 *proxy \_ 檔案名 \_* 不包含明確路徑，則會將檔案寫入至目前的目錄或 [**/out**](-out.md) 參數所指定的目錄。 *Proxy 檔案名中的明確 \_ \_* 路徑會覆寫 **/out** 參數規格。

如需其他 MIDL 編譯器所產生之介面 proxy 檔案和其他檔案的詳細描述，請參閱 [一般 Midl 命令列語法](general-midl-command-line-syntax.md)。

## <a name="examples"></a>範例

**midl/proxy 我的 \_ proxy .c 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/iid**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




