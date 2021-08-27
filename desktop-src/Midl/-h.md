---
title: /h 參數
description: /H 選項的功能相當於/header 選項。
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h 參數 MIDL
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71bf02668a583b330684338cbc3f639fbbda5a340c7226e10956233aa8dc9ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105608"
---
# <a name="h-switch"></a>/h 參數

**/H** 選項的功能相當於 [**/header**](-header.md)選項。

``` syntax
midl /h filename
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*filename* 
</dt> <dd>

指定覆寫預設標頭檔名稱的標頭檔名稱。 檔案名可以用雙引號括住 ( ") 來防止 shell 解讀特殊字元。

</dd> </dl>

## <a name="remarks"></a>備註

**/H** 參數指定 *檔案名* 作為標頭檔的名稱，其中包含 idl 檔案中包含的所有定義，而不含 idl 語法。 這個檔案可以用來做為 C 或 c + + 標頭檔。

## <a name="examples"></a>範例

**midl/h tlibhead .h 檔案名 .idl**

**midl/h "midl .h" 檔案名 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> </dl>

 

 




