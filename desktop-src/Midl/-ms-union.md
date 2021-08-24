---
title: /ms_union 參數
description: /Ms 聯 \_ 集參數控制 nonencapsulated 聯集的 NDR 對齊。注意：此屬性是為了回溯相容性而提供。
ms.assetid: 683d1498-6419-4600-ad5b-c0b6ea44a8e1
keywords:
- /ms_union switch MIDL
topic_type:
- apiref
api_name:
- /ms_union
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b8e2f4b86929954ad67c845cf546d46f5950698fce7c21d721613af3611a066
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811388"
---
# <a name="ms_union-switch"></a>/ms 聯 \_ 集參數

**/Ms 聯 \_ 集** 參數控制 nonencapsulated 聯集的 NDR 對齊。

> [!Note]  
> 這個屬性是為了回溯相容性而提供。 不建議在新介面中使用。

 

``` syntax
midl /ms_union
```

## <a name="switch-options"></a>切換選項

此參數沒有任何參數。

## <a name="remarks"></a>備註

MIDL 編譯器會鏡像 nonencapsulated 聯集的憑證-DCE IDL 編譯器的行為。 不過，因為舊版 MIDL 編譯器沒有這樣做，所以 **/ms 聯 \_ 集** 參數會提供與舊版 midl 編譯器的介面相容性。

Ms 聯 \_ 集功能可以用來做為命令列參數 (**/ms 聯 \_ 集**) 、IDL 介面屬性或 idl 型別屬性。

## <a name="examples"></a>範例

**midl/ms 聯 \_ 集檔案 .idl**

## <a name="see-also"></a>另請參閱

<dl> <dt>

[一般 MIDL 命令列語法](general-midl-command-line-syntax.md)
</dt> <dt>

[ (IDL) 檔案的介面定義](interface-definition-idl-file.md)
</dt> </dl>

 

 




