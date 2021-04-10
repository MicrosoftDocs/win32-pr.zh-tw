---
title: 主題檔案格式
description: 本檔討論主題 ( 的格式。主題) 檔。 主題檔案是一個 .ini 文字檔，可分為區段，以指定顯示在 Windows 桌面上的視覺元素。 區段名稱會以方括弧括住 ( \\ ) 在 .ini 檔案中。
ms.assetid: 0b7b0ff7-f55a-4215-a2fd-6c3ea117d6e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b61ba97172fc5aaddb912183130941337a149536
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "103842852"
---
# <a name="theme-file-format"></a><span data-ttu-id="9cff9-105">主題檔案格式</span><span class="sxs-lookup"><span data-stu-id="9cff9-105">Theme File Format</span></span>

<span data-ttu-id="9cff9-106">本檔討論主題 ( 的格式。主題) 檔。</span><span class="sxs-lookup"><span data-stu-id="9cff9-106">This document discusses the format of Theme (.theme) files.</span></span> <span data-ttu-id="9cff9-107">主題檔案是一個 .ini 文字檔，可分為區段，以指定顯示在 Windows 桌面上的視覺元素。</span><span class="sxs-lookup"><span data-stu-id="9cff9-107">A .theme file is a .ini text file that is divided into sections, which specify visual elements that appear on a Windows desktop.</span></span> <span data-ttu-id="9cff9-108">區段名稱會以方括弧括住 \[ \] ， (.Ini 檔案中的) 。</span><span class="sxs-lookup"><span data-stu-id="9cff9-108">Section names are wrapped in brackets (\[\]) in the .ini file.</span></span>

<span data-ttu-id="9cff9-109">Windows 7 引進了新的檔案格式 themepack，可協助使用者共用主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-109">A new file format, .themepack, was introduced with Windows 7 to help users share themes.</span></span> <span data-ttu-id="9cff9-110">您只能在 Windows 7 Home Premium 或更高版本的個人化主控台中選取主題，或只在安裝桌面元件時，在 Windows Server 2008 R2 上選取主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-110">Themes can be selected in the Personalization Control Panel only in Windows 7 Home Premium or higher, or only on Windows Server 2008 R2 when the Desktop component is installed.</span></span>

<span data-ttu-id="9cff9-111">本文將討論下列主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-111">The following topics are discussed in this article.</span></span>

