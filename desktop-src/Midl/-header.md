---
title: /header 參數
description: /Header 參數會指定標頭檔的名稱。
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /header 參數 MIDL
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde032d611cb09f3da2d048bfab85bd3b0a1c8aadebf251fe8c01ecd8630a36e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808968"
---
# <a name="header-switch"></a>/header 參數

**/Header** 參數會指定標頭檔的名稱。

``` syntax
midl /header filename
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*filename* 
</dt> <dd>

指定覆寫預設標頭檔名稱的標頭檔名稱。 檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

指定的檔案名會取代預設的檔案名。 預設檔案名的取得方式是將 IDL 副檔名 (取代為副檔名 .h 的 idl) 。 若為 OLE 介面， **/header** 參數會覆寫介面標頭檔案的預設名稱。

當您匯入檔案時，指定的檔案名只適用于一個標頭檔，也就是對應至命令列上指定之 IDL 檔案的標頭檔。

如果 *filename* 未包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。 *檔案名* 中的明確路徑會覆寫 **/out** 參數規格。

## <a name="examples"></a>範例

**midl/header "bar. h" 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> </dl>

 

 




