---
title: /lcid 參數
description: /Lcid MIDL 編譯器選項可讓您在輸入檔、檔案名和目錄路徑中使用國際字元。
ms.assetid: 2ab4ba67-4414-4889-8ed7-83f4888caf8b
keywords:
- /lcid 參數 MIDL
topic_type:
- apiref
api_name:
- /lcid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ceff1f9a4ef2f6c95a8dac12ff689995efe4fdd3619cf48e11043967fec053
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385511"
---
# <a name="lcid-switch"></a>/lcid 參數

**/Lcid** MIDL 編譯器選項可讓您在輸入檔、檔案名和目錄路徑中使用國際字元。

``` syntax
midl /lcid localeID
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*localeID* 
</dt> <dd>

指定用於 Windows 國語言支援的32位地區設定識別碼。 地區設定識別碼應以 decimal 指定。

</dd> </dl>

## <a name="remarks"></a>備註

在輸入檔案中，您可以使用當地語系化的批註、字串、helpstrings 和識別碼。 尤其是， **/lcid** 參數提供完整的 DBCS 支援，以代表日文、中文和韓文等亞洲語言。

> [!Note]  
> **/Lcid** 參數可搭配 MIDL 版本3.01.75 和更新版本使用。

 

## <a name="examples"></a>範例

**midl/lcid 1041 iface .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**Lcid**](lcid.md)
</dt> </dl>

 

 




