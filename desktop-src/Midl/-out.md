---
title: /out 參數
description: /Out 參數會指定 MIDL 編譯器寫入輸出檔的預設目錄。
ms.assetid: 37cfe989-137a-4336-8c66-e6b9c23473df
keywords:
- /out 參數 MIDL
topic_type:
- apiref
api_name:
- /out
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d688f17957170c6f3a8887030ea2c67140c0ff8c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966222"
---
# <a name="out-switch"></a>/out 參數

**/Out** 參數會指定 MIDL 編譯器寫入輸出檔的預設目錄。

``` syntax
midl /out path-specification
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*路徑規格* 
</dt> <dd>

指定要在其中產生存根、標頭和交換器檔案之目錄的路徑。 您可以指定磁片磁碟機規格、絕對目錄路徑或兩者。 您可以使用雙引號 ( ") 來明確地括住路徑，以防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

您可以使用磁碟機號、絕對路徑名稱或兩者來指定輸出目錄。 **/Out** 選項可以搭配任何啟用個別輸出檔規格的參數使用。

未指定 **/out** 參數時，會將檔案寫入至目前的目錄。

藉由指定為 [**/cstub**](-cstub.md)、 [**/header**](-header.md)、 [**/proxy**](-proxy.md)或 [**/sstub**](-sstub.md)參數一部分的明確路徑名稱，可覆寫 **/out** 參數指定的預設目錄。

## <a name="examples"></a>範例

**midl/out c： \\ mydir \\ mysubdir \\ subdir2 更深層的檔案名 .idl**

**midl/out c： filename .idl**

**midl/out \\ mydir \\ mysubdir \\ 另一個檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/proxy**](-proxy.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




