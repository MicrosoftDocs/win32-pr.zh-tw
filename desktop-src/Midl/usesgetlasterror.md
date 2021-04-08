---
title: usesgetlasterror 屬性
description: '\ Usesgetlasterror \ 屬性工作表示呼叫端可以呼叫 GetLastError 來取得錯誤碼。'
ms.assetid: 8e9ab8b5-f446-4aab-bb40-b6f78799e18e
keywords:
- usesgetlasterror 屬性 MIDL
topic_type:
- apiref
api_name:
- usesgetlasterror
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0f403430f70fde71696ec2a35a34161f08bada9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681817"
---
# <a name="usesgetlasterror-attribute"></a>usesgetlasterror 屬性

**\[ Usesgetlasterror \]** 屬性會向呼叫端發出信號，告知呼叫端可以呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)來取得錯誤碼。

``` syntax
[
    module-attributes
]
module module-name
{
    [entry(entry-id), usesgetlasterror [, other-attributes]] return-type function-name(param-list);
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*模組屬性* 
</dt> <dd>

將套用至 [**模組**](module.md)的零或多個 MIDL 屬性。

</dd> <dt>

*模組名稱* 
</dt> <dd>

[**模組**](module.md)的識別碼名稱。

</dd> <dt>

*專案識別碼* 
</dt> <dd>

指定模組進入點–函數名稱或整數識別碼。

</dd> <dt>

*其他屬性* 
</dt> <dd>

將套用至遠端程式的零或多個 MIDL 屬性。

</dd> <dt>

*傳回類型* 
</dt> <dd>

完成時，遠端程式將會傳回的資料類型。

</dd> <dt>

*函數名稱* 
</dt> <dd>

在 IDL 檔案中定義之遠端程式的名稱。

</dd> <dt>

*param 清單* 
</dt> <dd>

遠端程式的零或多個參數。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ Usesgetlasterror \]** 屬性可以在模組進入點上設定，如果該進入點使用 Windows 函數 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)傳回錯誤碼。 屬性會告知呼叫端，如果呼叫該函式時發生錯誤，呼叫端可以呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 來取得錯誤碼。

## <a name="examples"></a>範例

``` syntax
[
    dllname("MyOwn.dll")
] 
module MyModule
{
    [entry("One"), usesgetlasterror, bindable, requestedit,
     propputref, defaultbind] HRESULT Func1(
         [in]IUnknown * iParam1, 
         [out] long * Param2) ;
    [entry("TwentyOne"), usesgetlasterror, 
     hidden, vararg] SAFEARRAY (int) Func2(
         [in, out] SAFEARRAY (variant) *varP) ;

    // Other module definition statements.
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> </dl>

 

 