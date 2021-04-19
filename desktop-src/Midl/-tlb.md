---
title: /tlb 參數
description: /Tlb 參數會指定 MIDL 編譯器所產生之類型程式庫的檔案名。
ms.assetid: 7d5d9f92-ed1a-46bc-beb1-4be70d0a4813
keywords:
- /tlb 參數 MIDL
topic_type:
- apiref
api_name:
- /tlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff0078f75865c8048eead911b310e102b779317
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968073"
---
# <a name="tlb-switch"></a>/tlb 參數

**/Tlb** 參數會指定 MIDL 編譯器所產生之類型程式庫的檔案名。

``` syntax
midl /tlb filename
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*filename* 
</dt> <dd>

指定 (TLB) 檔的輸出類型程式庫名稱。 根據預設，如果未使用 **/tlb** 參數，則 tlb 檔案的名稱會與 IDL 檔案相同，副檔名為。Tlb。

</dd> </dl>

## <a name="examples"></a>範例

**midl/tlb newname .tlb**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/notlb**](-notlb.md)
</dt> </dl>

 

 




