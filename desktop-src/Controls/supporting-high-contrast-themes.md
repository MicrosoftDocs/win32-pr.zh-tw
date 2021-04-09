---
title: 支援高對比主題
description: 本主題比較 Windows 8 對舊版 Windows 的高對比主題的支援，並說明如何在 Windows 8 應用程式中支援高對比主題。
ms.assetid: 6E4F1198-E69C-4C60-B3B0-2702AECAA203
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2068d64b585f302f578296c9e156895c23b9bce9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842763"
---
# <a name="supporting-high-contrast-themes"></a><span data-ttu-id="01c95-103">支援高對比主題</span><span class="sxs-lookup"><span data-stu-id="01c95-103">Supporting High Contrast Themes</span></span>

<span data-ttu-id="01c95-104">本主題比較 Windows 8 對舊版 Windows 的高對比主題的支援，並說明如何在 Windows 8 應用程式中支援高對比主題。</span><span class="sxs-lookup"><span data-stu-id="01c95-104">This topic compares the support for high contrast themes in Windows 8 to that of previous versions of Windows, and explains how to support high contrast themes in a Windows 8 application.</span></span>

<span data-ttu-id="01c95-105">其中包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="01c95-105">It includes the following sections.</span></span>

-   [<span data-ttu-id="01c95-106">高對比主題的支援總覽</span><span class="sxs-lookup"><span data-stu-id="01c95-106">Overview of Support for High Contrast Themes</span></span>](#overview-of-support-for-high-contrast-themes)
-   [<span data-ttu-id="01c95-107">在 Windows 8 和更新版本中支援高對比主題</span><span class="sxs-lookup"><span data-stu-id="01c95-107">Supporting High Contrast Themes in Windows 8 and later</span></span>](#supporting-high-contrast-themes-in-windows-8-and-later)
-   [<span data-ttu-id="01c95-108">將相容性區段新增至您的應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="01c95-108">Adding a Compatibility Section to Your Application Manifest</span></span>](#adding-a-compatibility-section-to-your-application-manifest)
-   [<span data-ttu-id="01c95-109">在舊版 Windows 中偵測高對比</span><span class="sxs-lookup"><span data-stu-id="01c95-109">Detecting High Contrast in Previous Versions of Windows</span></span>](#detecting-high-contrast-in-previous-versions-of-windows)
-   [<span data-ttu-id="01c95-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="01c95-110">Related topics</span></span>](#related-topics)

## <a name="overview-of-support-for-high-contrast-themes"></a><span data-ttu-id="01c95-111">高對比主題的支援總覽</span><span class="sxs-lookup"><span data-stu-id="01c95-111">Overview of Support for High Contrast Themes</span></span>

<span data-ttu-id="01c95-112">Windows 7 及更早版本支援兩個主題模型，包括舊版 Windows 傳統模型和目前的視覺化樣式。</span><span class="sxs-lookup"><span data-stu-id="01c95-112">Windows 7 and earlier support two theming models, including the legacy Windows classic model, and the current visual styles.</span></span> <span data-ttu-id="01c95-113">Windows 傳統模型已透過 Windows 7 保留，主要是為了支援各種高對比主題。</span><span class="sxs-lookup"><span data-stu-id="01c95-113">The Windows classic model has been retained through Windows 7 mainly to support the various high contrast themes.</span></span> <span data-ttu-id="01c95-114">不過，Windows 傳統模型有一些缺點：</span><span class="sxs-lookup"><span data-stu-id="01c95-114">However, the Windows classic model has a number of drawbacks:</span></span>

-   <span data-ttu-id="01c95-115">不支援使用視覺化樣式的主題，例如 Windows Aero。</span><span class="sxs-lookup"><span data-stu-id="01c95-115">No support for themes that use visual styles, such as Windows Aero.</span></span> <span data-ttu-id="01c95-116">高對比主題的使用者必須使用 Windows 傳統 UI。</span><span class="sxs-lookup"><span data-stu-id="01c95-116">Users of high contrast themes must use the Windows classic UI.</span></span>
-   <span data-ttu-id="01c95-117">不支援依賴桌面視窗管理員 (DWM) 執行的 UI 功能，例如縮圖預覽和 Windows 7 中引進的全螢幕放大鏡。</span><span class="sxs-lookup"><span data-stu-id="01c95-117">No support for UI features that rely on Desktop Window Manager (DWM) to run, such as thumbnail previews and the full screen magnifier that was introduced in Windows 7.</span></span>
-   <span data-ttu-id="01c95-118">開發人員必須維護兩個不同的程式碼路徑，以支援兩個不同的主題模型。</span><span class="sxs-lookup"><span data-stu-id="01c95-118">Developers must maintain two separate code paths to support the two different theming models.</span></span>

<span data-ttu-id="01c95-119">在 Windows 8 和更新版本中，下列主題模型的變更會解決先前的缺點：</span><span class="sxs-lookup"><span data-stu-id="01c95-119">In Windows 8 and later, the following changes to the theming model address the previous drawbacks:</span></span>

-   <span data-ttu-id="01c95-120">不再支援 Windows 傳統主題模型，讓開發人員只針對以 Windows 8 為目標的應用程式維護一個程式碼路徑。</span><span class="sxs-lookup"><span data-stu-id="01c95-120">The Windows classic theming model is no longer supported, enabling developers to maintain just one code path for applications that target only Windows 8.</span></span>
-   <span data-ttu-id="01c95-121">由於視覺效果樣式和 DWM 都在 Windows 8 中，因此高對比使用者可以存取縮圖預覽和全螢幕放大鏡等功能。</span><span class="sxs-lookup"><span data-stu-id="01c95-121">Because visual styles and DWM are on in Windows 8, high contrast users have access to features such as thumbnail previews and the full-screen magnifier.</span></span>
-   <span data-ttu-id="01c95-122">視覺化樣式支援設定各種 UI 元素的色彩，讓高對比使用者可以自訂 UI，以配合個別的需求和喜好設定。</span><span class="sxs-lookup"><span data-stu-id="01c95-122">Visual styles support setting the colors of various UI elements, enabling high contrast users to customize the UI to accommodate individual needs and preferences.</span></span>
-   <span data-ttu-id="01c95-123">Windows 8 包含的現有應用程式的相容性支援，是根據 Windows 傳統主題模型，設計成使用高對比主題。</span><span class="sxs-lookup"><span data-stu-id="01c95-123">Windows 8 includes compatibility support for existing applications that are designed to use high contrast themes based on the Windows classic theming model.</span></span>

## <a name="supporting-high-contrast-themes-in-windows-8-and-later"></a><span data-ttu-id="01c95-124">在 Windows 8 和更新版本中支援高對比主題</span><span class="sxs-lookup"><span data-stu-id="01c95-124">Supporting High Contrast Themes in Windows 8 and later</span></span>

<span data-ttu-id="01c95-125">在 Windows 8 中，因為視覺效果樣式是在高對比模式中，所以只要您注意下列指導方針，支援高對比的主題就會很簡單。</span><span class="sxs-lookup"><span data-stu-id="01c95-125">In Windows 8, because visual styles are on in high contrast mode, supporting high contrast themes is straightforward as long as you heed the following guidelines.</span></span>

-   <span data-ttu-id="01c95-126">字型和控制項大小。</span><span class="sxs-lookup"><span data-stu-id="01c95-126">Font and control sizes.</span></span> <span data-ttu-id="01c95-127">為了確保您的 UI 可供殘障使用者存取，請根據目前的主題設定來設定字型大小。</span><span class="sxs-lookup"><span data-stu-id="01c95-127">To ensure that your UI is accessible to users with disabilities, set font sizes according to the current theme settings.</span></span> <span data-ttu-id="01c95-128">將控制項的大小設定為至少預設大小。</span><span class="sxs-lookup"><span data-stu-id="01c95-128">Set the size of controls to be at least the default size.</span></span>
-   <span data-ttu-id="01c95-129">[色彩]。</span><span class="sxs-lookup"><span data-stu-id="01c95-129">Colors.</span></span> <span data-ttu-id="01c95-130">避免使用硬式編碼的色彩。</span><span class="sxs-lookup"><span data-stu-id="01c95-130">Avoid using hard-coded colors.</span></span> <span data-ttu-id="01c95-131">相反地，請使用系統色彩，因為它們是以目前的主題為基礎。</span><span class="sxs-lookup"><span data-stu-id="01c95-131">Instead, use the system colors because they are based on the current theme.</span></span> <span data-ttu-id="01c95-132">使用自訂色彩可能會干擾和覆寫高對比主題中的色彩。</span><span class="sxs-lookup"><span data-stu-id="01c95-132">Using custom colors can interfere with and override the colors in the high contrast themes.</span></span>
-   <span data-ttu-id="01c95-133">應用程式資訊清單。</span><span class="sxs-lookup"><span data-stu-id="01c95-133">Application manifest.</span></span> <span data-ttu-id="01c95-134">設計用來使用新高對比主題的應用程式應該在其資訊清單中定義應用程式相容性區段，其中包含 Windows 8 相容性 Guid。</span><span class="sxs-lookup"><span data-stu-id="01c95-134">Applications designed to work with the new high contrast themes should have an application compatibility section defined in their manifest that contains the Windows 8 compatibility GUIDs.</span></span> <span data-ttu-id="01c95-135">否則，Windows 會假設應用程式是針對較舊版本的 Windows 所設計，並藉由模擬 Windows 傳統主題模型來呈現應用程式 UI。</span><span class="sxs-lookup"><span data-stu-id="01c95-135">Otherwise, Windows assumes that the application is designed for an older version of Windows and renders the application UI by simulating the Windows classic theming model.</span></span>

## <a name="adding-a-compatibility-section-to-your-application-manifest"></a><span data-ttu-id="01c95-136">將相容性區段新增至您的應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="01c95-136">Adding a Compatibility Section to Your Application Manifest</span></span>

<span data-ttu-id="01c95-137">應用程式資訊清單是描述應用程式需求的 XML 檔。</span><span class="sxs-lookup"><span data-stu-id="01c95-137">An application manifest is an XML file that describes the requirements for an application.</span></span> <span data-ttu-id="01c95-138">資訊清單的相容性區段會識別應用程式所支援的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="01c95-138">The compatibility section of the manifest identifies the versions of Windows supported by the application.</span></span> <span data-ttu-id="01c95-139">[相容性] 區段中會使用下列 Guid 來識別各種不同版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="01c95-139">The following GUIDs are used in the compatibility section to identify the various versions of Windows.</span></span>

| <span data-ttu-id="01c95-140">版本</span><span class="sxs-lookup"><span data-stu-id="01c95-140">Version</span></span>       | <span data-ttu-id="01c95-141">GUID</span><span class="sxs-lookup"><span data-stu-id="01c95-141">GUID</span></span>                                   |
|---------------|----------------------------------------|
| <span data-ttu-id="01c95-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01c95-142">Windows Vista</span></span> | <span data-ttu-id="01c95-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="01c95-143">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span> |
| <span data-ttu-id="01c95-144">Windows 7</span><span class="sxs-lookup"><span data-stu-id="01c95-144">Windows 7</span></span>     | <span data-ttu-id="01c95-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="01c95-145">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span> |
| <span data-ttu-id="01c95-146">Windows 8</span><span class="sxs-lookup"><span data-stu-id="01c95-146">Windows 8</span></span>     | <span data-ttu-id="01c95-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="01c95-147">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span> |



 

<span data-ttu-id="01c95-148">相容性區段可以指定多個版本的 Windows，但每個版本都必須包含在它自己的 `<supportedOS/>` 標記內。</span><span class="sxs-lookup"><span data-stu-id="01c95-148">The compatibility section can specify multiple versions of Windows, but each must be contained within its own `<supportedOS/>` tag.</span></span> <span data-ttu-id="01c95-149">下列範例顯示在相容性區段中指定 Windows 7 和 Windows 8 的應用程式資訊清單：</span><span class="sxs-lookup"><span data-stu-id="01c95-149">The following example shows an application manifest that specifies Windows 7 and Windows 8 in the compatibility section:</span></span>


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1">
        <application>
            <!--The ID below indicates application support for Windows 8 -->
            <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>

            <!--The ID below indicates application support for Windows 7 -->
            <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        </application>
    </compatibility>
</assembly>
```



<span data-ttu-id="01c95-150">如果應用程式沒有相容性資訊清單，則會假設為 Windows Vista 應用程式，且當高對比主題為使用中時，不會在工作區中使用主題控制項。</span><span class="sxs-lookup"><span data-stu-id="01c95-150">If an application does not have a compatibility manifest, it is assumed to be a Windows Vista application and does not use themed controls in the client area when a high contrast theme is active.</span></span> <span data-ttu-id="01c95-151">此外，某些視覺效果樣式函式的行為會受到影響。</span><span class="sxs-lookup"><span data-stu-id="01c95-151">Also, the behavior of some visual styles functions are affected.</span></span> <span data-ttu-id="01c95-152">例如， [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive)、 [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive)和 [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) 會傳回 FALSE，而 [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) 和 [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) 則會傳回 Null 控制碼。</span><span class="sxs-lookup"><span data-stu-id="01c95-152">For example, [**IsThemeActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-isthemeactive), [**IsCompositionActive**](/windows/desktop/api/Uxtheme/nf-uxtheme-iscompositionactive), and [**IsAppThemed**](/windows/desktop/api/Uxtheme/nf-uxtheme-isappthemed) return FALSE, while [**OpenThemeData**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedata) and [**OpenThemeDataEx**](/windows/desktop/api/Uxtheme/nf-uxtheme-openthemedataex) return a NULL handle.</span></span> <span data-ttu-id="01c95-153">這是為了提供相容性支援，因此在 Windows 8 之前建立的應用程式仍然可以像舊版 Windows （視覺效果樣式無法使用）的高對比模式一樣呈現其 UI。</span><span class="sxs-lookup"><span data-stu-id="01c95-153">This is for compatibility support, so that applications built before Windows 8 can still render their UI in the same look as the high contrast mode of previous versions of Windows where visual styles are not available.</span></span>

<span data-ttu-id="01c95-154">在 Windows 8，應用程式仍會獲得桌面電腦群組合的優點。</span><span class="sxs-lookup"><span data-stu-id="01c95-154">On Windows 8, the application still receives the benefits of desktop composition.</span></span> <span data-ttu-id="01c95-155">例如，這表示可用性應用程式（例如，全螢幕放大鏡）不會依賴個別應用程式資訊清單的狀態。</span><span class="sxs-lookup"><span data-stu-id="01c95-155">This means, for example, that usability applications such as the full screen magnifier don't depend on the status of an individual application's manifest.</span></span> <span data-ttu-id="01c95-156">可用性應用程式會繼續在高對比模式下運作，而應用程式不會在其資訊清單中識別為 Windows 8 相容性。</span><span class="sxs-lookup"><span data-stu-id="01c95-156">The usability application continues to work in high contrast mode with an application that does not identify itself as Windows 8 compatible in its manifest.</span></span>

<span data-ttu-id="01c95-157">下列影像顯示在 Windows 7 上具有高對比的簡單對話方塊。</span><span class="sxs-lookup"><span data-stu-id="01c95-157">The following images show a simple dialog box in high contrast on Windows 7.</span></span>

![hig 對比對話方塊](images/win7-high-contrast.png)

<span data-ttu-id="01c95-159">此影像會在 Windows 8 上顯示相同的對話方塊，但在應用程式資訊清單中指定了 Windows 7 相容性：</span><span class="sxs-lookup"><span data-stu-id="01c95-159">This image shows the same dialog box in high contrast on Windows 8, but with Windows 7 compatibility specified in the application manifest:</span></span>

![w8 高對比對話方塊](images/win7-compat.png)

<span data-ttu-id="01c95-161">此影像會顯示在 Windows 8 上具有高對比的相同對話方塊，並在應用程式資訊清單中指定 Windows 8：</span><span class="sxs-lookup"><span data-stu-id="01c95-161">This image shows the same dialog box in high contrast on Windows 8, with Windows 8 specified in the application manifest:</span></span>

![使用資訊清單 w8 高對比對話方塊](images/win8-manifest.png)

## <a name="detecting-high-contrast-in-previous-versions-of-windows"></a><span data-ttu-id="01c95-163">在舊版 Windows 中偵測高對比</span><span class="sxs-lookup"><span data-stu-id="01c95-163">Detecting High Contrast in Previous Versions of Windows</span></span>

<span data-ttu-id="01c95-164">在舊版 Windows 上執行的應用程式無法存取新的高對比主題。</span><span class="sxs-lookup"><span data-stu-id="01c95-164">Applications running on previous versions of Windows do not have access to the new high contrast themes.</span></span> <span data-ttu-id="01c95-165">如果您的應用程式需要在舊版中執行，您應該在 Windows 傳統主題模型中包含以高 contraWindowsst 轉譯 UI 的支援。</span><span class="sxs-lookup"><span data-stu-id="01c95-165">If your application needs to run on previous versions of , you should include support for rendering your UI in high contraWindowsst in the Windows classic theming model.</span></span> <span data-ttu-id="01c95-166">您的應用程式可以藉由使用 **SPI \_ GETHIGHCONTRAST** 旗標呼叫 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)函式，來判斷高對比主題是否為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="01c95-166">Your application can determine whether a high contrast theme is active by calling the [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) function with the **SPI\_GETHIGHCONTRAST** flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01c95-167">相關主題</span><span class="sxs-lookup"><span data-stu-id="01c95-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01c95-168">啟用視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="01c95-168">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="01c95-169">視覺化樣式</span><span class="sxs-lookup"><span data-stu-id="01c95-169">Visual Styles</span></span>](themes-overview.md)
</dt> </dl>

 

 