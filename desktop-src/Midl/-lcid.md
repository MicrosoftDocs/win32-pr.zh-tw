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
ms.openlocfilehash: 370548bb9899ce84173f2321a129aaeda1c6fe81
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312950"
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

指定 Windows 國家語言支援中使用的32位地區設定識別碼。 地區設定識別碼應以 decimal 指定。

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

 

 




