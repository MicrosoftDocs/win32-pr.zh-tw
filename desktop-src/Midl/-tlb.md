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
ms.openlocfilehash: 081723648788ec51fa65a4770deb336f665804a9527dc223000826870dbe1ee0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643748"
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

 

 




