---
title: proxy 屬性
description: '\ Proxy \ 屬性可防止 Automation 註冊為雙重介面的 proxy/stub 處理常式。'
ms.assetid: 88e59938-83c9-436a-931c-f4396fdcf653
keywords:
- proxy 屬性 MIDL
topic_type:
- apiref
api_name:
- proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81cb7f67f87153825db59d921b6ee9ec7df6cd334ed2228896c8dec5f9d5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641417"
---
# <a name="proxy-attribute"></a>proxy 屬性

**\[ Proxy \]** 屬性會防止 Automation 註冊為雙重介面的 proxy/stub 處理常式。

``` syntax
[ 
    proxy, 
    uuid(string-uuid <>)
    [ , interface-attribute-list <>] 
] 
interface interface-name <> : base-interface <>
{
    ...
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*字串-uuid* 
</dt> <dd>

指定一個字串，其中包含8個十六進位數位，後面接著連字號，再接著三個4個十六進位數位的群組，後面接著連字號，再接著12個十六進位數位。 您可以用引號括住 UUID 字串，但使用 MIDL 編譯器參數 [**/osf**](-osf.md)時除外。

</dd> <dt>

*介面屬性清單* 
</dt> <dd>

指定套用至整個介面的零或多個 IDL 屬性清單。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

介面的名稱。

</dd> <dt>

*基底介面* 
</dt> <dd>

指定此衍生介面繼承成員函式、狀態碼和介面屬性之介面的名稱。 衍生介面不會繼承型別定義。 若要這樣做，請使用 [**import**](import.md) 關鍵字匯入基底介面的 IDL 檔案。

</dd> </dl>

## <a name="remarks"></a>備註

使用 \[  \] 雙重介面的 PROXY 屬性可防止 TLB 接管產生的存根。 如果指定了這個屬性，當 typelib 未註冊時，就不應該取消註冊 typelib proxy。

### <a name="flags"></a>Flags

<dl> <dt>

<span id="TYPEFLAG_PROXY"></span><span id="typeflag_proxy"></span>TYPEFLAG \_ PROXY
</dt> <dd>

介面可以用 TYPEFLAG proxy 旗標標示， \_ 表示它們將使用 PROXY/stub 動態連結程式庫。 此旗標指定當 typelib 未註冊時，不應該取消註冊 typelib proxy。

</dd> </dl>

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**使用 MIDL 產生類型程式庫**](generating-a-type-library-with-midl-2.md)
</dt> <dt>

[**雙**](dual.md)
</dt> <dt>

[**TYPEFLAGS**](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> </dl>

 

 