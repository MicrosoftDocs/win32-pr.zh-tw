---
title: /savePP 參數
description: 指定/savePP 指示詞時，MIDL 編譯器不會刪除 C/c + + 預處理器的輸出。
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP 參數 MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022493"
---
# <a name="savepp-switch"></a>/savePP 參數

指定 **/savePP** 指示詞時，MIDL 編譯器不會刪除 C/c + + 預處理器的輸出。

``` syntax
midl /savePP
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

此參數可讓開發人員分辨 MIDL 編譯器所剖析的內容，而且對進行調試很有用。 預處理器的輸出會寫入 TEMP 環境變數所指定之目錄中的一或多個暫存檔案。 輸出檔或檔案的名稱，會遵循中間 .tmp 的命名慣例 \* 。 請注意，單一編譯可能會產生數個前置處理的輸入資料流程;這是因為匯入 IDL 檔案（而不是使用 **\# include**）會導致個別的預處理器執行。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**/cpp \_ cmd**](-cpp-cmd.md)
</dt> <dt>

[**/cpp \_ opt**](-cpp-opt.md)
</dt> <dt>

[/no \_ cpp、/nocpp](-no-cpp-nocpp.md)
</dt> </dl>

 

 




