---
title: entry 屬性
description: '\ Entry \ 屬性會藉由識別 DLL 中的進入點，來指定模組中匯出的函式或常數。'
ms.assetid: 1d2d6429-d828-44ec-8b0a-cefb64c6e706
keywords:
- 專案屬性 MIDL
topic_type:
- apiref
api_name:
- entry
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e596284a83c48bcfc84ef4f7985aed7c33ba7da
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314743"
---
# <a name="entry-attribute"></a>entry 屬性

**\[ 專案 \]** 屬性會藉由識別 DLL 中的進入點，指定匯出的函式或模組中的常數。

``` syntax
[
    uuid(uuid-number), 
    entry(entry-id)
  [, optional-attribute-list]
]
module modulename 
{
    elementlist
};
```

## <a name="parameters"></a>參數

<dl> <dt>

*uuid-數位* 
</dt> <dd>

指定 [**模組**](module.md)的通用唯一識別碼。

</dd> <dt>

*專案識別碼* 
</dt> <dd>

指定模組進入點函數名稱或整數識別碼。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定要套用至 [**模組**](module.md)的 MIDL 編譯器的零或多個屬性。

</dd> <dt>

*modulename* 
</dt> <dd>

指定其他軟體元件用來表示 [**模組**](module.md)的名稱。

</dd> <dt>

*elementlist* 
</dt> <dd>

指定一或多個模組元素定義語句。

</dd> </dl>

## <a name="remarks"></a>備註

如果 **\[ 專案 \]** 屬性的 *entryid* 變數是字串，這就是命名的進入點。 如果 *entryid* 是數位，則進入點是由序數所定義。 這個屬性會提供方法來取得模組中的函式位址。

## <a name="examples"></a>範例

``` syntax
[
    dllname("MyAppsFirst.dll")
] 
module MyModule
{
    [entry(20), bindable, requestedit, 
     propputref, defaultbind ] HRESULT Func1(
         [in]IUnknown * Param1, 
         [out] MyType * Param2);
    [entry("TwentyOne"), hidden, vararg] SAFEARRAY (int) Func2(
        [in, out] SAFEARRAY (variant) *varP) ;
    [entry(22)] Float Func3(
        [in] lpstr pName, [in] double dLevel,
        [out] short * sByte) ;
    } ;
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**dllname**](dllname-str-.md)
</dt> <dt>

[**模組**](module.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 