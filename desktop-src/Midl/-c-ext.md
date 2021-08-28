---
title: /c_ext 參數
description: 此參數已從 MIDL 編譯器的3.0 版淘汰。 不過，使用 c \_ ext 參數將不會產生編譯器錯誤，因此您不需要從現有的 makefile 移除對/ms \_ ext 或/c \_ ext 的參考。
ms.assetid: 3d4072ba-5563-4014-a4ed-2e3aa26bb00a
keywords:
- /c_ext switch MIDL
topic_type:
- apiref
api_name:
- /c_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb0f63a2dcf53716ea7b8825791fb723fbc768f5c8d237ac1b75e78ddc31bc0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388258"
---
# <a name="c_ext-switch"></a>/c \_ ext 參數

此參數已從 MIDL 編譯器的3.0 版淘汰。 不過，使用 **c \_ ext** 參數將不會產生編譯器錯誤，因此您不需要從現有的 makefile 移除對 [**/ms \_ ext**](-ms-ext.md) 或 **/c \_ ext** 的參考。

``` syntax
midl /c_ext
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

下列功能現在預設為可用：

-   許多現有的標頭檔會使用不屬於 DCE IDL 的限定詞來定義具有辨識符號的類型，例如 **遠** 和 **stdcall**。 這些編譯器 (，而在 DCE 相容性模式中，MIDL 編譯器) 在嘗試處理這些限定詞時產生錯誤。 MIDL 編譯器可讓您編譯包含這些限定詞的 IDL 檔案。 類型限定詞不會影響資料在網路上的傳輸方式。
-   您可以省略方向屬性，例如 [**\[ in \]**](in.md)或 [**\[ out \]**](out-idl.md)。

預設模式支援下列 C 語言延伸模組：

-   結構和等位中的位欄位
-   以兩個斜線字元開頭的批註 (//) 
-   外部宣告
-   參數清單中有省略號的程式 ( ... ) 
-   在32位平臺上， [**int**](int.md) 是原生32位基底類型;在16位平臺上，可辨識 **int** 但不是可遠端處理的類型
-   未在遠端作業中使用的類型 [**void \***](void.md)
-   類型限定詞（包括具有 ANSI 一致前置詞的表單）包含兩個底線字元 **： cdecl**、 **\_ \_ cdecl**、 [**const**](const.md)、 **\_ \_ const**、 **export**、 **\_ \_ export**、 **far**、 **\_ \_ far**、 **loadds**、 **\_ \_ loadds**、 **near**、 **\_ \_ near**、 **pascal**、 **\_ \_ pascal**、 **stdcall**、 **\_ \_ stdcall**、 **volatile** 和 **\_ \_ volatile**。

如需宣告限定詞的詳細資訊，請參閱 Microsoft C/c + + 檔。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/app \_ 設定**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




