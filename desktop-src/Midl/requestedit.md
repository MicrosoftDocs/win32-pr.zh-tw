---
title: requestedit 屬性
description: '\ Requestedit \ 屬性工作表示屬性支援 OnRequestEdit 通知。'
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- requestedit 屬性 MIDL
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51a894e5d4a09e7535e10a73e1bd118245e5886e0cdbb23b0f0645e588ab4adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146351"
---
# <a name="requestedit-attribute"></a>requestedit 屬性

**\[ Requestedit \]** 屬性指出屬性支援 **OnRequestEdit** 通知。

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a>參數

<dl> <dt>

*選用-屬性* 
</dt> <dd>

零或多個 MIDL 屬性。

</dd> <dt>

*傳回類型* 
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

支援 **OnRequestEdit** 通知表示在進行變更之前，物件會將變更屬性之許可權的要求傳送給用戶端。 物件可以支援資料系結，但不能有這個屬性。

### <a name="flags"></a>Flags

FUNCFLAG \_ FREQUESTEDIT、VARFLAG \_ FREQUESTEDIT

## <a name="examples"></a>範例

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
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

 

 