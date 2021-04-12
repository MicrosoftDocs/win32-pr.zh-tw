---
description: 說明如何使用 PenInputPanel 物件來編寫系統層級的 Tablet PC 輸入面板。
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: 使用 PenInputPanel 類別來設計輸入面板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320732"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a><span data-ttu-id="aadeb-103">使用 PenInputPanel 類別來設計輸入面板</span><span class="sxs-lookup"><span data-stu-id="aadeb-103">Programming the Input Panel Using the PenInputPanel Class</span></span>

<span data-ttu-id="aadeb-104">\[[**PenInputPanel**](peninputpanel-class.md) 已被 [>textinput](/previous-versions/ms581554(v=vs.100))取代。</span><span class="sxs-lookup"><span data-stu-id="aadeb-104">\[[**PenInputPanel**](peninputpanel-class.md) has been replaced by [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100)).</span></span> <span data-ttu-id="aadeb-105">請參閱程式 [設計文字輸入面板](programming-the-text-input-panel.md)。\]</span><span class="sxs-lookup"><span data-stu-id="aadeb-105">Please refer to [Programming the Text Input Panel](programming-the-text-input-panel.md).\]</span></span>

<span data-ttu-id="aadeb-106">說明如何使用 [**PenInputPanel**](peninputpanel-class.md) 物件來編寫系統層級的 Tablet PC 輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-106">Description of using the [**PenInputPanel**](peninputpanel-class.md) object to program the system-level Tablet PC Input Panel.</span></span>

## <a name="input-panel-vs-the-peninputpanel-object"></a><span data-ttu-id="aadeb-107">輸入面板與 PenInputPanel 物件</span><span class="sxs-lookup"><span data-stu-id="aadeb-107">Input Panel vs. the PenInputPanel Object</span></span>

<span data-ttu-id="aadeb-108">在 Microsoft Windows XP Tablet PC Edition 1.0 版中，系統層級的 Tablet PC 輸入面板提供了通用的機制，可在 Windows 平臺上完成文字輸入，但不提供程式設計的存取。</span><span class="sxs-lookup"><span data-stu-id="aadeb-108">In Microsoft Windows XP Tablet PC Edition version 1.0, the system-level Tablet PC Input Panel provides a universal mechanism to accomplish text input across the Windows platform, but it does not provide programmatic access.</span></span> <span data-ttu-id="aadeb-109">在 Windows XP Tablet PC Edition 軟體發展工具組中 (SDK) 1.5 版和更新版本中， [**PenInputPanel**](peninputpanel-class.md) 物件可讓您將文字輸入工具直接整合到您的應用程式，並提供先前未提供的控制層級。</span><span class="sxs-lookup"><span data-stu-id="aadeb-109">In Windows XP Tablet PC Edition Software Development Kit (SDK) version 1.5 and later, the [**PenInputPanel**](peninputpanel-class.md) object enables you to integrate text input tools directly into your applications, and provide a level of control not previously available.</span></span> <span data-ttu-id="aadeb-110">從 Windows XP Tablet PC Edition 2005 開始，系統層級的輸入面板已升級為包含 **PenInputPanel** 物件提供的就地輸入功能，以及更多。</span><span class="sxs-lookup"><span data-stu-id="aadeb-110">Starting with the Windows XP Tablet PC Edition 2005, the system-level Input Panel has been upgraded to include the in-place input functionality provided by the **PenInputPanel** object and more.</span></span>

<span data-ttu-id="aadeb-111">下圖顯示透過 [ [自動宣告表單範例](auto-claims-form-sample.md) ] 範例顯示的輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-111">The following graphic shows Input Panel displayed over the [Auto Claims Form Sample](auto-claims-form-sample.md) sample.</span></span>

