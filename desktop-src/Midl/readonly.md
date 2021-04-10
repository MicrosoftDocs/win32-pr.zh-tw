---
title: readonly 屬性
description: '\ Readonly \ 屬性禁止指派給變數。'
ms.assetid: b81064e6-e788-48d1-9958-203f1e3c7e4d
keywords:
- readonly 屬性 MIDL
topic_type:
- apiref
api_name:
- readonly
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b4ef4ca5f32b96146ed5ab0ec085d32b24dca3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933190"
---
# <a name="readonly-attribute"></a>readonly 屬性

**\[ Readonly \]** 屬性禁止指派給變數。

``` syntax
[readonly [, optional-attributes]] data-type identifier
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用-屬性* 
</dt> <dd>

零或多個 MIDL 屬性。

</dd> <dt>

*資料類型* 
</dt> <dd>

*識別碼* 所包含的資料類型。

</dd> <dt>

*identifier* 
</dt> <dd>

軟體可參考資料儲存位置的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Readonly \]** 屬性禁止指派給變數。 只有在參數層級才支援 **\[ readonly \]** ，而不是在方法層級支援。

### <a name="flags"></a>Flags

VARFLAG \_ FREADONLY

## <a name="examples"></a>範例

``` syntax
HRESULT Method3([in, readonly] int iMmutable);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[TYPEFLAGS](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 