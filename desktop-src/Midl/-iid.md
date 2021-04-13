---
title: /iid 參數
description: /Iid 參數會指定 COM 介面之介面識別碼檔案的名稱，並覆寫將 \_ i. c 加入至 IDL 檔案名所取得的預設名稱。
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /iid 參數 MIDL
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373228"
---
# <a name="iid-switch"></a>/iid 參數

**/Iid** 參數會指定 COM 介面之介面識別碼檔案的名稱，並覆寫將 \_ i. c 加入至 IDL 檔案名所取得的預設名稱。

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*filename* 
</dt> <dd>

指定介面識別碼檔案名，此名稱會覆寫 COM 介面的預設介面識別碼檔案名。 檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

**/Iid** 參數不會影響 RPC 介面。

如果 *filename* 未包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。 *檔案名* 中的明確路徑會覆寫 **/out** 參數規格。

## <a name="examples"></a>範例

**midl/iid "my \_ iid .c" 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




