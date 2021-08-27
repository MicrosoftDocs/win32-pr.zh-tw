---
title: /cstub 參數
description: /Cstub 參數會指定 RPC 介面的用戶端 stub 檔案名。
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub 參數 MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b4f635b6d09c85b345eea6dcb7320294e226ad6f2540f01af1e9b3e8098671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105657"
---
# <a name="cstub-switch"></a>/cstub 參數

**/Cstub** 參數會指定 RPC 介面的用戶端 stub 檔案名。

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*stub \_ 檔案名 \_* 
</dt> <dd>

指定覆寫預設用戶端 stub 檔案名的檔案名。 檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

指定的檔案名會取代預設的檔案名。 根據預設，檔案名是藉由將副檔名 \_ c. 新增至 IDL 檔案的名稱取得。 此參數不會影響 OLE 介面。

當您匯入檔案時，指定的檔案名只適用于一個存根檔案，也就是對應至命令列上指定之 IDL 檔案的存根檔案。

如果 *存根 \_ 檔案名 \_* 不包含明確路徑，則會將檔案寫入至目前目錄或 [**/out**](-out.md) 參數所指定的目錄。 *存根檔案名中的明確 \_ \_* 路徑會覆寫 **/out** 參數規格。

**/Client** none 參數優先于 **/cstub** 參數。

## <a name="examples"></a>範例

**midl/cstub my \_ cstub .c 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




