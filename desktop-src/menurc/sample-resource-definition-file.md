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
# <a name="sample-resource-definition-file"></a><span data-ttu-id="41829-103">範例 Resource-Definition 檔案</span><span class="sxs-lookup"><span data-stu-id="41829-103">Sample Resource-Definition File</span></span>

<span data-ttu-id="41829-104">下列範例顯示的腳本檔案定義了應用程式命名圖形的資源：</span><span class="sxs-lookup"><span data-stu-id="41829-104">The following example shows a script file that defines the resources for an application named Shapes:</span></span>

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

<span data-ttu-id="41829-105">[**Cursor**](cursor-resource.md)語句會為應用程式的資料指標資源 ShapesCursor 命名，並指定資料指標檔案圖形。[下一]，包含該資料指標的影像。</span><span class="sxs-lookup"><span data-stu-id="41829-105">The [**CURSOR**](cursor-resource.md) statement names the application's cursor resource ShapesCursor and specifies the cursor file SHAPES.CUR, which contains the image for that cursor.</span></span>

<span data-ttu-id="41829-106">[**Icon**](icon-resource.md)語句會為應用程式的圖示資源 ShapesIcon 命名，並指定圖示檔圖形。.ICO，其中包含該圖示的影像。</span><span class="sxs-lookup"><span data-stu-id="41829-106">The [**ICON**](icon-resource.md) statement names the application's icon resource ShapesIcon and specifies the icon file SHAPES.ICO, which contains the image for that icon.</span></span>

<span data-ttu-id="41829-107">[**Menu**](menu-resource.md)語句會定義名為 **ShapesMenu** 的應用程式功能表，這個快顯功能表具有五個功能表項目。</span><span class="sxs-lookup"><span data-stu-id="41829-107">The [**MENU**](menu-resource.md) statement defines an application menu named **ShapesMenu**, a pop-up menu with five menu items.</span></span>

<span data-ttu-id="41829-108">功能表定義的主體（以大括弧括住），或 **開頭** 和 **結尾** 關鍵字會指定每個功能表項目，以及當使用者選取該專案時所傳回的功能表識別碼。</span><span class="sxs-lookup"><span data-stu-id="41829-108">The body of the menu definition, enclosed by the curly braces, or the **BEGIN** and **END** keywords, specifies each menu item and the menu identifier that is returned when the user selects that item.</span></span> <span data-ttu-id="41829-109">例如，當使用者選取功能表識別碼識別碼時，功能表上的第一個專案會 **清除** \_ 。</span><span class="sxs-lookup"><span data-stu-id="41829-109">For example, the first item on the menu, **Clear**, returns the menu identifier ID\_CLEAR when the user selects it.</span></span> <span data-ttu-id="41829-110">功能表識別碼會定義在應用程式標頭檔中，即 .H。</span><span class="sxs-lookup"><span data-stu-id="41829-110">The menu identifiers are defined in the application header file, SHAPES.H.</span></span>

 

 




