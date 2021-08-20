---
title: /env 參數
description: /Env 參數會選取應用程式執行所在的環境。
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /env 參數 MIDL
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86114a14d3e8fd9a5f8ca01da6bea259fd635f4758101c0bfab54d03d2986fa6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992355"
---
# <a name="env-switch"></a>/env 參數

**/Env** 參數會選取應用程式執行所在的環境。

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32 * * * *


</dt> <dd>

指示 MIDL 編譯器產生32位環境的存根檔或類型程式庫檔案。

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

指示 MIDL 編譯器為 Intel 架構64位 (IA64) 環境產生存根檔案或類型程式庫檔案。

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * *


</dt> <dd>

指示 MIDL 編譯器為 Advanced 微型裝置64位 (AMD64) 環境產生存根檔案或類型程式庫檔案。

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>win64 * * * *


</dt> <dd>

與 *ia64* 相同的行為。

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

**/Env** 參數主要會影響在該環境中用於結構的封裝層級。 請務必為 MIDL 編譯器和 C 編譯器指定相同的封裝層級設定。

**/Env** 參數會決定封裝層級和其他設定，如下所示：

-   當您指定 **win32** 時，產生的存根會針對所有涉及遠端作業的類型使用 C-編譯器封裝層級8。 [**Int**](int.md)資料類型都是32位。 指標是32位。
-   當您指定 **ia64** 或 **AMD64** 時，MIDL 編譯器會以跨編譯器模式執行，表示 (Intel 或 AMD) 64 位平臺。 產生的存根會針對所有涉及遠端作業的類型使用 C 編譯器封裝層級8。 [**Long**](long.md)和 [**int**](int.md)資料類型是32位。 指標是64位。

[**/Align**](-align.md)、 [**/pack**](-pack.md)和 [**/Zp**](-zp.md)參數的優先順序高於 **/env** 設定。

如需 MIDL 和 RPC 64 位支援的詳細資訊，請參閱 [設計64位相容的介面](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces)。

## <a name="examples"></a>範例

**midl/env win32 檔案名 .idl**

**midl/env ia64 檔案名 .idl**

**midl/env amd64 檔案名 .idl**

**midl/env win64 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/pack**](-pack.md)
</dt> <dt>

[**/Zp**](-zp.md)
</dt> </dl>

 

 