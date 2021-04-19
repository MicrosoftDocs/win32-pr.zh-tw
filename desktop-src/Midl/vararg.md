---
title: vararg 屬性
description: '\ Vararg \ 屬性指定函式接受不定數目的參數。 若要完成這項操作，最後一個參數必須是 VARIANT 型別的安全陣列，其中包含所有剩餘的參數。'
ms.assetid: df0995d3-5266-4a13-90aa-d78bfa753e0e
keywords:
- vararg 屬性 MIDL
topic_type:
- apiref
api_name:
- vararg
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3880a3713daaff13fe827beb989dd377440af4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "107001079"
---
# <a name="vararg-attribute"></a>vararg 屬性

**\[ Vararg \]** 屬性指定函式接受不定數目的參數。 若要完成這項操作，最後一個參數必須是 **VARIANT** 型別的安全陣列，其中包含所有剩餘的參數。

``` syntax
[vararg [, optional-attributes]] return-type function-name(
  [optional-param-attributes] param-list, 
  SAFEARRAY(VARIANT) last-param-name);
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用-屬性* 
</dt> <dd>

指定要套用至函數的零或多個屬性。 以逗號分隔多個屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

完成時遠端程式所傳回的資料類型。

</dd> <dt>

*函數名稱* 
</dt> <dd>

遠端程式的名稱。

</dd> <dt>

*選用-param-屬性* 
</dt> <dd>

指定要在屬性清單之後立即套用至函數參數的零或多個屬性。

</dd> <dt>

*param 清單* 
</dt> <dd>

指定所有參數，並儲存最後的、變化的參數。

</dd> <dt>

*last-param 名稱* 
</dt> <dd>

不同參數的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

您無法將 **\[** [**選擇性**](optional.md) **\]** 或 **\[** [**defaultvalue**](defaultvalue.md) **\]** 屬性套用至具有 **\[ \] vararg** 屬性之函式中的任何參數。

## <a name="examples"></a>範例

``` syntax
[vararg] VARIANT_BOOL Button([in]SAFEARRAY(VARIANT) psa);
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**值**](defaultvalue.md)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[**選**](optional.md)
</dt> </dl>

 

 