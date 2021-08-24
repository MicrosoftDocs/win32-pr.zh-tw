---
title: /no_def_idir 參數
description: 使用/I 參數指定目錄時，/no \_ def \_ idir 參數會指示 MIDL 編譯器只搜尋以/i 參數指定的目錄。
ms.assetid: 9a396de4-332d-4832-8e8b-291690cd3a10
keywords:
- /no_def_idir switch MIDL
topic_type:
- apiref
api_name:
- /no_def_idir
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c93d61bff28ad0aa4306047755c88419d0b925431f9b3ea476ec957dcd62b98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811298"
---
# <a name="no_def_idir-switch"></a>/no \_ def \_ idir 參數

使用 [**/i**](-i.md) 參數指定目錄時， **/no \_ def \_ idir** 參數會指示 MIDL 編譯器只搜尋以 **/i** 參數指定的目錄，並忽略目前的目錄以及 INCLUDE 環境變數所指定的目錄。

``` syntax
midl /no_def_idir
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

使用 [**/i**](-i.md) 參數指定目錄時， **/no \_ def \_ idir** 參數會指示 MIDL 編譯器只搜尋目前目錄。

## <a name="examples"></a>範例

``` syntax
; search only the current directory 
midl /no_def_idir filename.idl  

; search only the specified directories 
midl /no_def_idir /I c:\c700\include filename.idl 
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**/I**](-i.md)
</dt> </dl>

 

 




