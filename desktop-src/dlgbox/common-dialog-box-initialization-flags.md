---
title: 通用對話方塊初始化旗標
description: 旗標是用來修改通用對話方塊的行為和外觀。
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- 一般對話方塊程式庫，初始化
- 通用對話方塊，初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/19/2020
ms.locfileid: "104463984"
---
# <a name="common-dialog-box-initialization-flags"></a>通用對話方塊初始化旗標

旗標是用來修改通用對話方塊的行為和外觀。 初始化旗標是您在用來建立對話方塊的結構 **旗標** 成員中設定的值。 您可以使用旗標來指定對話方塊中的哪些控制項接收初始值、停用選取的控制項，以及修改使用者可使用控制項設定的值範圍。 您也可以使用旗標來啟用對話方塊的攔截程式和自訂範本。

例如，您可以在 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **旗標** 成員中設定 **CF \_ 效果** 值，以指示 [**字型**] 對話方塊來顯示效果控制項。 這些控制項可讓使用者選擇字型色彩以及刪除線和底線效果。

初始化旗標值對於每個通用對話方塊都是唯一的，而且會詳細說明下列對應的下列結構的 **旗標** 成員：

-   [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [**PAGESETUPDLG**](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [**PRINTDLG**](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [**PRINTDLGEX**](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