![輸入面板會顯示在用於汽車宣告的表單上](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

<span data-ttu-id="aadeb-113">輸入面板會將相同的就地輸入功能提供給在 Windows XP Tablet PC Edition 2005 或更新版本上執行的任何應用程式，而不需要額外的程式碼，藉此取代 [**PenInputPanel**](peninputpanel-class.md) 。</span><span class="sxs-lookup"><span data-stu-id="aadeb-113">Input Panel supersedes the [**PenInputPanel**](peninputpanel-class.md) by supplying the same in-place input functionality to any application running on Windows XP Tablet PC Edition 2005 or later without the need for additional code.</span></span> <span data-ttu-id="aadeb-114">本文說明如何使用 **PenInputPanel** 物件來提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="aadeb-114">This article on using the **PenInputPanel** object is provided for backward compatibility.</span></span> <span data-ttu-id="aadeb-115">如果應用程式是在 Windows XP Tablet PC Edition 2005 或更新版本上執行，則已使用 **PenInputPanel** 物件的應用程式將會有相同的功能，但該輸入面板將會顯示，而不是 **PenInputPanel** 。</span><span class="sxs-lookup"><span data-stu-id="aadeb-115">Applications that already utilize the **PenInputPanel** object will function the same except that Input Panel will be displayed instead of the **PenInputPanel** when the application is run on Windows XP Tablet PC Edition 2005 or later.</span></span>

<span data-ttu-id="aadeb-116">如果您正在開發 Tablet PC 的新應用程式，而且想要擁有就地使用者輸入解決方案，輸入面板會在 Windows XP Tablet PC Edition 2005 或更新版本上自動提供此應用程式。</span><span class="sxs-lookup"><span data-stu-id="aadeb-116">If you are developing a new application for the Tablet PC and want to have an in-place user input solution, Input Panel provides this automatically on Windows XP Tablet PC Edition 2005 or later.</span></span> <span data-ttu-id="aadeb-117">不需要具現化 [**PenInputPanel**](peninputpanel-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="aadeb-117">There is no need to instantiate the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

## <a name="disabling-the-input-panel"></a><span data-ttu-id="aadeb-118">停用輸入面板</span><span class="sxs-lookup"><span data-stu-id="aadeb-118">Disabling the Input Panel</span></span>

<span data-ttu-id="aadeb-119">在某些情況下，您可能會想要停用輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-119">There may be cases where you want to disable Input Panel.</span></span> <span data-ttu-id="aadeb-120">有兩種方法可達成這個目標。</span><span class="sxs-lookup"><span data-stu-id="aadeb-120">There are two ways to accomplish this.</span></span> <span data-ttu-id="aadeb-121">您可以用程式設計的方式完成這項工作，或設定一個登錄專案來停用整個應用程式的輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-121">You can accomplish this programmatically or by setting a registry entry that disables Input Panel for your entire application.</span></span>

### <a name="disabling-input-panel-programmatically"></a><span data-ttu-id="aadeb-122">以程式設計方式停用輸入面板</span><span class="sxs-lookup"><span data-stu-id="aadeb-122">Disabling Input Panel Programmatically</span></span>

<span data-ttu-id="aadeb-123">若要以程式設計的方式停用輸入面板，請具現化 [**PenInputPanel**](peninputpanel-class.md) ，並 [**將其自動**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)**值** 屬性設定為</span><span class="sxs-lookup"><span data-stu-id="aadeb-123">To disable Input Panel programmatically, instantiate the [**PenInputPanel**](peninputpanel-class.md) and set its [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) property to **False**.</span></span>


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



<span data-ttu-id="aadeb-124">若要在單一應用程式中停用多個控制項的輸入面板，請為每個控制項具現化 [**PenInputPanel**](peninputpanel-class.md) 物件，並將每個控制項 [**的 [自動**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)] 屬性設定為 **False** ，或具現化單一 **PenInputPanel** ，並將其從控制項移至控制項，作為輸入焦點變更。</span><span class="sxs-lookup"><span data-stu-id="aadeb-124">To disable Input Panel for multiple controls in a single application, either instantiate a [**PenInputPanel**](peninputpanel-class.md) object for each control and set the [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)property to **False** for each or instantiate a single **PenInputPanel** and move it from control to control as input focus changes.</span></span> <span data-ttu-id="aadeb-125">如需這兩種技術的詳細資訊，請參閱 [PenInputPanel 範例](peninputpanel-sample.md) 主題。</span><span class="sxs-lookup"><span data-stu-id="aadeb-125">For more information about these two techniques, see the [PenInputPanel Sample](peninputpanel-sample.md) topic.</span></span>

### <a name="disabling-input-panel-through-the-registry"></a><span data-ttu-id="aadeb-126">透過登錄停用輸入面板</span><span class="sxs-lookup"><span data-stu-id="aadeb-126">Disabling Input Panel Through the Registry</span></span>

<span data-ttu-id="aadeb-127">您可以設定一個登錄專案，以停用整個應用程式的輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-127">You can set a registry entry to disable Input Panel for your entire application.</span></span> <span data-ttu-id="aadeb-128">不過，這也會對一般對話方塊停用它，例如 [ **開啟** 檔案] 對話方塊、[ **列印** ] 對話方塊和 [ **儲存** 盤案] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="aadeb-128">However, this will also disable it for common dialog boxes such as the **File Open** dialog box, the **Print** dialog box, and the **File Save** dialog box.</span></span> <span data-ttu-id="aadeb-129">這可能會讓應用程式中的使用者體驗與其他 Tablet PC 應用程式不一致。</span><span class="sxs-lookup"><span data-stu-id="aadeb-129">This may make the user experience in your application inconsistent with other Tablet PC applications.</span></span>

<span data-ttu-id="aadeb-130">將 `DisableInPlace` 登錄機碼設定為零，可避免在應用程式中出現輸入面板使用者介面 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="aadeb-130">Setting the `DisableInPlace` registry key to zero prevents Input Panel user interface (UI) from appearing in an application.</span></span> <span data-ttu-id="aadeb-131">您必須將登錄機 `DisableInPlace` 碼放在 `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` 。</span><span class="sxs-lookup"><span data-stu-id="aadeb-131">You must place the `DisableInPlace` registry key at `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\`.</span></span> <span data-ttu-id="aadeb-132">然後，使用您要在其中停用輸入面板的應用程式完整路徑來新增登錄值。</span><span class="sxs-lookup"><span data-stu-id="aadeb-132">Then, add a new registry value by using the full path of the application in which you want to disable Input Panel.</span></span> <span data-ttu-id="aadeb-133">下列範例登錄專案會在名為 MyApp 的應用程式中停用輸入面板：</span><span class="sxs-lookup"><span data-stu-id="aadeb-133">The following example registry entry disables Input Panel in an application called MyApp:</span></span>

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

<span data-ttu-id="aadeb-134">如果您在停用輸入面板 UI 之後仍看到應用程式發生問題，可能需要停用基礎架構，以查詢您的應用程式是否有插入號位置。</span><span class="sxs-lookup"><span data-stu-id="aadeb-134">If you still see a problem in your application after you disable the Input Panel UI, it may be necessary to disable the underlying framework, which queries your application for the caret location.</span></span> <span data-ttu-id="aadeb-135">例如，輸入面板可能會在應用程式的插入號追蹤程式碼中公開 bug。</span><span class="sxs-lookup"><span data-stu-id="aadeb-135">For example, Input Panel may expose a bug in your application's caret tracking code.</span></span> <span data-ttu-id="aadeb-136">關閉插入號追蹤查詢也可防止輸入面板 UI 出現。</span><span class="sxs-lookup"><span data-stu-id="aadeb-136">Turning off the caret tracking query also prevents the Input Panel UI from appearing.</span></span> <span data-ttu-id="aadeb-137">若要停用架構，請將登錄機 `EnableCaretTracking` 碼設定為零。</span><span class="sxs-lookup"><span data-stu-id="aadeb-137">To disable the framework, set the `EnableCaretTracking` registry key to zero.</span></span> <span data-ttu-id="aadeb-138">在上找出此金鑰 `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` 。</span><span class="sxs-lookup"><span data-stu-id="aadeb-138">Locate this key at `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\`.</span></span>

> [!Note]  
> <span data-ttu-id="aadeb-139">Windows XP 中的協助工具工具和語音技術也會使用此架構，因此停用查詢也會在您的應用程式中停用這些功能。</span><span class="sxs-lookup"><span data-stu-id="aadeb-139">Accessibility tools and speech technology in Windows XP also use this framework, so disabling the query also disables these features in your application.</span></span>

 

## <a name="the-input-panel-and-web-pages"></a><span data-ttu-id="aadeb-140">輸入面板和網頁</span><span class="sxs-lookup"><span data-stu-id="aadeb-140">The Input Panel and Web Pages</span></span>

<span data-ttu-id="aadeb-141">為了在網頁上使用 API，它必須在部分信任環境中運作。</span><span class="sxs-lookup"><span data-stu-id="aadeb-141">In order to use an API on a Web page, it must function in a partial trust environment.</span></span> <span data-ttu-id="aadeb-142">所有 [**PenInputPanel**](peninputpanel-class.md) 類別成員都需要完全信任，但下列除外：</span><span class="sxs-lookup"><span data-stu-id="aadeb-142">All [**PenInputPanel**](peninputpanel-class.md) class members require full trust except the following:</span></span>

-   <span data-ttu-id="aadeb-143">僅 (managed 程式碼) 的[PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90))函式</span><span class="sxs-lookup"><span data-stu-id="aadeb-143">[PenInputPanel Constructors](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (managed code only)</span></span>
-   <span data-ttu-id="aadeb-144">[Dispose 方法](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (僅限 managed 程式碼) </span><span class="sxs-lookup"><span data-stu-id="aadeb-144">[Dispose Method](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (managed code only)</span></span>
-   <span data-ttu-id="aadeb-145">[AttachedEditControl 屬性](/previous-versions/ms582239(v=vs.100)) (僅限 managed 程式碼) </span><span class="sxs-lookup"><span data-stu-id="aadeb-145">[AttachedEditControl Property](/previous-versions/ms582239(v=vs.100)) (managed code only)</span></span>
-   [<span data-ttu-id="aadeb-146">**自動屬性**</span><span class="sxs-lookup"><span data-stu-id="aadeb-146">**AutoShow Property**</span></span>](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

<span data-ttu-id="aadeb-147">這些 Api 會在部分信任環境中運作，例如網頁，可讓您具現化 [**PenInputPanel**](peninputpanel-class.md) 物件、將它附加至控制項，以及停用該控制項的輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-147">These APIs function in a partial trust environment, such as a Web page, enabling you to instantiate a [**PenInputPanel**](peninputpanel-class.md) object, attach it to a control, and disable Input Panel for that control.</span></span> <span data-ttu-id="aadeb-148">如需詳細資訊，請參閱使用 [網頁上](ink-on-the-web.md)的 PenInputPanel 類別和筆墨來設計輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-148">For more information, see Programming the Input Panel Using the PenInputPanel Class and [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="the-peninputpanel-object"></a><span data-ttu-id="aadeb-149">PenInputPanel 物件</span><span class="sxs-lookup"><span data-stu-id="aadeb-149">The PenInputPanel Object</span></span>

<span data-ttu-id="aadeb-150">本主題的其餘部分將說明如何在啟用 Tablet PC 的應用程式中使用 [**PenInputPanel**](peninputpanel-class.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="aadeb-150">The rest of this topic describes how to use the [**PenInputPanel**](peninputpanel-class.md) object in your Tablet PC–enabled applications.</span></span> <span data-ttu-id="aadeb-151">更具體來說，本主題會參考 **PenInputPanel** 物件在討論程式設計物件時，參考 UI 元素時的 [畫筆輸入面板]，而 [電腦輸入面板] (或 [輸入面板]) 參考到 Tablet PC 螢幕側邊的全域輸入面板。</span><span class="sxs-lookup"><span data-stu-id="aadeb-151">More specifically, this topic refers to the **PenInputPanel** object when discussing the programming object, the pen input panel when referring to the UI element, and the PC Input Panel (or Input Panel) when referring to the global input panel typically found on the side of the Tablet PC screen.</span></span>

<span data-ttu-id="aadeb-152">下列各節說明 [**PenInputPanel**](peninputpanel-class.md) 物件和 UI。</span><span class="sxs-lookup"><span data-stu-id="aadeb-152">The following sections describe the [**PenInputPanel**](peninputpanel-class.md) object and UI.</span></span>

-   [<span data-ttu-id="aadeb-153">關於輸入面板</span><span class="sxs-lookup"><span data-stu-id="aadeb-153">About the Input Panel</span></span>](about-the-input-panel.md)
-   [<span data-ttu-id="aadeb-154">具現化 PenInputPanel 類別</span><span class="sxs-lookup"><span data-stu-id="aadeb-154">Instantiating the PenInputPanel Class</span></span>](instantiating-the-peninputpanel-class.md)
-   [<span data-ttu-id="aadeb-155">模擬支援</span><span class="sxs-lookup"><span data-stu-id="aadeb-155">Factoid Support</span></span>](factoid-support.md)
-   [<span data-ttu-id="aadeb-156">Text Services Framework (TSF)</span><span class="sxs-lookup"><span data-stu-id="aadeb-156">Text Services Framework</span></span>](text-services-framework.md)
-   [<span data-ttu-id="aadeb-157">最佳作法</span><span class="sxs-lookup"><span data-stu-id="aadeb-157">Best Practices</span></span>](best-practices.md)

 

 
