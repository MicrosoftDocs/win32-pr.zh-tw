---
title: import 屬性
description: 匯入指示詞會指定另一個 IDL、ODL 或標頭檔，其中包含您想要從主要 IDL 檔案參考的定義。
ms.assetid: b52fb2c7-ce60-474f-8833-7a821844f747
keywords:
- 匯入屬性 MIDL
topic_type:
- apiref
api_name:
- import
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64ff13c069c6bba819720a9d1120a42c25af4b51
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314767"
---
# <a name="import-attribute"></a>import 屬性

匯 **入** 指示詞會指定另一個 IDL、ODL 或標頭檔，其中包含您想要從主要 IDL 檔案參考的定義。

``` syntax
import "filename" [[ , ... ]] ;
```

## <a name="parameters"></a>參數

<dl> <dt>

*filename* 
</dt> <dd>

指定要匯入之標頭、IDL 或 ODL 檔案的名稱。

</dd> </dl>

## <a name="remarks"></a>備註

使用匯 **入** 指示詞時，匯入的檔案中的所有 IDL 語句（例如 typedef、常數宣告和介面定義）都會變成可供匯入。IDL 檔案。

匯入的檔案會分開處理 (這表示會從匯入 IDL 檔案) 獨立叫用 CPP 預處理器。 如此一來，預處理器指示詞（例如 \# define）不會將匯入的標頭或 IDL 檔案從匯入的 idl 檔案中執行。

如同 C 語言預處理器宏 **\# 在內**， **import** 指示詞會指示編譯器包含匯入的 IDL 檔案中所定義的資料類型。 和 **\# include** 指示詞不同，匯 **入** 指示詞會忽略程式原型，因為匯入檔案中的任何作業都不會產生任何 stub。

如需使用匯 **入** 將標頭檔併入 IDL 檔案的特定資訊，請參閱匯 [入系統標頭檔](importing-system-header-files.md)。

C 語言標頭 (。H) 針對介面產生的檔案不會直接包含匯入的型別，而是會針對對應至已匯入介面的標頭檔產生 **\# include** 指示詞。 例如，當您匯入基底時。IDL 至您衍生的。IDL，衍生產生的標頭檔。H 將包含指示詞， **\# 包含** BASE. H。

適用的規則如下：

-   匯 **入** 關鍵字是選擇性的，而且可以在 IDL 檔案中出現零次或多次。
-   每個 **import** 關鍵字都可以與一個以上的檔案名相關聯。
-   以逗號分隔多個檔案名。
-   您必須將檔案名括在引號內，並以分號 ( 結束 import 語句，) 。
-   您可以將沒有屬性的介面匯入至另一個 IDL 檔案。 不過，介面必須只包含資料類型;它不能包含任何程式。 如果匯入的介面中包含一個程式，您必須指定 [**本機**](local.md) 或 [**UUID**](uuid.md) 屬性。
-   匯 **入** 函式 idempotentÂ的是，一次匯入介面沒有額外的效果。

> [!Note]  
> 匯 **入** 指示詞的行為獨立于 MIDL 編譯器模式參數 [**/ms \_ ext**](-ms-ext.md) (預設) 、 [**/osf**](-osf.md)和 [**/app \_**](-app-config.md)設定。 不過，編譯器模式 (**/osf** 或 **/ms \_ ext**) 可能會影響匯入類型上的指標屬性裝飾。 如需詳細資訊，請參閱 [指標屬性類型繼承](/windows/desktop/Rpc/pointer-attribute-type-inheritance)。

 

## <a name="examples"></a>範例

``` syntax
import "myoldodl.odl";  
import "unknwn.idl";
import "part1.idl", "part2.idl", "part3.idl"; 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/app \_ 設定**](-app-config.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> <dt>

[**importlib**](importlib.md)
</dt> <dt>

[**包括**](include.md)
</dt> <dt>

[匯入系統標頭檔](importing-system-header-files.md)
</dt> <dt>

[匯入檔案和型別程式庫](importing-files-and-type-libraries.md)
</dt> <dt>

[**/ms \_ ext**](-ms-ext.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 