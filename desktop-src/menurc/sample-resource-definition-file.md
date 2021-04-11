---
title: 範例 Resource-Definition 檔案
description: 定義名為圖形之應用程式資源的範例腳本檔案。
ms.assetid: 0362b1be-7671-4685-8eb8-bff502224939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e6a870b4b63b0e88e5ddcd069e8318e4bdb750
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021789"
---
# <a name="sample-resource-definition-file"></a>範例 Resource-Definition 檔案

下列範例顯示的腳本檔案定義了應用程式命名圖形的資源：

``` syntax
#include "shapes.h"

ShapesCursor  CURSOR  SHAPES.CUR
ShapesIcon    ICON    SHAPES.ICO

ShapesMenu MENU
{
    POPUP "&Shape"
    {
        MENUITEM "&Clear", ID_CLEAR
        MENUITEM "&Rectangle", ID_RECT
        MENUITEM "&Triangle", ID_TRIANGLE
        MENUITEM "&Star", ID_STAR
        MENUITEM "&Ellipse", ID_ELLIPSE
    }
}
```

[**Cursor**](cursor-resource.md)語句會為應用程式的資料指標資源 ShapesCursor 命名，並指定資料指標檔案圖形。[下一]，包含該資料指標的影像。

[**Icon**](icon-resource.md)語句會為應用程式的圖示資源 ShapesIcon 命名，並指定圖示檔圖形。.ICO，其中包含該圖示的影像。

[**Menu**](menu-resource.md)語句會定義名為 **ShapesMenu** 的應用程式功能表，這個快顯功能表具有五個功能表項目。

功能表定義的主體（以大括弧括住），或 **開頭** 和 **結尾** 關鍵字會指定每個功能表項目，以及當使用者選取該專案時所傳回的功能表識別碼。 例如，當使用者選取功能表識別碼識別碼時，功能表上的第一個專案會 **清除** \_ 。 功能表識別碼會定義在應用程式標頭檔中，即 .H。

 

 




