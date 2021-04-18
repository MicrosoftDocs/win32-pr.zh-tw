---
title: /sstub 參數
description: /Sstub 參數會指定 RPC 介面的伺服器 stub 檔案名。
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub 參數 MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965621"
---
# <a name="sstub-switch"></a>/sstub 參數

**/Sstub** 參數會指定 RPC 介面的伺服器 stub 檔案名。

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*stub \_ 檔案名 \_* 
</dt> <dd>

指定覆寫預設伺服器 stub 檔案名的檔案名。 檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

指定的檔案名會取代預設的檔案名。 根據預設，檔案名是藉由將 \_ S. C 加入至 IDL 檔案的名稱取得。 此參數不會影響 OLE 介面。

當您匯入檔案時，指定的檔案名只適用于一個存根檔案，也就是對應至命令列上指定之 IDL 檔案的存根檔案。

如果 *存根 \_ 檔案名 \_* 不包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。 *存根檔案名中的明確 \_ \_* 路徑會覆寫 **/out** 參數規格。

**/Server** 無參數優先于 **/sstub** 參數。

## <a name="examples"></a>範例

**midl/sstub my \_ sstub .c 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




