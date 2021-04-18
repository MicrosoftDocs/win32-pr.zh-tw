---
title: /sal 參數
description: /Sal 參數會指示 MIDL 在產生的存根檔案中產生 SAL 注釋。
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /sal 參數 MIDL
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968674"
---
# <a name="sal-switch"></a>/sal 參數

**/Sal** 參數會指示 MIDL 在產生的存根檔案中產生 sal 注釋。

``` syntax
midl /sal
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

MIDL 會將指標和陣列參數標示為反映 IDL 檔案中的參數描述（由 RPC 和 NDR 封送處理引擎強制執行）的注釋。 除非命令列上也有 [**/sal \_ local**](-sal-local.md) ，否則 MIDL 不會針對以 [**\[ \] 區域**](local.md)屬性標記的介面方法中的參數建立批註。 若要覆寫 MIDL 產生的注釋，請使用 [ [**\[ 批註 \]**](annotate.md) ] 屬性。

MIDL 產生的注釋一律會加上 RPC 的前置詞 \_ \_ \_ ，而且需要使用 **rpcsal** 的標頭將批註轉譯成標準 SAL 注釋。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/sal \_ 本機**](-sal-local.md)
</dt> <dt>

[**\[注釋\]**](annotate.md)
</dt> </dl>

 

 




