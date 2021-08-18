---
title: include 屬性
description: ACF include 語句會指定要包含在產生的存根程式碼中的一或多個標頭檔。
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- 包含屬性 MIDL
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 827ec8deec34a42d39fc3973dff73e9912ecb96bfee62e348ef7aebfee6ee9f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067200"
---
# <a name="include-attribute"></a>include 屬性

ACF **include** 語句會指定要包含在產生的存根程式碼中的一或多個標頭檔。

``` syntax
include filenames;
```

## <a name="parameters"></a>參數

<dl> <dt>

*檔案名* 
</dt> <dd>

指定一或多個 C 語言標頭檔的名稱。 使用完整的檔案名，包括。H 副檔名並以引號括住每個檔案名。 以逗號分隔多個 C 語言標頭檔名稱。

</dd> </dl>

## <a name="remarks"></a>備註

由於 **include** 語句的結果，產生的 stub 程式碼將包含 C 預處理器 **\# include** 語句。 您會在編譯存根時提供 C 語言標頭檔。 Include 語句依賴 C 編譯器機制來搜尋目錄結構中包含的檔案。

> [!Note]  
> 使用匯 [**入**](import.md) 指示詞，而不是包含您想要提供給 IDL 檔案之資料類型之系統檔案的 **include** 指示詞。 匯 **入** 指示詞會忽略函式原型，並可讓您使用 MIDL 編譯器參數，以優化支援常式的產生。

 

## <a name="examples"></a>範例

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[應用程式佈建檔 (ACF) ](application-configuration-file-acf-.md)
</dt> <dt>

[**進口**](import.md)
</dt> <dt>

[匯入檔案和型別程式庫](importing-files-and-type-libraries.md)
</dt> <dt>

[匯入系統標頭檔](importing-system-header-files.md)
</dt> </dl>

 

 




