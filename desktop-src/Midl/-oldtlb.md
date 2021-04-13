---
title: /oldtlb 參數
description: /Oldtlb 參數會指示 MIDL 編譯器產生舊格式的類型程式庫。
ms.assetid: cf5fe000-7262-4812-a6ab-f12a558ac068
keywords:
- /oldtlb 參數 MIDL
topic_type:
- apiref
api_name:
- /oldtlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a08e468d0acff16aa1df4a45fcacafeb676b00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375085"
---
# <a name="oldtlb-switch"></a>/oldtlb 參數

**/Oldtlb** 參數會指示 MIDL 編譯器產生舊格式的類型程式庫。

``` syntax
midl /oldtlb
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

**/Oldtlb** 參數會覆寫預設值，並指示 MIDL 編譯器在目前的 Windows 版本上，使用 [CreateTypeLib](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib)而不是 [CreateTypeLib2](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-createtypelib2)來產生舊格式的類型程式庫。

## <a name="examples"></a>範例

**midl/oldtlb 檔案名 .idl**

**midl/oldtlb myoldodl. odl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/newtlb**](-newtlb.md)
</dt> </dl>

 

 