-   [<span data-ttu-id="9cff9-112">建立主題檔案</span><span class="sxs-lookup"><span data-stu-id="9cff9-112">Creating a Theme File</span></span>](#creating-a-theme-file)
-   [<span data-ttu-id="9cff9-113">主題檔案的描述</span><span class="sxs-lookup"><span data-stu-id="9cff9-113">Description of a Theme File</span></span>](#description-of-a-theme-file)
    -   <span data-ttu-id="9cff9-114">[\[主題 \] 區段](#theme-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-114">[\[Theme\] Section](#theme-section)</span></span>
    -   <span data-ttu-id="9cff9-115">[\[主控台 \\ 色彩 \] 區段](#control-panelcolors-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-115">[\[Control Panel\\Colors\] Section](#control-panelcolors-section)</span></span>
    -   <span data-ttu-id="9cff9-116">[\[主控台資料 \\ 指標 \] 區段](#control-panelcursors-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-116">[\[Control Panel\\Cursors\] Section](#control-panelcursors-section)</span></span>
    -   <span data-ttu-id="9cff9-117">[\[主控台 \\ Desktop \] 區段](#control-paneldesktop-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-117">[\[Control Panel\\Desktop\] Section](#control-paneldesktop-section)</span></span>
    -   <span data-ttu-id="9cff9-118">[\[投影片 \] 區段](#slideshow-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-118">[\[Slideshow\] Section](#slideshow-section)</span></span>
    -   <span data-ttu-id="9cff9-119">[\[計量 \] 區段](#metrics-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-119">[\[Metrics\] Section](#metrics-section)</span></span>
    -   <span data-ttu-id="9cff9-120">[\[視覺化樣式 \] 區段](#visual-styles-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-120">[\[Visual Styles\] Section](#visual-styles-section)</span></span>
    -   <span data-ttu-id="9cff9-121">[\[聲音 \] 和 \[ AppEvents \] 區段 (音效) ](#sounds-and-appevents-sections-sounds)</span><span class="sxs-lookup"><span data-stu-id="9cff9-121">[\[Sounds\] and \[AppEvents\] Sections (Sounds)](#sounds-and-appevents-sections-sounds)</span></span>
    -   <span data-ttu-id="9cff9-122">[\[開機 \] 區段](#boot-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-122">[\[Boot\] Section](#boot-section)</span></span>
    -   <span data-ttu-id="9cff9-123">[\[MasterThemeSelector \] 區段](#masterthemeselector-section)</span><span class="sxs-lookup"><span data-stu-id="9cff9-123">[\[MasterThemeSelector\] Section](#masterthemeselector-section)</span></span>
-   [<span data-ttu-id="9cff9-124">主題檔案的範例</span><span class="sxs-lookup"><span data-stu-id="9cff9-124">Example of a Theme File</span></span>](#example-of-a-theme-file)
-   [<span data-ttu-id="9cff9-125">安裝主題檔案</span><span class="sxs-lookup"><span data-stu-id="9cff9-125">Installing Theme Files</span></span>](#installing-theme-files)
-   [<span data-ttu-id="9cff9-126">主題套件</span><span class="sxs-lookup"><span data-stu-id="9cff9-126">Theme Packs</span></span>](#theme-packs)
-   [<span data-ttu-id="9cff9-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cff9-127">Related topics</span></span>](#related-topics)

## <a name="creating-a-theme-file"></a><span data-ttu-id="9cff9-128">建立主題檔案</span><span class="sxs-lookup"><span data-stu-id="9cff9-128">Creating a Theme File</span></span>

<span data-ttu-id="9cff9-129">主題檔案可讓您變更某些桌面元素的外觀。</span><span class="sxs-lookup"><span data-stu-id="9cff9-129">A .theme file enables you to change the appearance of certain desktop elements.</span></span> <span data-ttu-id="9cff9-130">您可以透過兩種方式來建立或修改主題檔案：</span><span class="sxs-lookup"><span data-stu-id="9cff9-130">You can create or modify a .theme file in two ways:</span></span>

-   <span data-ttu-id="9cff9-131">修改主控台中的個人化或顯示設定，並將設定儲存為主題檔案。</span><span class="sxs-lookup"><span data-stu-id="9cff9-131">Modify personalization or display settings in Control Panel and save the settings as a .theme file.</span></span> <span data-ttu-id="9cff9-132">如需相關指示，請參閱 Windows 說明。</span><span class="sxs-lookup"><span data-stu-id="9cff9-132">See your Windows Help for instructions.</span></span>
-   <span data-ttu-id="9cff9-133">手動建立一個主題檔，以進一步控制您主題的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9cff9-133">Create a .theme file manually for a greater level of control over the details of your theme.</span></span>

<span data-ttu-id="9cff9-134">若要讓您的主題可供其他使用者使用，您必須提供您的主題檔案，以及背景圖片、螢幕保護裝置和圖示檔案。</span><span class="sxs-lookup"><span data-stu-id="9cff9-134">To make your theme available to other users, you must supply your .theme file, as well as the background picture, screen saver, and icons files.</span></span> <span data-ttu-id="9cff9-135">您可以使用 [主題套件](#theme-packs)來完成此動作。</span><span class="sxs-lookup"><span data-stu-id="9cff9-135">You can do this with a [theme pack](#theme-packs).</span></span>

## <a name="description-of-a-theme-file"></a><span data-ttu-id="9cff9-136">主題檔案的描述</span><span class="sxs-lookup"><span data-stu-id="9cff9-136">Description of a Theme File</span></span>

<span data-ttu-id="9cff9-137">主題檔案有數個必要和選用的區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-137">Theme files have a number of required and optional sections.</span></span> <span data-ttu-id="9cff9-138">以下說明主題檔案的區段，並提供如何針對不同的元素指定變更的範例。</span><span class="sxs-lookup"><span data-stu-id="9cff9-138">The following describe the sections of .theme files and provide examples of how to specify changes for the different elements.</span></span>

### <a name="theme-section"></a><span data-ttu-id="9cff9-139">\[主題 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-139">\[Theme\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-140">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-140">This section is optional.</span></span> <span data-ttu-id="9cff9-141">如果您未在您的主題檔案中包含此區段，系統會使用預設設定。</span><span class="sxs-lookup"><span data-stu-id="9cff9-141">If you do not include this section in your .theme file, the system uses default settings.</span></span>

 

<span data-ttu-id="9cff9-142">[ \[ 主題] \] 區段會識別自訂主題的名稱，並指定您主題的品牌標誌和桌面圖示。</span><span class="sxs-lookup"><span data-stu-id="9cff9-142">The \[Theme\] section identifies the name of your custom theme and specifies your theme's brand logo and desktop icons.</span></span>

<span data-ttu-id="9cff9-143">主題區段的第一個 \[ 部分 \] 包含下列兩個元素：</span><span class="sxs-lookup"><span data-stu-id="9cff9-143">The first part of the \[Theme\] section contains the following two elements:</span></span>



| <span data-ttu-id="9cff9-144">元素</span><span class="sxs-lookup"><span data-stu-id="9cff9-144">Element</span></span>                                                                                                                    | <span data-ttu-id="9cff9-145">描述</span><span class="sxs-lookup"><span data-stu-id="9cff9-145">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cff9-146">DisplayName = 名稱</span><span class="sxs-lookup"><span data-stu-id="9cff9-146">DisplayName=name</span></span><br/> <span data-ttu-id="9cff9-147">或</span><span class="sxs-lookup"><span data-stu-id="9cff9-147">or</span></span><br/> <span data-ttu-id="9cff9-148">DisplayName = @module 、-stringid 指定</span><span class="sxs-lookup"><span data-stu-id="9cff9-148">DisplayName=@module,-stringId</span></span><br/> <span data-ttu-id="9cff9-149">範例： DisplayName = @themeui.dll 、-2013</span><span class="sxs-lookup"><span data-stu-id="9cff9-149">example: DisplayName=@themeui.dll,-2013</span></span> | <span data-ttu-id="9cff9-150">DisplayName 是將會顯示在個人化主控台中的主題名稱。</span><span class="sxs-lookup"><span data-stu-id="9cff9-150">DisplayName is the theme name that will show up in the Personalization Control Panel.</span></span> <span data-ttu-id="9cff9-151">它可以是字串或當地語系化名稱的參考。</span><span class="sxs-lookup"><span data-stu-id="9cff9-151">It can be a string or a reference to a localized name.</span></span><br/> <span data-ttu-id="9cff9-152">此為選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="9cff9-152">This field is optional.</span></span> <span data-ttu-id="9cff9-153">如果遺失，則會使用主題檔案名作為主題名稱。</span><span class="sxs-lookup"><span data-stu-id="9cff9-153">If it is missing, the theme filename is used as the theme name.</span></span><br/>                                                                                                                                                                                                                                         |
| <span data-ttu-id="9cff9-154">BrandImage = 影像的路徑</span><span class="sxs-lookup"><span data-stu-id="9cff9-154">BrandImage=path to image</span></span><br/> <span data-ttu-id="9cff9-155">範例： BrandImage = c： \\ Fabrikam \\brand.png</span><span class="sxs-lookup"><span data-stu-id="9cff9-155">example: BrandImage=c:\\Fabrikam\\brand.png</span></span><br/>                                 | <span data-ttu-id="9cff9-156">**Windows 7 和更新版本** BrandImage 會指定在個人化主控台的主題預覽中所併入之品牌化圖形檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9cff9-156">**Windows 7 and later** BrandImage specifies the path to a branded graphic file that is incorporated in the theme preview in the Personalization Control Panel.</span></span><br/> <span data-ttu-id="9cff9-157">圖示圖形必須是 PNG 檔。</span><span class="sxs-lookup"><span data-stu-id="9cff9-157">The icon graphic must be a PNG file.</span></span> <span data-ttu-id="9cff9-158">圖形會調整為80x240 圖元，因此建議您提供該大小的影像。</span><span class="sxs-lookup"><span data-stu-id="9cff9-158">The graphic is scaled to 80x240 pixels, so it is recommended that you provide an image of that size.</span></span> <span data-ttu-id="9cff9-159">主題資源庫會遵循您品牌圖示的透明區域。</span><span class="sxs-lookup"><span data-stu-id="9cff9-159">The Theme gallery respects the transparent regions of your brand icon.</span></span><br/> <span data-ttu-id="9cff9-160">此為選擇性欄位。</span><span class="sxs-lookup"><span data-stu-id="9cff9-160">This field is optional.</span></span> <span data-ttu-id="9cff9-161">如果遺失，則不會顯示任何標誌作為主題圖示。</span><span class="sxs-lookup"><span data-stu-id="9cff9-161">If it is missing, no logo is displayed as the theme icon.</span></span><br/> |



 

<span data-ttu-id="9cff9-162">[主題] 區段的其餘 \[ \] 部分會指定桌面功能的自訂圖示，例如 [電腦]、[我的檔]、[網路] 和 [資源回收筒。</span><span class="sxs-lookup"><span data-stu-id="9cff9-162">The rest of the \[Theme\] section specifies custom icons for desktop features like Computer, My Documents, Network, and Recycle Bin.</span></span> <span data-ttu-id="9cff9-163">如果您未指定自訂桌面圖示，桌面會顯示系統預設桌面圖示。</span><span class="sxs-lookup"><span data-stu-id="9cff9-163">If you do not specify custom desktop icons, the desktop displays the system default desktop icons.</span></span>

<span data-ttu-id="9cff9-164">以下是主題檔案如何設定 **電腦** 圖示的兩個範例。</span><span class="sxs-lookup"><span data-stu-id="9cff9-164">The following are two examples of how a .theme file sets the **Computer** icon.</span></span>


```
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\Computer.ico
```




```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%ProgramFiles%\Fabrikam\MyApp.exe,0
```



<span data-ttu-id="9cff9-165">以下是 Windows 7 中預設桌面圖示的值。</span><span class="sxs-lookup"><span data-stu-id="9cff9-165">The following are values for the default desktop icons in Windows 7.</span></span>


```
; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55
```



### <a name="control-panelcolors-section"></a><span data-ttu-id="9cff9-166">\[主控台 \\ 色彩 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-166">\[Control Panel\\Colors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-167">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-167">This section is optional.</span></span> <span data-ttu-id="9cff9-168">如果您未在您的主題檔案中包含此區段，系統會使用預設設定。</span><span class="sxs-lookup"><span data-stu-id="9cff9-168">If you do not include this section in your .theme file, the system uses default settings.</span></span> <span data-ttu-id="9cff9-169">如果您的主題使用 Aero 視覺化樣式，您應該避免覆寫這個區段中的預設值。</span><span class="sxs-lookup"><span data-stu-id="9cff9-169">If your theme uses the Aero visual style, you should avoid overriding the default values in this section.</span></span>

 

<span data-ttu-id="9cff9-170">您可以自訂元素的色彩，例如捲軸、文字和按鈕。</span><span class="sxs-lookup"><span data-stu-id="9cff9-170">The color of elements, such as scroll bars, text, and buttons, are customizable.</span></span> <span data-ttu-id="9cff9-171">這個主題檔會指定要針對這些元素變更的 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="9cff9-171">The .theme file specifies the RGB values to change for these elements.</span></span> <span data-ttu-id="9cff9-172">這些值會覆寫視覺化樣式的預設值，而且當您的主題是以 Windows 傳統、Windows 7 Basic 或高對比主題為基礎時，就會使用這些值。</span><span class="sxs-lookup"><span data-stu-id="9cff9-172">The values override the default values of the visual style and are used when your theme is based on Windows Classic, Windows 7 Basic, or High Contrast themes.</span></span>

<span data-ttu-id="9cff9-173">以下是如何設定色彩的範例。</span><span class="sxs-lookup"><span data-stu-id="9cff9-173">Following is an example of how colors are set.</span></span>


```
[Control Panel\Colors]
ActiveTitle=10 36 106
Background=166 202 240
Hilight=10 36 106
HilightText=255 255 255
TitleText=255 255 255
Window=255 255 255
WindowText=0 0 0
Scrollbar=212 208 200
InactiveTitle=128 128 128
Menu=212 208 200
WindowFrame=0 0 0
MenuText=0 0 0
ActiveBorder=212 208 200
InactiveBorder=212 208 200
AppWorkspace=128 128 128
ButtonFace=212 208 200
ButtonShadow=128 128 128
GrayText=128 128 128
ButtonText=0 0 0
InactiveTitleText=212 208 200
ButtonHilight=255 255 255
ButtonDkShadow=64 64 64
ButtonLight=212 208 200
InfoText=0 0 0
InfoWindow=255 255 225
GradientActiveTitle=166 202 240
GradientInactiveTitle=192 192 192
```



### <a name="control-panelcursors-section"></a><span data-ttu-id="9cff9-174">\[主控台資料 \\ 指標 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-174">\[Control Panel\\Cursors\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-175">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-175">This section is optional.</span></span> <span data-ttu-id="9cff9-176">如果您未在您的主題檔案中包含此區段，系統會使用預設資料指標。</span><span class="sxs-lookup"><span data-stu-id="9cff9-176">If you do not include this section in your .theme file, the system uses default cursors.</span></span>

 

<span data-ttu-id="9cff9-177">主題也可以變更資料指標的外觀。</span><span class="sxs-lookup"><span data-stu-id="9cff9-177">A theme can also change the appearance of cursors.</span></span> <span data-ttu-id="9cff9-178">若要這樣做，您可以建立檔案來取代預設的 Windows 資料指標。</span><span class="sxs-lookup"><span data-stu-id="9cff9-178">To do so, you create .cur files to replace the default Windows cursors.</span></span> <span data-ttu-id="9cff9-179">下列範例是來自訂稱為 *體育* 主題之資料指標的主題檔案。</span><span class="sxs-lookup"><span data-stu-id="9cff9-179">The following example is from a .theme file that defines the cursors for a theme called *Sports*.</span></span>


```
[Control Panel\Cursors]
Arrow=%SystemRoot%\sports_arrow.cur
Help=%SystemRoot%\sports_help.cur
AppStarting=%SystemRoot%\sports_wait.ani
Wait=%SystemRoot%\sports_busy.ani
NWPen=%SystemRoot%\sports_pen.cur
No=%SystemRoot%\sports_no.cur
SizeNS=%SystemRoot%\sports_size_ns.cur
SizeWE=%SystemRoot%\sports_size_we.cur
Crosshair=%SystemRoot%\sports_cross.cur
IBeam=%SystemRoot%\sports_beam.cur
SizeNWSE=%SystemRoot%\sports_size_nwse.cur
SizeNESW=%SystemRoot%\sports_size_nesw.cur
SizeAll=%SystemRoot%\sports_move.cur
UpArrow=%SystemRoot%\sports_up.cur
DefaultValue=Windows default
```



### <a name="control-paneldesktop-section"></a><span data-ttu-id="9cff9-180">\[主控台 \\ Desktop \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-180">\[Control Panel\\Desktop\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-181">此為必要區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-181">This section is required.</span></span> <span data-ttu-id="9cff9-182">如果您未在您的主題檔案中包含此區段，系統會忽略您的主題，而不會在主控台中顯示主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-182">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="9cff9-183">您可以建立自訂桌面背景，並指定影像檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="9cff9-183">You can create a custom desktop background and specify a path to the image file.</span></span> <span data-ttu-id="9cff9-184">下列範例顯示如何修改桌面外觀。</span><span class="sxs-lookup"><span data-stu-id="9cff9-184">The following example shows how to modify the desktop appearance.</span></span>


```
[Control Panel\Desktop]
Wallpaper=%WinDir%\web\wallpaper\Windows\img0.jpg
; The path to the wallpaper picture can point to a 
; .bmp, .gif, .jpg, .png, or .tif file.

TileWallpaper=0
; 0: The wallpaper picture should not be tiled 
; 1: The wallpaper picture should be tiled 

WallpaperStyle=2
; 0:  The image is centered if TileWallpaper=0 or tiled if TileWallpaper=1
; 2:  The image is stretched to fill the screen
; 6:  The image is resized to fit the screen while maintaining the aspect 
      ratio. (Windows 7 and later)
; 10: The image is resized and cropped to fill the screen while maintaining 
      the aspect ratio. (Windows 7 and later)
```



### <a name="slideshow-section"></a><span data-ttu-id="9cff9-185">\[投影片 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-185">\[Slideshow\] Section</span></span>

<span data-ttu-id="9cff9-186">**Windows 7 和更新版本。**</span><span class="sxs-lookup"><span data-stu-id="9cff9-186">**Windows 7 and later.**</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-187">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-187">This section is optional.</span></span> <span data-ttu-id="9cff9-188">如果您未在您的主題檔案中包含此區段，系統會使用 \[ 主控台 desktop 區段中指定的桌面背景 \\ 影像 \] 。</span><span class="sxs-lookup"><span data-stu-id="9cff9-188">If you do not include this section in your .theme file, the system uses the desktop background image specified in the \[Control Panel\\Desktop\] section.</span></span> <span data-ttu-id="9cff9-189">如果您包含此區段，您必須在這裡指定投影片放映設定。</span><span class="sxs-lookup"><span data-stu-id="9cff9-189">If you include this section, you must specify slide show settings here.</span></span>

 

<span data-ttu-id="9cff9-190">您主題的背景可以是一張投影片，其中的影像儲存在本機或 RSS 摘要所提供的影像。</span><span class="sxs-lookup"><span data-stu-id="9cff9-190">Your theme's background can be a slide show either of images stored locally or of images served by an RSS feed.</span></span> <span data-ttu-id="9cff9-191">檔案的 [投影片] \[ \] 區段包含下列屬性：</span><span class="sxs-lookup"><span data-stu-id="9cff9-191">The \[Slideshow\] section of the file contains the following attributes:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9cff9-192">屬性</span><span class="sxs-lookup"><span data-stu-id="9cff9-192">Attribute</span></span></th>
<th><span data-ttu-id="9cff9-193">描述</span><span class="sxs-lookup"><span data-stu-id="9cff9-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cff9-194">Interval = 毫秒數</span><span class="sxs-lookup"><span data-stu-id="9cff9-194">Interval=number of milliseconds</span></span></td>
<td><span data-ttu-id="9cff9-195">必要。</span><span class="sxs-lookup"><span data-stu-id="9cff9-195">Required.</span></span> <span data-ttu-id="9cff9-196">間隔是決定背景變更頻率的數位。</span><span class="sxs-lookup"><span data-stu-id="9cff9-196">Interval is a number that determines how often the background changes.</span></span> <span data-ttu-id="9cff9-197">它是以毫秒為單位來測量。</span><span class="sxs-lookup"><span data-stu-id="9cff9-197">It is measured in milliseconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cff9-198">隨機 = 0 或1</span><span class="sxs-lookup"><span data-stu-id="9cff9-198">Shuffle=0 or 1</span></span></td>
<td><span data-ttu-id="9cff9-199">必要。</span><span class="sxs-lookup"><span data-stu-id="9cff9-199">Required.</span></span> <span data-ttu-id="9cff9-200">隨機識別是否為背景洗牌。</span><span class="sxs-lookup"><span data-stu-id="9cff9-200">Shuffle identifies whether the background shuffles.</span></span><br/> <span data-ttu-id="9cff9-201">0 = 停用</span><span class="sxs-lookup"><span data-stu-id="9cff9-201">0 = Disabled</span></span><br/> <span data-ttu-id="9cff9-202">1 = 啟用</span><span class="sxs-lookup"><span data-stu-id="9cff9-202">1 = Enabled</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cff9-203">Rss 摘要 = RSS 摘要的 URL</span><span class="sxs-lookup"><span data-stu-id="9cff9-203">RSSFeed=URL to RSS feed</span></span></td>
<td><span data-ttu-id="9cff9-204">如果未指定 ImagesRootPath，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="9cff9-204">Required if ImagesRootPath is not specified.</span></span> <span data-ttu-id="9cff9-205">Rss 摘要指定要作為背景投影片放映使用的 RSS 摘要。</span><span class="sxs-lookup"><span data-stu-id="9cff9-205">RSSFeed specifies an RSS feed to use as the background slide show.</span></span> <span data-ttu-id="9cff9-206">若要讓摘要能夠運作，您必須參考符合 &quot; &quot; <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS 平臺</a>所使用之主機殼標準的高解析度映射。</span><span class="sxs-lookup"><span data-stu-id="9cff9-206">For the feed to work, you need to reference high-resolution images adhering to the &quot;enclosures&quot; standard used by the <a href="/previous-versions/windows/desktop/ms684701(v=vs.85)">Windows RSS Platform</a>.</span></span> <span data-ttu-id="9cff9-207">由於這項限制，必須以手動方式建立包含 RSS 摘要的主題檔案。</span><span class="sxs-lookup"><span data-stu-id="9cff9-207">Because of this limitation, .theme files that include an RSS feed must be created manually.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9cff9-208">您無法同時指定 Rss 摘要和 ImagesRootPath。</span><span class="sxs-lookup"><span data-stu-id="9cff9-208">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cff9-209">ImagesRootPath = 映射資料夾的路徑</span><span class="sxs-lookup"><span data-stu-id="9cff9-209">ImagesRootPath=path to image folder</span></span></td>
<td><span data-ttu-id="9cff9-210">如果未指定 Rss 摘要，則為必要項。</span><span class="sxs-lookup"><span data-stu-id="9cff9-210">Required if RSSFeed is not specified.</span></span> <span data-ttu-id="9cff9-211">ImagesRootPath 指定一組您想要用來做為背景投影片放映的影像路徑。</span><span class="sxs-lookup"><span data-stu-id="9cff9-211">ImagesRootPath specifies a path to a set of images you want to use as the background slide show.</span></span> <span data-ttu-id="9cff9-212">子資料夾中的影像不包含在投影片放映中。</span><span class="sxs-lookup"><span data-stu-id="9cff9-212">Images in subfolders are not included in the slide show.</span></span><br/> <span data-ttu-id="9cff9-213">ImagesRootPath 支援路徑中的環境變數替代。</span><span class="sxs-lookup"><span data-stu-id="9cff9-213">ImagesRootPath supports Environment Variable substitutions in the path.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="9cff9-214">您無法同時指定 Rss 摘要和 ImagesRootPath。</span><span class="sxs-lookup"><span data-stu-id="9cff9-214">You cannot specify both an RSSFeed and ImagesRootPath.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cff9-215">專案<em>N</em>路徑 = 路徑 (s) 至特定映射 (s) </span><span class="sxs-lookup"><span data-stu-id="9cff9-215">Item<em>N</em>Path=path(s) to specific image(s)</span></span></td>
<td><span data-ttu-id="9cff9-216">與 ImagesRootPath 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="9cff9-216">For use with ImagesRootPath.</span></span> <br/> <span data-ttu-id="9cff9-217">專案<em>N</em>路徑指定特定影像的路徑，讓您可以將投影片放映限制為特定影像，而不是資料夾中的所有影像。</span><span class="sxs-lookup"><span data-stu-id="9cff9-217">Item<em>N</em>Path specifies paths to specific images, so that you can limit the slide show to particular images instead of all images in a folder.</span></span> <span data-ttu-id="9cff9-218">如果未指定路徑，則會在投影片放映中使用 ImagesRootPath 路徑中的所有影像，包括建立和安裝主題之後加入的影像。</span><span class="sxs-lookup"><span data-stu-id="9cff9-218">If no paths are specified, all images in the ImagesRootPath path are used in the slide show, including images added after creating and installing the theme.</span></span><br/> <span data-ttu-id="9cff9-219">專案<em>N</em>路徑支援路徑中的環境變數替代。</span><span class="sxs-lookup"><span data-stu-id="9cff9-219">Item<em>N</em>Path supports Environment Variable substitutions in the path.</span></span> <span data-ttu-id="9cff9-220"><em>N</em> 為0、1、2等等。</span><span class="sxs-lookup"><span data-stu-id="9cff9-220"><em>N</em> is 0, 1, 2, and so on.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9cff9-221">下列範例示範如何指定將投影片放映的投影片放映，以包含一組儲存在本機的影像。</span><span class="sxs-lookup"><span data-stu-id="9cff9-221">The following examples show how a .theme file specifies the slide show to include a set of images stored locally.</span></span>


```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%SystemRoot%\Web\Wallpaper
```




```
[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg
```



<span data-ttu-id="9cff9-222">下列範例是主題檔案的範本，該檔案會使用 RSS 摘要中的影像來建立桌面背景投影片放映。</span><span class="sxs-lookup"><span data-stu-id="9cff9-222">The following example is a template for a .theme file that creates a desktop background slide show using images from an RSS feed.</span></span> <span data-ttu-id="9cff9-223">遵循下列步驟來自訂範本：</span><span class="sxs-lookup"><span data-stu-id="9cff9-223">Follow these steps to customize the template:</span></span>

1.  <span data-ttu-id="9cff9-224">複製下列範例，並將它貼到文字編輯器中。</span><span class="sxs-lookup"><span data-stu-id="9cff9-224">Copy the following example and paste it into a text editor.</span></span>
2.  <span data-ttu-id="9cff9-225">將 {themename} 取代為您要在個人化主控台主題圖庫中顯示的名稱。</span><span class="sxs-lookup"><span data-stu-id="9cff9-225">Replace {themename} with the name you want to appear in the Personalization Control Panel themes gallery.</span></span>
3.  <span data-ttu-id="9cff9-226">以相容 RSS 摘要的完整路徑取代 {rssfeedurl}。</span><span class="sxs-lookup"><span data-stu-id="9cff9-226">Replace {rssfeedurl} with the full path to a compatible RSS feed.</span></span>
4.  <span data-ttu-id="9cff9-227">將變更儲存為副檔名為 ". 主題" 的檔案。</span><span class="sxs-lookup"><span data-stu-id="9cff9-227">Save the changes as a file with the ".theme" extension.</span></span>


```
[Theme]
DisplayName={themename}

[Slideshow]
Interval=1800000
Shuffle=1
RssFeed={rssfeedurl}

[Control Panel\Desktop]
TileWallpaper=0
WallpaperStyle=10
Pattern=

[Control Panel\Cursors]
AppStarting=%SystemRoot%\cursors\aero_working.ani
Arrow=%SystemRoot%\cursors\aero_arrow.cur
Crosshair=
Hand=%SystemRoot%\cursors\aero_link.cur
Help=%SystemRoot%\cursors\aero_helpsel.cur
IBeam=
No=%SystemRoot%\cursors\aero_unavail.cur
NWPen=%SystemRoot%\cursors\aero_pen.cur
SizeAll=%SystemRoot%\cursors\aero_move.cur
SizeNESW=%SystemRoot%\cursors\aero_nesw.cur
SizeNS=%SystemRoot%\cursors\aero_ns.cur
SizeNWSE=%SystemRoot%\cursors\aero_nwse.cur
SizeWE=%SystemRoot%\cursors\aero_ew.cur
UpArrow=%SystemRoot%\cursors\aero_up.cur
Wait=%SystemRoot%\cursors\aero_busy.ani
DefaultValue=Windows Aero
Link=

[VisualStyles]
Path=%SystemRoot%\resources\themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X6B74B8FC
Transparency=1

[MasterThemeSelector]
MTSM=DABJDKT
```



### <a name="metrics-section"></a><span data-ttu-id="9cff9-228">\[計量 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-228">\[Metrics\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-229">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-229">This section is optional.</span></span> <span data-ttu-id="9cff9-230">如果您未在您的主題檔案中包含此區段，系統會使用預設的視覺化樣式設定。</span><span class="sxs-lookup"><span data-stu-id="9cff9-230">If you do not include this section in your .theme file, the system uses default visual style settings.</span></span>

 

<span data-ttu-id="9cff9-231">您可以在主題檔案中指定系統計量。</span><span class="sxs-lookup"><span data-stu-id="9cff9-231">You can specify system metrics in a .theme file.</span></span> <span data-ttu-id="9cff9-232">系統計量是各種顯示元素的維度，例如視窗框線寬度、圖示高度或捲軸寬度。</span><span class="sxs-lookup"><span data-stu-id="9cff9-232">System metrics are the dimensions of various display elements, such as the window border width, icon height, or scroll bar width.</span></span> <span data-ttu-id="9cff9-233">NonclientMetrics 和 IconMetrics 值是 NONCLIENTMETRICS 和 ICONMETRICS 在 winuser 中定義的二進位結構。</span><span class="sxs-lookup"><span data-stu-id="9cff9-233">The NonclientMetrics and IconMetrics values are binary structures defined by NONCLIENTMETRICS and ICONMETRICS in winuser.h.</span></span> <span data-ttu-id="9cff9-234">以下是如何變更系統計量的範例。</span><span class="sxs-lookup"><span data-stu-id="9cff9-234">Following is an example of how to change system metrics.</span></span>


```
[Control Panel\Desktop\WindowMetrics]

[Metrics]
IconMetrics=76 0 0 0 139 0 0 0 139 0 0 0 1 0 0 0 245
255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0 0 0 0
0 0 0 0 84 97 104 111 109 97 0 119 0 0 7 0 0 0 0 0 216
31 7 0 28 52 1 1 216 31 7 0 176 36 1 1 
NonclientMetrics=84 1 0 0 1 0 0 0 16 0 0 0 16 0 0 0 18
0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
188 2 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 0 0
0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 0 12 0 0 0
15 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 188 2
0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 80 37 11
0 0 0 0 0 140 221 6 0 227 115 247 119 2 40 11 0 7 0 0
0 18 0 0 0 18 0 0 0 245 255 255 255 0 0 0 0 0 0 0 0 0
0 0 0 144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0
0 0 0 0 0 60 222 6 0 50 71 252 119 120 1 7 0 76 73 252
119 8 6 7 0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0
144 1 0 0 0 0 0 0 0 0 0 0 84 97 104 111 109 97 0 119 0
0 7 0 120 1 7 0 120 1 7 0 40 37 11 0 120 1 7 0 120 1 7
0 245 255 255 255 0 0 0 0 0 0 0 0 0 0 0 0 144 1 0 0 0
0 0 0 0 0 0 0 84 97 104 111 109 97 0 0 92 1 0 0 136 4
0 0 40 37 1 1 0 0 7 0 184 221 6 0 46 75 232 119 
```



### <a name="visual-styles-section"></a><span data-ttu-id="9cff9-235">\[視覺化樣式 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-235">\[Visual Styles\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-236">此為必要區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-236">This section is required.</span></span> <span data-ttu-id="9cff9-237">如果您未在您的主題檔案中包含此區段，系統會忽略您的主題，而不會在主控台中顯示主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-237">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="9cff9-238">您可以在 msstyles 檔案中提供有關桌面元素大小和色彩的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="9cff9-238">You can supply specific information concerning the size and color of desktop elements in .msstyles files.</span></span> <span data-ttu-id="9cff9-239">您可以使用 msstyles 檔案來取代主題檔案的 [色彩] 和 [大小] 區段，讓您更詳細地修改桌面元素。</span><span class="sxs-lookup"><span data-stu-id="9cff9-239">The color and size sections of .theme files can be replaced by .msstyles files which enable you to modify desktop elements in more detail.</span></span> <span data-ttu-id="9cff9-240">這些檔案是在主題檔案的視覺化樣式區段中指定。</span><span class="sxs-lookup"><span data-stu-id="9cff9-240">These files are specified in the visual styles section of a .theme file.</span></span> <span data-ttu-id="9cff9-241">以下是視覺化樣式區段的範例。</span><span class="sxs-lookup"><span data-stu-id="9cff9-241">Following is an example of a visual styles section.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
```



<span data-ttu-id="9cff9-242">將 Path 元素加入至 msstyles 檔案是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="9cff9-242">Adding a Path element to a .msstyles file is optional.</span></span> <span data-ttu-id="9cff9-243">如果您提供路徑，您應該從主題檔案中移除 [度量] 和 [色彩] 區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-243">If you supply a path, you should remove the metrics and color sections from the .theme file.</span></span> <span data-ttu-id="9cff9-244">移除這些區段時，主題的色彩、字型和大小會來自 msstyles 檔案，並符合 msstyles 作者的意圖。</span><span class="sxs-lookup"><span data-stu-id="9cff9-244">When these sections are removed, the colors, fonts, and sizes for a theme come from the .msstyles file and match the .msstyles author's intent.</span></span> <span data-ttu-id="9cff9-245">無法移除 [度量] 和 [色彩] 區段可能會導致 Windows 或應用程式有繪製問題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-245">Failing to remove the metric and color sections can cause Windows or applications to have drawing problems.</span></span>

<span data-ttu-id="9cff9-246">**Windows Vista/windows 7：** 當路徑指向 Aero. msstyles 時，您可以指定所需的半透明色彩，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="9cff9-246">**Windows Vista / Windows 7:** When the path points to Aero.msstyles, you can specify the desired Glass Color, as shown in the following example.</span></span>

<span data-ttu-id="9cff9-247">**Windows 7：** 當路徑指向 Aero. msstyles 時，您也可以指定所需的透明度值，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="9cff9-247">**Windows 7:** When the path points to Aero.msstyles, you can also specify the desired Transparency value, as shown in the following example.</span></span>


```
[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0X7298844C
Transparency=1
```



<span data-ttu-id="9cff9-248">如果 ColorizationColor 和透明度值完全符合系統色彩，個人化主控台會顯示色彩的系統名稱。</span><span class="sxs-lookup"><span data-stu-id="9cff9-248">If the ColorizationColor and Transparency values exactly match a system color, the Personalization Control Panel displays the system name for the color.</span></span> <span data-ttu-id="9cff9-249">否則，色彩會標示為「自訂」。</span><span class="sxs-lookup"><span data-stu-id="9cff9-249">Otherwise, the color is labeled "Custom."</span></span>

<span data-ttu-id="9cff9-250">以下顯示 Windows 7 基本主題的 >visualstyles 一節。</span><span class="sxs-lookup"><span data-stu-id="9cff9-250">The following shows a VisualStyles section for the Windows 7 Basic theme.</span></span>


```
[VisualStyles]
Path=%ResourceDir%\Themes\Aero\Aero.msstyles
Composition=0
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x6B74B8FC
Transparency=1
```



<span data-ttu-id="9cff9-251">以下顯示 Windows 傳統主題的 >visualstyles 一節。</span><span class="sxs-lookup"><span data-stu-id="9cff9-251">The following shows a VisualStyles section for the Windows Classic theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-854
Size=@themeui.dll,-2019
Transparency=0
```



<span data-ttu-id="9cff9-252">以下顯示高對比黑色主題的 >visualstyles 區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-252">The following shows a VisualStyles section for a High Contrast Black theme.</span></span>


```
[VisualStyles]
Path=
ColorStyle=@themeui.dll,-852
Size=@themeui.dll,-2019
Transparency=0
```



### <a name="sounds-and-appevents-sections-sounds"></a><span data-ttu-id="9cff9-253">\[聲音 \] 和 \[ AppEvents \] 區段 (音效) </span><span class="sxs-lookup"><span data-stu-id="9cff9-253">\[Sounds\] and \[AppEvents\] Sections (Sounds)</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-254">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-254">This section is optional.</span></span> <span data-ttu-id="9cff9-255">如果您的主題檔案中未包含此區段，系統會使用預設的音效設定。</span><span class="sxs-lookup"><span data-stu-id="9cff9-255">If you do not include this section in your .theme file, the system uses default sound settings.</span></span>

 

<span data-ttu-id="9cff9-256">使用者可以在主控台中選取 **音效** 圖示，以將聲音與應用程式中發生的事件產生關聯。</span><span class="sxs-lookup"><span data-stu-id="9cff9-256">The user can select the **Sound** icon in Control Panel to associate sounds with events that occur in applications.</span></span> <span data-ttu-id="9cff9-257">例如，當應用程式開啟時，可以播放 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="9cff9-257">For example, a .wav file can play when an application is opened.</span></span> <span data-ttu-id="9cff9-258">主題檔案可以指定 .wav 檔來取代預設的 .wav 檔。</span><span class="sxs-lookup"><span data-stu-id="9cff9-258">A .theme file can specify .wav files to replace the default ones.</span></span> <span data-ttu-id="9cff9-259">下列範例示範如何執行。</span><span class="sxs-lookup"><span data-stu-id="9cff9-259">The following example shows how to do this.</span></span>


```
[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=%WinDir%\media\tada.wav

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=%WinDir%\media\The Microsoft Sound.wav

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav
```



<span data-ttu-id="9cff9-260">**Windows 7 和更新版本：** 您可以指定音效配置名稱，而不是個別列出每個音效。</span><span class="sxs-lookup"><span data-stu-id="9cff9-260">**Windows 7 and later:** A sound scheme name can be specified instead of listing each sound separately.</span></span>


```
[Sounds]
; "Quirky" sound scheme
SchemeName=@%SystemRoot%\System32\mmres.dll,-819
```



<span data-ttu-id="9cff9-261">SchemeName 值會指定音效配置名稱或當地語系化的音效配置名稱（如上述範例所示）。</span><span class="sxs-lookup"><span data-stu-id="9cff9-261">The SchemeName value specifies the sound scheme name or the localized sound scheme name, as shown in the example above.</span></span>

### <a name="boot-section"></a><span data-ttu-id="9cff9-262">\[開機 \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-262">\[Boot\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-263">**螢幕保護裝置在 Windows 10 年度更新版和之後已淘汰。**</span><span class="sxs-lookup"><span data-stu-id="9cff9-263">**Screen Savers are deprecated in the Windows 10 Anniversary Update and beyond.**</span></span>

 

> [!Note]  
> <span data-ttu-id="9cff9-264">此為選擇性區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-264">This section is optional.</span></span> <span data-ttu-id="9cff9-265">如果您未在您的主題檔案中包含此區段，則不會使用任何螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="9cff9-265">If you do not include this section in your .theme file, no screen saver is used.</span></span>

 

<span data-ttu-id="9cff9-266">在 [主題] 檔案中，您可以指定 Windows 要使用的螢幕保護裝置。</span><span class="sxs-lookup"><span data-stu-id="9cff9-266">In the .theme file, you can specify the screen saver for Windows to use.</span></span> <span data-ttu-id="9cff9-267">以下範例說明這點。</span><span class="sxs-lookup"><span data-stu-id="9cff9-267">The following example shows this.</span></span>


```
[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr
```



### <a name="masterthemeselector-section"></a><span data-ttu-id="9cff9-268">\[MasterThemeSelector \] 區段</span><span class="sxs-lookup"><span data-stu-id="9cff9-268">\[MasterThemeSelector\] Section</span></span>

> [!Note]  
> <span data-ttu-id="9cff9-269">此為必要區段。</span><span class="sxs-lookup"><span data-stu-id="9cff9-269">This section is required.</span></span> <span data-ttu-id="9cff9-270">如果您未在您的主題檔案中包含此區段，系統會忽略您的主題，而不會在主控台中顯示主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-270">If you do not include this section in your .theme file, the system ignores your Theme and does not display the Theme in Control Panel.</span></span>

 

<span data-ttu-id="9cff9-271">主題檔案的主要主題選取器區段應該一律包含為指出檔案有效的標記。</span><span class="sxs-lookup"><span data-stu-id="9cff9-271">The master theme selector section of the .theme file should always be included as a tag that indicates the file is valid.</span></span> <span data-ttu-id="9cff9-272">您沒有此參數的值選擇。</span><span class="sxs-lookup"><span data-stu-id="9cff9-272">You do not have a choice of values for this parameter.</span></span> <span data-ttu-id="9cff9-273">如下所示。</span><span class="sxs-lookup"><span data-stu-id="9cff9-273">The following shows this.</span></span>


```
[MasterThemeSelector]
MTSM=DABJDKT
```



## <a name="example-of-a-theme-file"></a><span data-ttu-id="9cff9-274">主題檔案的範例</span><span class="sxs-lookup"><span data-stu-id="9cff9-274">Example of a Theme File</span></span>

<span data-ttu-id="9cff9-275">下列範例顯示完整的主題檔案。</span><span class="sxs-lookup"><span data-stu-id="9cff9-275">The following example shows a complete .theme file.</span></span>


```
[Theme]
DisplayName=My Current Theme
BrandImage=c:\Fabrikam\brand.png

; Computer
[CLSID\{20D04FE0-3AEA-1069-A2D8-08002B30309D}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-109

; Documents
[CLSID\{59031A47-3F72-44A7-89C5-5595FE6B30EE}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\shell32.dll,-235

; Network
[CLSID\{F02C1A0D-BE21-4350-88B0-7367FC96EF3C}\DefaultIcon]
DefaultValue=%SystemRoot%\System32\imageres.dll,-25

; Recycle Bin
[CLSID\{645FF040-5081-101B-9F08-00AA002F954E}\DefaultIcon]
Full=%SystemRoot%\System32\imageres.dll,-54
Empty=%SystemRoot%\System32\imageres.dll,-55

[Control Panel\Cursors]
Arrow=
Help=
AppStarting=
Wait=
NWPen=
No=
SizeNS=
SizeWE=
Crosshair=
IBeam=
SizeNWSE=
SizeNESW=
SizeAll=
UpArrow=
DefaultValue=Windows default

[Control Panel\Desktop]
Wallpaper=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
TileWallpaper=0
WallpaperStyle=2
Pattern=
ScreenSaveActive=0

[AppEvents\Schemes\Apps\.Default\.Default]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\AppGPFault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Maximize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuCommand]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\MenuPopup]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Minimize]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Open]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreDown]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RestoreUp]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\RingIn]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\Ringout]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemAsterisk]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemDefault]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemExclamation]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemExit]
DefaultValue=

[AppEvents\Schemes\Apps\.Default\SystemHand]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemQuestion]
DefaultValue=%WinDir%\media\chord.wav

[AppEvents\Schemes\Apps\.Default\SystemStart]
DefaultValue=

[AppEvents\Schemes\Apps\Explorer\EmptyRecycleBin]
DefaultValue=%WinDir%\media\ding.wav

[AppEvents\Schemes\Apps\.Default\Close]
DefaultValue=

[Slideshow]
Interval=1800000
Shuffle=1
ImagesRootPath=%ProgramFiles%\fabrikam\wallpaper
Item0Path=%ProgramFiles%\fabrikam\wallpaper\ocean.jpg
Item1Path=%ProgramFiles%\fabrikam\wallpaper\mountain.jpg
Item2Path=%ProgramFiles%\fabrikam\wallpaper\river.jpg

[boot]
SCRNSAVE.EXE=%WinDir%\System32\bubbles.scr

[MasterThemeSelector]
MTSM=DABJDKT
ThemeColorBPP=4

[VisualStyles]
Path=%SystemRoot%\resources\Themes\Aero\Aero.msstyles
ColorStyle=NormalColor
Size=NormalSize
ColorizationColor=0x856E3BA1
Transparency=1
```



## <a name="installing-theme-files"></a><span data-ttu-id="9cff9-276">安裝主題檔案</span><span class="sxs-lookup"><span data-stu-id="9cff9-276">Installing Theme Files</span></span>

<span data-ttu-id="9cff9-277">當 Windows 初始化時，作業系統會列舉% WinDir% 資源的第一層子目錄， \\ \\ 以找出可用的主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-277">When Windows is initialized, the operating system enumerates the first-level subdirectories of %WinDir%\\Resources\\ to identify available themes.</span></span> <span data-ttu-id="9cff9-278">系統預設主題檔案位於% WinDir% \\ 資源 \\ 主題。</span><span class="sxs-lookup"><span data-stu-id="9cff9-278">The system default theme files are located in %WinDir%\\Resources\\Themes.</span></span> <span data-ttu-id="9cff9-279">使用者主題檔案儲存在% WinDir% \\ Users \\ <username> \\ AppData \\ Local \\ Microsoft \\ Windows 主題中 \\ 。</span><span class="sxs-lookup"><span data-stu-id="9cff9-279">The user theme files are stored in %WinDir%\\Users\\<username>\\AppData\\Local\\Microsoft\\Windows\\Themes.</span></span>

<span data-ttu-id="9cff9-280">主題檔案具有檔案關聯;因此，主題安裝程式應用程式可以在 ShellExecute 的主題檔案上呼叫 [](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) ，以在指定的主題主控台中開啟 **個人** 化視窗。</span><span class="sxs-lookup"><span data-stu-id="9cff9-280">A .theme file has file associations; therefore, theme installer applications can call [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) on a .theme file to open the **Personalization** window in Control Panel to the specified theme.</span></span>

## <a name="theme-packs"></a><span data-ttu-id="9cff9-281">主題套件</span><span class="sxs-lookup"><span data-stu-id="9cff9-281">Theme Packs</span></span>

<span data-ttu-id="9cff9-282">**Windows 7 和更新版本。**</span><span class="sxs-lookup"><span data-stu-id="9cff9-282">**Windows 7 and later.**</span></span> <span data-ttu-id="9cff9-283">主題套件是一個 .cab 檔案，其中不僅包含主題檔案，還包含在另一部電腦上執行該主題所需的檔案，例如音效檔和影像。</span><span class="sxs-lookup"><span data-stu-id="9cff9-283">A theme pack is a .cab file that contains not only the .theme file but also the files needed to implement the theme on another computer, such as sound files and images.</span></span> <span data-ttu-id="9cff9-284">使用者可以透過個人化主控台建立主題套件。</span><span class="sxs-lookup"><span data-stu-id="9cff9-284">Users can create theme packs through the Personalization Control Panel.</span></span>

<span data-ttu-id="9cff9-285">支援的檔案類型包括下列各項：</span><span class="sxs-lookup"><span data-stu-id="9cff9-285">Supported file types include the following:</span></span>



| <span data-ttu-id="9cff9-286">檔案類型</span><span class="sxs-lookup"><span data-stu-id="9cff9-286">File type</span></span>    | <span data-ttu-id="9cff9-287">分機</span><span class="sxs-lookup"><span data-stu-id="9cff9-287">Extension</span></span>                           |
|--------------|-------------------------------------|
| <span data-ttu-id="9cff9-288">佈景主題</span><span class="sxs-lookup"><span data-stu-id="9cff9-288">Theme</span></span>        | <span data-ttu-id="9cff9-289">.theme</span><span class="sxs-lookup"><span data-stu-id="9cff9-289">.theme</span></span>                              |
| <span data-ttu-id="9cff9-290">Image</span><span class="sxs-lookup"><span data-stu-id="9cff9-290">Image</span></span>        | <span data-ttu-id="9cff9-291">.jpg、jpeg、.bmp、.dib、.tif、.png</span><span class="sxs-lookup"><span data-stu-id="9cff9-291">.jpg, .jpeg, .bmp, .dib, .tif, .png</span></span> |
| <span data-ttu-id="9cff9-292">音效</span><span class="sxs-lookup"><span data-stu-id="9cff9-292">Sound</span></span>        | <span data-ttu-id="9cff9-293">.wav</span><span class="sxs-lookup"><span data-stu-id="9cff9-293">.wav</span></span>                                |
| <span data-ttu-id="9cff9-294">滑鼠游標</span><span class="sxs-lookup"><span data-stu-id="9cff9-294">Mouse cursor</span></span> | <span data-ttu-id="9cff9-295">。</span><span class="sxs-lookup"><span data-stu-id="9cff9-295">.cur, .ani</span></span>                          |
| <span data-ttu-id="9cff9-296">桌面圖示</span><span class="sxs-lookup"><span data-stu-id="9cff9-296">Desktop icon</span></span> | <span data-ttu-id="9cff9-297">.ico</span><span class="sxs-lookup"><span data-stu-id="9cff9-297">.ico</span></span>                                |
| <span data-ttu-id="9cff9-298">品牌標誌</span><span class="sxs-lookup"><span data-stu-id="9cff9-298">Brand logo</span></span>   | <span data-ttu-id="9cff9-299">.png</span><span class="sxs-lookup"><span data-stu-id="9cff9-299">.png</span></span>                                |



 

## <a name="related-topics"></a><span data-ttu-id="9cff9-300">相關主題</span><span class="sxs-lookup"><span data-stu-id="9cff9-300">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cff9-301">視覺化樣式總覽</span><span class="sxs-lookup"><span data-stu-id="9cff9-301">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

