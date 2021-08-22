---
title: /align 參數
description: /Align 參數的功能與 MIDL/Zp 選項相同，而且 MIDL 編譯器只會針對回溯相容性與 Mktyplib.exe 進行辨識。
ms.assetid: 7f303c49-a6b5-4e3c-95e5-5c49e338c766
keywords:
- /align 參數 MIDL
topic_type:
- apiref
api_name:
- /align
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 187607b783678d3045224daec021eabf436fa8ba1884128789f44b06ac4365ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067648"
---
# <a name="align-switch"></a>/align 參數

**/Align** 參數的功能與 midl [**/Zp**](-zp.md)選項相同，而且 midl 編譯器只會針對回溯相容性與 mktyplib.exe 進行辨識。

> [!Note]  
> Mktyplib.exe 工具已淘汰。 請改用 MIDL 編譯器。

 

``` syntax
midl /align:alignment
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*對準* 
</dt> <dd>

指定程式庫中類型的對齊方式。 *對齊* 值可以是1、2、4或8。 值1表示自然對齊; *n* 表示位元組 *n* 的對齊方式。 當您未指定 **/align** 參數時，預設值為8。

</dd> </dl>

## <a name="remarks"></a>備註

如果您要產生新的 makefile，請使用 [**/Zp**](-zp.md) 參數。

對齊值會對應到 Microsoft C/c + + 編譯器所使用的 [**/Zp**](-zp.md) 選項值。 當您叫用 MIDL 編譯器時，請務必指定相同的對齊方式。

如需詳細資訊，請參閱 Microsoft C/c + + 程式設計檔。 如需使用非標準封裝層級的潛在危險討論，請參閱 [**/Zp**](-zp.md) 說明主題。

## <a name="examples"></a>範例

**midl/align：4檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 




