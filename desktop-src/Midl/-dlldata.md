---
title: /dlldata 參數
description: /Dlldata 參數是用來指定為 proxy DLL 產生之 dlldata.c 檔的檔案名。 如果未指定/dlldata 參數，則會使用預設檔案名 Dlldata.c。
ms.assetid: 5211498b-c641-447f-9514-a98766e26ea9
keywords:
- /dlldata 參數 MIDL
topic_type:
- apiref
api_name:
- /dlldata
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d1274226ae9768d45bb11e1a1f5b55caeddcc247a74a7ac08e03e3fcdacb0e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105638"
---
# <a name="dlldata-switch"></a>/dlldata 參數

**/Dlldata** 參數是用來指定為 proxy DLL 產生之 dlldata.c 檔的檔案名。 如果未指定 **/dlldata** 參數，則會使用預設檔案名 dlldata.c。

``` syntax
midl /dlldata file-name
```

## <a name="switch-options"></a>切換選項

<dl> <dt>

*檔案名* 
</dt> <dd>

MIDL 編譯器將為 proxy DLL 產生的 C 原始程式檔名稱。

</dd> </dl>

## <a name="remarks"></a>備註

*檔案名* 所指定的檔案必須連結至 proxy DLL。 Dlldata.c 檔案包含 proxy DLL 的 class factory 所需的進入點和資料結構。 這些資料結構會指定 proxy DLL 中包含的物件介面。 Dlldata.c 檔案也會指定 proxy DLL 之 class factory 的類別識別碼。 這一律是第一個 proxy 檔案的第一個介面 (IID) 的 UUID，)  (依字母順序排列。

在將進入特定 proxy DLL 的所有 IDL 檔案上叫用 MIDL 時，應指定相同的 dlldata.c 檔。 Dlldata.c 檔案會在每個 MIDL 編譯期間建立或更新，以累加方式建立將進入 proxy DLL 的介面清單。

## <a name="examples"></a>範例

**midl/dlldata 資料 c。**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> </dl>

 

 




