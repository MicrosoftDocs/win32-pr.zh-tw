---
title: dllname (str) 屬性
description: '\ Dllname \ 屬性會定義包含模組進入點的 DLL 名稱。'
ms.assetid: dbf062ce-9dcc-4cc6-b7cd-cdc5945e399b
keywords:
- dllname (str) 屬性 MIDL
topic_type:
- apiref
api_name:
- dllname(str)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 990d277db855c2988021d19a0a756c49454546f7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023461"
---
# <a name="dllnamestr-attribute"></a>dllname (str) 屬性

**\[ Dllname \]** 屬性會定義包含模組進入點的 DLL 名稱。

``` syntax
[
    uuid(uuid-number), 
    dllname("filename")
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

*filename* 
</dt> <dd>

指定以 Null 終止的字串，其中包含 Dll 檔案的完整路徑。

</dd> <dt>

*選用-屬性-清單* 
</dt> <dd>

指定零個或更多 MIDL 介面屬性的清單。

</dd> <dt>

*modulename* 
</dt> <dd>

指定其他軟體元件可以用來參考模組的名稱。

</dd> <dt>

*elementlist* 
</dt> <dd>

指定一或多個模組元素定義語句。

</dd> </dl>

## <a name="remarks"></a>備註

模組上需要 **\[ dllname \]** 屬性。

## <a name="examples"></a>範例

``` syntax
[
    uuid(1e196b20-1f3c-1069-996b-00dd010fe676),
    helpstring("A meaningful comment"),   
    dllname("HANDY.DLL")
] 
module HandyStuff
{
    /* Module content definitions */
};
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**模組**](module.md)
</dt> <dt>

[**進入**](entry.md)
</dt> <dt>

[ODL 檔語法](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[ODL 檔案範例](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[使用 MIDL 產生類型程式庫](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 