---
title: 了 nocode 屬性
description: '\ 了 nocode \ 屬性用於 ACF 標頭或個別的函式，以防止產生用戶端 stub 程式碼。'
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- 了 nocode 屬性 MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ec4612bc1bd5db1a8cdcbecdced51911591cdf5c482c83381f86deafd66a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066958"
---
# <a name="nocode-attribute"></a>了 nocode 屬性

**\[ 了 nocode \]** 屬性可用於 ACF 標頭或個別的函式，以防止產生用戶端 stub 程式碼。

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>參數

<dl> <dt>

*ACF-介面-屬性* 
</dt> <dd>

指定套用至整個介面的一或多個屬性清單。 有效的屬性包括 **\[** [**auto \_ 控制碼**](auto-handle.md) **\]** 或 **\[** [**隱含 \_ 控制碼**](implicit-handle.md) **\]** ，以及程式 **\[** [**代碼**](code.md) **\]** 或 **\[ \] 了 nocode**。 當有兩個或多個介面屬性存在時，它們必須以逗號分隔。

</dd> <dt>

*介面-名稱* 
</dt> <dd>

指定介面的名稱。 在 DCE 相容性模式中，介面名稱必須符合 IDL 檔案中指定的介面名稱。 當您使用 MIDL 編譯器參數 [**/acf**](-acf.md)時，acf 中的介面名稱和 IDL 檔案中的介面名稱可能會不同。

</dd> <dt>

*檔案名-清單* 
</dt> <dd>

指定一或多個 C 語言標頭檔名稱的清單（以逗號分隔）。 必須提供完整的檔案名（包括副檔名）。

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

指定套用至指定類型的一或多個屬性清單（以逗號分隔）。 有效的類型屬性包括 [ **\[** [**配置**](allocate.md)] **\]** 。

</dd> <dt>

*typename* 
</dt> <dd>

指定 IDL 檔案中定義的類型。 ACF 中的類型屬性只能套用至 IDL 檔案中先前定義的類型。

</dd> <dt>

*ACF 函式-屬性* 
</dt> <dd>

指定套用至整個函數的屬性，例如， **\[** [**通訊 \_ 狀態**](comm-status.md) **\]** 。 函數屬性以方括弧括住。 以逗號分隔多個函式屬性。

</dd> <dt>

*函數名稱* 
</dt> <dd>

指定 IDL 檔案中所定義的函式名稱。

</dd> <dt>

*ACF-參數-屬性* 
</dt> <dd>

指定適用于參數的 ACF 屬性。 請注意，您可以將零個或更多屬性套用至參數。 以逗號分隔多個參數屬性。 ACF 參數屬性以方括弧括住。

</dd> <dt>

*參數-名稱* 
</dt> <dd>

指定 IDL 檔案中定義之函式的參數。 函數的每個參數都必須以相同的順序指定，並且使用 IDL 檔案中所定義的相同名稱。

</dd> </dl>

## <a name="remarks"></a>備註

**\[ 了 nocode \]** 屬性可以出現在 ACF 標頭中，也可以套用至個別的函式。

如果 **\[ 了 nocode \]** 屬性出現在 ACF 標頭中，則不會為任何遠端函式產生用戶端 stub 程式碼，除非它有 **\[** [**code**](code.md) **\]** function 屬性。 您可以藉由將程式 **\[ 代碼 \]** 屬性指定為函數屬性，來覆寫個別函式標頭中的 **\[ 了 nocode \]** 屬性。

當 **\[ 了 nocode \]** 屬性出現在函式的屬性清單中時，不會為函式產生任何用戶端 stub 程式碼。

當下列情況時，不會產生用戶端 stub 程式碼：

-   ACF 標頭包含 **\[ 了 nocode \]** 屬性。
-   **\[ 了 nocode \]** 屬性會套用至函數。
-   **\[** [**Local**](local.md) **\]** 屬性會套用至介面檔中的函式。

程式 **\[** [**代碼**](code.md) **\]** 或 **\[ 了 nocode \]** 可以出現在函式的屬性清單中，而您所選擇的只會出現一次。

當伺服器 stub 產生時，會忽略 **\[ 了 nocode \]** 屬性。 當您在 DCE 相容性模式中產生伺服器 stub 時，不能套用此應用。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**分配**](allocate.md)
</dt> <dt>

[**自動 \_ 處理**](auto-handle.md)
</dt> <dt>

[**代碼**](code.md)
</dt> <dt>

[**通訊 \_ 狀態**](comm-status.md)
</dt> <dt>

[**隱含 \_ 控制碼**](implicit-handle.md)
</dt> </dl>

 

 




