---
title: immediatebind 屬性
description: '\ Immediatebind \ 屬性工作表示資料庫將會立即收到資料系結物件屬性之所有變更的通知。'
ms.assetid: 1c08ddca-e273-43b3-a8f6-ed7f552e4e0e
keywords:
- immediatebind 屬性 MIDL
topic_type:
- apiref
api_name:
- immediatebind
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc8a797514c15f8d4c46bb6161946d5d0b6bd10b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104185569"
---
# <a name="immediatebind-attribute"></a>immediatebind 屬性

**\[ Immediatebind \]** 屬性指出資料庫將會立即收到資料系結物件屬性之所有變更的通知。

``` syntax
[
    interface-attribute-list
] 
interface | dispinterface interface-name 
{
    [bindable, immediatebind[, optional-attribute-list]] returntype function-name(params)
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的一或多個屬性清單。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定 [**介面**](interface.md)[**或分配介面的**](dispinterface.md)名稱。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

零或多個函數屬性。

</dd> <dt>

*returntype* 
</dt> <dd>

指定函式的傳回型別。

</dd> <dt>

*函數名稱* 
</dt> <dd>

在 IDL 檔案中指定函數的名稱。

</dd> <dt>

*params* 
</dt> <dd>

零或多個函數參數。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Immediatebind \]** 屬性可讓控制項區分需要通知資料庫每項變更的屬性，以及不需要通知資料庫的屬性。 例如，即使控制項尚未遺失焦點，也應該立即將 checkbox 控制項的每個變更傳送到基礎資料庫。 不過，若為 listbox 控制項，則會在反白顯示不同的選取專案時進行變更。 在控制項失去焦點之前通知資料庫變更，將不會有效率且不需要。 **\[ Immediatebind \]** 屬性可讓您藉由在應立即回報變更的表單上設定 immediatebind 位，來指定個別的屬性。

具有 **\[ immediatebind \]** 屬性的屬性也必須具有可系結 **\[** [](bindable.md) **\]** 屬性。

### <a name="flags"></a>Flags

FUNCFLAG \_ FIMMEDIATEBIND、VARFLAG \_ FIMMEDIATEBIND

## <a name="examples"></a>範例

``` syntax
[
    uuid(12345678-1234-1234-1234-123456789ABC)
] 
interface MyObject : IUnknown
{
    properties:
    methods:
        [id(1), propget, bindable, immediatebind] long Size(void);

        [id(1), propput, bindable, 
         immediatebind] HRESULT Size([in]long lSize);
}
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**bindable**](bindable.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**dispinterface**](dispinterface.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 