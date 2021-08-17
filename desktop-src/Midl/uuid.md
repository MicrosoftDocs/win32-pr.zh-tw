---
title: uuid 屬性
description: '\ Uuid \ 介面屬性會指定 (UUID) 的通用唯一識別碼，該識別碼會指派給介面，並將它與其他介面區別。'
ms.assetid: 72cf12f5-49cd-440d-9665-73211509d050
keywords:
- uuid 屬性 MIDL
topic_type:
- apiref
api_name:
- uuid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ce85ad2014e1f0563e2c20af7abec3cc476fab330b38340162f28fd390a5f8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066638"
---
# <a name="uuid-attribute"></a>uuid 屬性

**\[ Uuid \]** 介面屬性會指定 (uuid) 的通用唯一識別碼，該識別碼會指派給介面，並將它與其他介面區別。

``` syntax
uuid (string-uuid) 
uuid ("string-uuid")
```

## <a name="parameters"></a>參數

<dl> <dt>

*字串-uuid* 
</dt> <dd>

指定一個字串，其中包含8個十六進位數位，後面接著連字號，再接著三個4個十六進位數位的群組，後面接著連字號，再接著12個十六進位數位。 您可以用引號括住 UUID 字串，但使用 MIDL 編譯器參數 [**/osf**](-osf.md)時除外。

</dd> </dl>

## <a name="remarks"></a>備註

執行時間程式庫會使用 **\[ uuid \]** 屬性指定的介面 UUID，以協助建立用戶端和伺服器應用程式之間的通訊。 **\[ Uuid \]** 屬性可以出現在 RPC 介面或 COM 介面的介面屬性清單中。

若為 RPC 介面，介面屬性清單必須包含 **\[ uuid \]** 屬性或 **\[** [**區域**](local.md) **\]** 屬性，而您所選擇的屬性必須正好發生一次。 如果清單包含 **\[ uuid \]** 屬性，它也可以包含 **\[** [**version**](version.md) **\]** 屬性。

針對 (物件介面屬性識別的 COM 介面 **\[** [](object.md) **\]**) ，介面屬性清單必須包含 **\[ uuid \]** 屬性，但不能包含 **\[ version \]** 屬性。 COM 介面的清單可以包含 **\[ 本機 \]** 屬性，即使 **\[ uuid \]** 屬性存在也一樣。

Microsoft RPC 支援 DCE IDL 的延伸模組，可讓 UUID 以雙引號括住 ( "" "" ) 。 以引號括住的表單對於將 UUID 數位解讀為浮點數的 C 編譯器預處理器是必要的。

所有 UUID 值都應該是電腦產生的，以確保唯一性。 使用 Uuidgen.exe 公用程式來產生唯一的 UUID 值。

介面的 UUID 和版本號碼會用來判斷用戶端是否可以系結至伺服器。 若要讓用戶端系結至伺服器，在用戶端和伺服器介面中指定的 UUID 必須相同。

請注意，沒有屬性的介面可以匯入基底 IDL 檔案中。 不過，介面必須只包含沒有任何程式的資料類型。 如果介面中包含一個程式，則必須指定 local 或 UUID 屬性。

## <a name="examples"></a>範例

``` syntax
uuid(6B29FC40-CA47-1067-B31D-00DD010662DA) 
 
uuid("6B29FC40-CA47-1067-B31D-00DD010662DA")
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**介面**](interface.md)
</dt> <dt>

[**當地**](local.md)
</dt> <dt>

[**物件**](object.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**版本**](version.md)
</dt> </dl>

 

 




