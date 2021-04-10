---
title: /acf 參數
description: /Acf 參數允許使用者提供明確的 ACF 檔案名。 參數也允許在 IDL 和 ACF 檔中使用不同的介面名稱。
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /acf 參數 MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103932739"
---
# <a name="acf-switch"></a>/acf 參數

**/Acf** 參數允許使用者提供明確的 acf 檔案名。 參數也允許在 IDL 和 ACF 檔中使用不同的介面名稱。

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*acf \_ 檔案名* 
</dt> <dd>

指定 ACF 的名稱。 空白字元不一定會出現在 **/acf** 參數和檔案名之間。

</dd> </dl>

## <a name="remarks"></a>備註

根據預設，MIDL 編譯器會藉由將 IDL 副檔名 (（通常是使用 ACF 的) idl 來取代）來建立 ACF 的名稱。 當 **/acf** 參數存在時，acf 會從指定的檔案名取得其名稱。 **/Acf** 參數僅適用于 MIDL 編譯器命令列上指定的 IDL 檔案。 它並不適用于匯入的檔案。

使用 **/acf** 參數時，acf 中的介面名稱不需要與 MIDL 介面名稱相符。 這項功能可讓介面共用 ACF 規格。

如果未指定 ACF 的絕對路徑，MIDL 編譯器會在目前的目錄中搜尋、由 [**/i**](-i.md) 選項提供的目錄，以及包含路徑中的目錄。

如果找不到 ACF，MIDL 編譯器會假設這個介面沒有 ACF。 如需目錄順序的詳細資訊，請參閱 [**/i**](-i.md) 和 [**/no \_ def \_ idir**](-no-def-idir.md) 參數的參考專案。 如需 **/acf** 的相關詳細資訊，請參閱 [) 檔案 (的 IDL 介面定義](interface-definition-idl-file.md)。

## <a name="examples"></a>範例

**midl/acf bar. acf filename .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/I**](-i.md)
</dt> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/no \_ def \_ idir**](-no-def-idir.md)
</dt> </dl>

 

 




