---
title: /syntax_check 參數
description: /Syntax \_ 檢查參數表示編譯器只會檢查語法，並且不會產生輸出檔。
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check switch MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678519"
---
# <a name="syntax_check-switch"></a>/syntax \_ 檢查參數

**/Syntax \_ 檢查** 參數表示編譯器只會檢查語法，並且不會產生輸出檔。

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

此參數會覆寫所有其他參數，這些參數會指定輸出檔案的相關資訊。

您也可以使用 MIDL 編譯器選項 [**/Zs**](-zs.md)來指定語法檢查模式。

## <a name="examples"></a>範例

**midl/Zs 檔案名 .idl**

**midl/syntax \_ 檢查檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Zs**](-zs.md)
</dt> </dl>

 

 




