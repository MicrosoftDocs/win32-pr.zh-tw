---
title: public 屬性
description: '\ Public \ 屬性包含在類型程式庫中使用 typedef 關鍵字宣告的別名。'
ms.assetid: d4e90165-8b0d-47bb-998d-e515226be935
keywords:
- public 屬性 MIDL
topic_type:
- apiref
api_name:
- public
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8451ddf77b5074dbea609bfed144340dc877c00
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106967884"
---
# <a name="public-attribute"></a>public 屬性

**\[ Public \]** 屬性包含在類型程式庫中使用 [**typedef**](typedef.md)關鍵字宣告的別名。

``` syntax
typedef [public] data-type identifier;
```

## <a name="parameters"></a>參數

<dl> <dt>

*資料類型* 
</dt> <dd>

識別碼將為其別名的資料類型。

</dd> <dt>

*identifier* 
</dt> <dd>

軟體中將會知道 *資料類型* 的另一個名稱。

</dd> </dl>

## <a name="remarks"></a>備註

根據預設，以 [**typedef**](typedef.md)宣告且沒有其他屬性的別名會被視為 **\# 定義**，而且不會包含在類型程式庫中。 使用 **\[ public \]** 屬性可確保別名會成為類型程式庫的一部分。

> [!Note]  
> MIDL 編譯器要求您明確地將 **\[ 公用 \]** 屬性套用至您想要公開的每一個 typedef。

 

## <a name="examples"></a>範例

``` syntax
typedef [public] long MEMBERID;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**著**](typedef.md)
</dt> </dl>

 

 