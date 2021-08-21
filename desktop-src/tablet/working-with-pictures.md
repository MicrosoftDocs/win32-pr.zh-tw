---
description: 本主題說明如何使用系統調整圖片。Windows。SizeMode 屬性，以及如何在 Microsoft Visual Studio .net 中顯示圖片。
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: 使用圖片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6e3331d384f30084082e8ef29c5a3a5b44232843bc834a8282bf1786a088d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449174"
---
# <a name="working-with-pictures"></a>使用圖片

本主題說明如何使用系統來調整圖片[Windows。SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1)屬性，以及如何在 Microsoft Visual Studio .net 中顯示圖片。

## <a name="the-sizemode-property"></a>SizeMode 屬性

您可以使用 [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) 屬性指定影像如何容納在控制項中。 SizeMode 屬性可在 Managed 程式庫和 Automation 程式庫中使用。 透過 SizeMode，您可以：

-   調整控制項框線大小以符合影像。
-   延展影像以符合控制項框線。
-   將影像置中在控制項框線內。
-   將影像錨定至控制項的左上角，而不將影像或控制項調整 (如果您沒有調整影像或控制項) 的大小，則可能無法查看某些影像。

## <a name="working-with-pictures-in-visual-studio-net"></a>在 Visual Studio .net 中使用圖片

若要在設計階段顯示 Visual Studio .net 中的影像：

1.  將 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項拖曳到表單上，或按兩下 [工具箱] 中的 [InkPicture] 控制項。
2.  在 [ **屬性** ] 視窗中，選取 [ **影像** ] 屬性，然後按一下省略號按鈕以開啟 [ **開啟** ] 對話方塊。
3.  如果您要尋找特定檔案類型 (例如 .jpg 檔案) ，請在 [ **檔案類型** ] 方塊中選取它。
4.  選取您要顯示的檔案。

若要在設計階段清除圖片：

1.  在 [ **屬性** ] 視窗中，選取 [ **影像** ] 屬性，然後以滑鼠右鍵按一下縮圖影像。
2.  按一下 [重設]。

預設會顯示 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項，但不含任何框線。 您可以使用 [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) 屬性來提供標準或三維框線，以區別 InkPicture 方塊與表單的其餘部分，即使它不包含任何影像。

您可以在執行時間使用 [影像物件的](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) 方法來顯示影像：


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



您也可以包含背景影像與繼承的 [影像](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) 物件的 [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) 屬性;不過，該影像無法調整大小。

 

 
