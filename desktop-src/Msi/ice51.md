---
description: ICE51 會檢查是否已提供字型資源檔的標題。
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194097"
---
# <a name="ice51"></a>ICE51

ICE51 會檢查是否已提供字型資源檔的標題。

您必須提供沒有內嵌名稱之字型資源的標題。 只有 simsun18030.ttc、. ttf 和. otf 字型資源檔不需要標題，因為這些檔案包含內嵌名稱。 請勿提供包含內嵌名稱的字型資源標題，因為系統接著會註冊字型兩次。

**[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** ICE51 不會檢查 otf 字型資源檔。

## <a name="result"></a>結果

如果有任何 simsun18030.ttc、ttf 和 otf 字型資源檔具有標題，ICE51 會張貼錯誤。 如果有任何其他字型資源檔沒有標題，ICE51 會張貼警告。

## <a name="example"></a>範例

ICE51 會針對所顯示的範例報告下列警告。

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

ICE51 會針對所顯示的範例報告下列錯誤訊息。

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

[檔資料表](file-table.md) (部分) 



| 檔案  | FileName  |
|-------|-----------|
| Font1 | font1. ttf |
| Font2 | font2.fon |



 

[字型資料表](font-table.md)



| 檔案\_ | FontTitle          |
|--------|--------------------|
| Font1  | 非常酷炫的字型 |
| Font2  |                    |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



