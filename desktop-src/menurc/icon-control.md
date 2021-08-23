---
title: 圖示控制項
description: 定義圖示控制項。 此控制項是顯示在對話方塊中的圖示。
ms.assetid: fd2e1e7a-f386-4fdc-8b05-afce19dd3e8d
keywords:
- 圖示控制項功能表和其他資源
topic_type:
- apiref
api_name:
- ICON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4fc5191457996aabe4a70fefcf64235b3a9573cf12733f9ca7bff2ece6356e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034286"
---
# <a name="icon-control"></a>圖示控制項

定義圖示控制項。 此控制項是顯示在對話方塊中的圖示。

**Icon** 控制項語句（您只能在 [**DIALOGEX**](dialogex-resource.md)語句中使用）會定義控制項的圖示資源識別碼、圖示控制項識別碼、位置和屬性。

``` syntax
ICON text, id, x, y [, width, height, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*文本*
</dt> <dd>

圖示的名稱 (不是) 在資源檔中的其他位置定義的檔案名。

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*寬度*
</dt> <dd>

此值會被忽略，且應設定為零。

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*高度*
</dt> <dd>

此值會被忽略，且應設定為零。

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*風格*
</dt> <dd>

控制項樣式。 這是選擇性參數。 唯一可指定的值為 **SS \_ 圖示** 樣式。 這是指定是否指定這個參數的預設樣式。

</dd> </dl>

如需控制語句之一般語法的詳細資訊，請參閱 [通用控制項參數](common-control-parameters.md)。

## <a name="examples"></a>範例

這個範例會定義圖示控制項，其圖示識別碼為901，而其名稱為 myicon：

``` syntax
ICON "myicon", 901, 30, 30
```

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**圖示**](icon-resource.md)
</dt> </dl>

 

 




