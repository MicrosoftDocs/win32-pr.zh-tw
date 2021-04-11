---
title: pointer_default 屬性
description: '\ 指標 \_ default \ 屬性會指定除了出現在參數清單中最上層指標以外的所有指標的預設指標屬性。'
ms.assetid: a6e83034-8adb-483d-8d1e-432a1aed22c6
keywords:
- pointer_default 屬性 MIDL
topic_type:
- apiref
api_name:
- pointer_default
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08555358eb0abd42957d60527e18a4fd4f49165a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023330"
---
# <a name="pointer_default-attribute"></a>指標 \_ 預設屬性

**\[ 指標 \_ default \]** 屬性會指定除了出現在參數清單中最上層指標以外的所有指標的預設指標屬性。

``` syntax
pointer_default ( ptr | ref | unique )
```

## <a name="parameters"></a>參數

這個屬性沒有任何參數。

## <a name="examples"></a>範例

``` syntax
[
    uuid(6B29FC40-CA47-1067-B31D-00DD010662DA), 
    version(3.3), 
    pointer_default(unique)
] 
interface dictionary 
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**介面**](interface.md)
</dt> <dt>

[陣列和 Sized-Pointer 屬性](array-and-sized-pointer-attributes.md)
</dt> <dt>

[**陣 列**](arrays-1.md)
</dt> <dt>

[陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**獨特**](unique.md)
</dt> <dt>

[預設指標類型](/windows/desktop/Rpc/default-pointer-types)
</dt> </dl>

 

 