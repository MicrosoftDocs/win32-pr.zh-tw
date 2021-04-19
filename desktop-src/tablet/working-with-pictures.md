---
description: 本主題說明如何使用 SizeMode 屬性來調整圖片，以及如何在 Microsoft Visual Studio .NET 中顯示圖片。
ms.assetid: 9f4f0f96-68a3-447d-a239-599c9fd3e343
title: 使用圖片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af3a90c0d18253eaf4aea60eafc48bd1c24fcc3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971032"
---
# <a name="working-with-pictures"></a><span data-ttu-id="0758f-103">使用圖片</span><span class="sxs-lookup"><span data-stu-id="0758f-103">Working with Pictures</span></span>

<span data-ttu-id="0758f-104">本主題說明如何使用 [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) 屬性來調整圖片，以及如何在 Microsoft Visual Studio .net 中顯示圖片。</span><span class="sxs-lookup"><span data-stu-id="0758f-104">This topic describes how to adjust pictures using the [System.Windows.Forms.PictureBox.SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property, and how to display pictures in Microsoft Visual Studio .NET.</span></span>

## <a name="the-sizemode-property"></a><span data-ttu-id="0758f-105">SizeMode 屬性</span><span class="sxs-lookup"><span data-stu-id="0758f-105">The SizeMode Property</span></span>

<span data-ttu-id="0758f-106">您可以使用 [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) 屬性指定影像如何容納在控制項中。</span><span class="sxs-lookup"><span data-stu-id="0758f-106">You can specify how an image fits in the control with the [SizeMode](/dotnet/api/system.windows.forms.picturebox.sizemode?view=netcore-3.1) property.</span></span> <span data-ttu-id="0758f-107">SizeMode 屬性可在 Managed 程式庫和 Automation 程式庫中使用。</span><span class="sxs-lookup"><span data-stu-id="0758f-107">The SizeMode property is available in both the Managed Library and in the Automation Library.</span></span> <span data-ttu-id="0758f-108">透過 SizeMode，您可以：</span><span class="sxs-lookup"><span data-stu-id="0758f-108">With SizeMode you can:</span></span>

-   <span data-ttu-id="0758f-109">調整控制項框線大小以符合影像。</span><span class="sxs-lookup"><span data-stu-id="0758f-109">Resize the control borders to fit an image.</span></span>
-   <span data-ttu-id="0758f-110">延展影像以符合控制項框線。</span><span class="sxs-lookup"><span data-stu-id="0758f-110">Stretch an image to fit the control borders.</span></span>
-   <span data-ttu-id="0758f-111">將影像置中在控制項框線內。</span><span class="sxs-lookup"><span data-stu-id="0758f-111">Center an image within the control borders.</span></span>
-   <span data-ttu-id="0758f-112">將影像錨定至控制項的左上角，而不將影像或控制項調整 (如果您沒有調整影像或控制項) 的大小，則可能無法查看某些影像。</span><span class="sxs-lookup"><span data-stu-id="0758f-112">Anchor an image to the upper-left area of the control without resizing the image or control (some of the image may not be viewable if you do not resize the image or control).</span></span>

## <a name="working-with-pictures-in-visual-studio-net"></a><span data-ttu-id="0758f-113">在 Visual Studio .NET 中使用圖片</span><span class="sxs-lookup"><span data-stu-id="0758f-113">Working with Pictures in Visual Studio .NET</span></span>

<span data-ttu-id="0758f-114">若要在設計階段于 Visual Studio .NET 中顯示影像：</span><span class="sxs-lookup"><span data-stu-id="0758f-114">To display an image at design time in Visual Studio .NET:</span></span>

1.  <span data-ttu-id="0758f-115">將 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項拖曳到表單上，或按兩下 [工具箱] 中的 [InkPicture] 控制項。</span><span class="sxs-lookup"><span data-stu-id="0758f-115">Drag an [InkPicture](/previous-versions/aa514604(v=msdn.10)) control on a form, or double-click the InkPicture control in the Toolbox.</span></span>
2.  <span data-ttu-id="0758f-116">在 [ **屬性** ] 視窗中，選取 [ **影像** ] 屬性，然後按一下省略號按鈕以開啟 [ **開啟** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="0758f-116">In the **Properties** window, select the **Image** property, and then click the ellipsis button to open the **Open** dialog box.</span></span>
3.  <span data-ttu-id="0758f-117">如果您要尋找特定檔案類型 (例如 .jpg 檔案) ，請在 [ **檔案類型** ] 方塊中選取它。</span><span class="sxs-lookup"><span data-stu-id="0758f-117">If you are looking for a specific file type (for example, .jpg files), select it in the **Files of type** box.</span></span>
4.  <span data-ttu-id="0758f-118">選取您要顯示的檔案。</span><span class="sxs-lookup"><span data-stu-id="0758f-118">Select the file you want to display.</span></span>

<span data-ttu-id="0758f-119">若要在設計階段清除圖片：</span><span class="sxs-lookup"><span data-stu-id="0758f-119">To clear the picture at design time:</span></span>

1.  <span data-ttu-id="0758f-120">在 [ **屬性** ] 視窗中，選取 [ **影像** ] 屬性，然後以滑鼠右鍵按一下縮圖影像。</span><span class="sxs-lookup"><span data-stu-id="0758f-120">In the **Properties** window, select the **Image** property and right-click the thumbnail image.</span></span>
2.  <span data-ttu-id="0758f-121">按一下 [重設]。</span><span class="sxs-lookup"><span data-stu-id="0758f-121">Click **Reset**.</span></span>

<span data-ttu-id="0758f-122">預設會顯示 [InkPicture](/previous-versions/aa514604(v=msdn.10)) 控制項，但不含任何框線。</span><span class="sxs-lookup"><span data-stu-id="0758f-122">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) control is displayed by default without any borders.</span></span> <span data-ttu-id="0758f-123">您可以使用 [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) 屬性來提供標準或三維框線，以區別 InkPicture 方塊與表單的其餘部分，即使它不包含任何影像。</span><span class="sxs-lookup"><span data-stu-id="0758f-123">You can provide a standard or three-dimensional border using the [BorderStyle](/dotnet/api/system.windows.forms.picturebox.borderstyle?view=netcore-3.1) property to distinguish the InkPicture box from the rest of the form, even if it contains no image.</span></span>

<span data-ttu-id="0758f-124">您可以在執行時間使用 [影像物件的](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) 方法來顯示影像：</span><span class="sxs-lookup"><span data-stu-id="0758f-124">You can display an image at run time with the [System.Drawing.Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [FromFile](/dotnet/api/system.drawing.image.fromfile?view=dotnet-plat-ext-3.1&preserve-view=true) method:</span></span>


```C++
ctlInkPicture.Image = Image.FromFile("c:\myImageFile")
```



<span data-ttu-id="0758f-125">您也可以包含背景影像與繼承的 [影像](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) 物件的 [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) 屬性;不過，該影像無法調整大小。</span><span class="sxs-lookup"><span data-stu-id="0758f-125">You can also include a background image with the inherited [Image](/dotnet/api/system.drawing.image?view=dotnet-plat-ext-3.1&preserve-view=true) object's [BackgroundImage](/dotnet/api/system.windows.forms.control.backgroundimage?view=netcore-3.1) property; however, that image cannot be resized.</span></span>

 

 
