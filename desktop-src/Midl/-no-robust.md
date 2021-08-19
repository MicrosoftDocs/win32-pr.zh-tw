---
title: /no_robust 參數
description: /No \_ 健全的參數會指示 MIDL 編譯器明確停用/robust 命令列功能。 /Robust 命令列參數與其相關聯的功能是 MIDL version 6.0.359 和更新版本的預設編譯器設定。
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust switch MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808853"
---
# <a name="no_robust-switch"></a>/no \_ 穩固的交換器

**/No \_ 健全** 的參數會指示 MIDL 編譯器明確停用 [**/robust**](-robust.md)命令列功能。 **/Robust** 命令列參數與其相關聯的功能是 MIDL version 6.0.359 和更新版本的預設編譯器設定。

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

使用 MIDL 版本6.0.359 和更新版本時，MIDL 編譯器預設會設定 [**/robust**](-robust.md) 。 如果產生的存根需要在 Microsoft Windows NT、Windows 95/98 或 Windows Me 上執行，則必須使用 **/no \_ 健全** 的命令列參數來停用 **/robust** 功能。

## <a name="examples"></a>範例

**midl/no \_ 健全的檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




