---
title: /ms_ext 參數
description: 自 MIDL 3.0 版起，ms ext 參數所啟用的功能 \_ 現在是 midl 編譯器的預設模式。
ms.assetid: 175894c9-fa7e-4907-966d-e9df5a8e2745
keywords:
- /ms_ext switch MIDL
topic_type:
- apiref
api_name:
- /ms_ext
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73bee998e96d26c0f5bb2a1e0f28446433681a7175ff181556ad7976c58af356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118644557"
---
# <a name="ms_ext-switch"></a>/ms \_ ext 參數

自 MIDL 3.0 版起， **ms \_ ext** 參數所啟用的功能現在是 midl 編譯器的預設模式。

``` syntax
midl /ms_ext
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

使用參數將不會產生編譯器錯誤，因此您不需要從現有的 makefile 移除對 **/ms \_ ext** 或 [**/c \_ ext**](-c-ext.md) 的參考。

下列適用于憑證 DCE 的 Microsoft 擴充功能現在預設為可用：

-   OLE 物件的介面定義。 如需針對 OLE 介面產生之檔案的詳細資訊，請參閱[針對 COM 介面產生](files-generated-for-a-com-interface.md)的檔案。
-   在用戶端上指定靜態回呼函數的 [**\[ 回呼 \]**](callback.md)屬性
-    (加上 *引號的 \_ 字串*) 和 [**\# pragma midl \_ echo**](pragma.md)的 [**cpp \_ 引號**](cpp-quote.md)
-   [**wchar \_ t**](wchar-t.md) 寬字元類型、常數和字串
-    (稀疏枚舉器的 [**列舉初始化**](enum.md)) 
-   作為大小和鑒別子規范的運算式
-   [處理延伸模組](/windows/desktop/Rpc/microsoft-rpc-binding-handle-extensions)
-   [指標屬性類型繼承](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
-   [多個介面](/windows/desktop/Rpc/registering-interfaces)
-   介面區塊外部的定義
-   您可以省略 [](/windows/desktop/Rpc/directional-parameter-attributes) \[ [**中的**](in.md)方向屬性 [](out-idl.md) ，放大\]

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[指標屬性類型繼承](/windows/desktop/Rpc/pointer-attribute-type-inheritance)
</dt> <dt>

[**/app \_ 設定**](-app-config.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> </dl>

 

 