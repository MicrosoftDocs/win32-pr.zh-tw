---
title: 自訂驗證常式
description: 本節說明如何建立 UI 協助工具檢查程式 (AccChecker) tool 的自訂驗證常式。
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931996"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="5039f-103">自訂驗證常式</span><span class="sxs-lookup"><span data-stu-id="5039f-103">Custom Verification Routines</span></span>

<span data-ttu-id="5039f-104">本節說明如何建立 UI 協助工具檢查程式 (AccChecker) tool 的自訂驗證常式。</span><span class="sxs-lookup"><span data-stu-id="5039f-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="5039f-105">建立自訂驗證</span><span class="sxs-lookup"><span data-stu-id="5039f-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="5039f-106">自訂驗證範例</span><span class="sxs-lookup"><span data-stu-id="5039f-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="5039f-107">使用自訂驗證</span><span class="sxs-lookup"><span data-stu-id="5039f-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="5039f-108">AccChecker 圖形消費者介面 (GUI) </span><span class="sxs-lookup"><span data-stu-id="5039f-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="5039f-109">AccChecker 自動化</span><span class="sxs-lookup"><span data-stu-id="5039f-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="5039f-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="5039f-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="5039f-111">UI 協助工具檢查程式 (AccChecker) 是一種輔助功能測試工具，其設計目的是要驗證控制項或應用程式 UI 中 Microsoft Active Accessibility (MSAA) 的執行。</span><span class="sxs-lookup"><span data-stu-id="5039f-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="5039f-112">使用一組內建的自動化驗證常式來測試 MSAA 執行可能公開的高影響協助工具問題。</span><span class="sxs-lookup"><span data-stu-id="5039f-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="5039f-113">您可以使用可延伸的 AccChecker 平臺，利用自訂常式來增強這些原生驗證常式。</span><span class="sxs-lookup"><span data-stu-id="5039f-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="5039f-114">建立自訂驗證</span><span class="sxs-lookup"><span data-stu-id="5039f-114">Creating a Custom Verification</span></span>

<span data-ttu-id="5039f-115">自訂驗證是以類別庫 (DLL) 來建立的，它會 (`IVerificationRoutine`) 包含一個成員 () 的單一介面 `Execute` ：</span><span class="sxs-lookup"><span data-stu-id="5039f-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="5039f-116">**參數**</span><span class="sxs-lookup"><span data-stu-id="5039f-116">**Parameters**</span></span>

<span data-ttu-id="5039f-117">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="5039f-117">*hwnd*</span></span>

<span data-ttu-id="5039f-118">類型： **system.object**</span><span class="sxs-lookup"><span data-stu-id="5039f-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="5039f-119">要驗證之元素的 HWND。</span><span class="sxs-lookup"><span data-stu-id="5039f-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="5039f-120">*記錄*</span><span class="sxs-lookup"><span data-stu-id="5039f-120">*logger*</span></span>

<span data-ttu-id="5039f-121">類型： **AccCheck。 ILogger**</span><span class="sxs-lookup"><span data-stu-id="5039f-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="5039f-122">選取的記錄方法。</span><span class="sxs-lookup"><span data-stu-id="5039f-122">The selected logging method.</span></span> <span data-ttu-id="5039f-123">可能的類型包括 **AccumulatingLogger** (由 AccChecker 用來快取所有記錄專案，直到驗證完成為止) 、 **ConsoleLogger**、 **TextFileLogger** 和 **XMLSerializingLogger**。</span><span class="sxs-lookup"><span data-stu-id="5039f-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="5039f-124">*AllowUI*</span><span class="sxs-lookup"><span data-stu-id="5039f-124">*AllowUI*</span></span>

<span data-ttu-id="5039f-125">類型： **bool**</span><span class="sxs-lookup"><span data-stu-id="5039f-125">Type: **bool**</span></span>

<span data-ttu-id="5039f-126">指出驗證常式是否顯示正在測試的 UI。</span><span class="sxs-lookup"><span data-stu-id="5039f-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="5039f-127">通常會在自動化測試案例中設為 false。</span><span class="sxs-lookup"><span data-stu-id="5039f-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="5039f-128">*圖形*</span><span class="sxs-lookup"><span data-stu-id="5039f-128">*graphics*</span></span>

<span data-ttu-id="5039f-129">類型： **AccCheck. GraphicsHelper**</span><span class="sxs-lookup"><span data-stu-id="5039f-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="5039f-130">用於 AccChecker 中的螢幕擷取畫面和其他視覺效果。</span><span class="sxs-lookup"><span data-stu-id="5039f-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="5039f-131">自訂驗證範例</span><span class="sxs-lookup"><span data-stu-id="5039f-131">Sample Custom Verification</span></span>

<span data-ttu-id="5039f-132">下列範例是 c # 自訂驗證，可執行簡單的元素樹深度檢查。</span><span class="sxs-lookup"><span data-stu-id="5039f-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="5039f-133">如果專案樹狀結構的深度大於50層級，則會記錄錯誤，如果元素樹狀結構是深度20到50層級，則會記錄警告，否則會記錄資訊訊息。</span><span class="sxs-lookup"><span data-stu-id="5039f-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="5039f-134">包含驗證範例程式碼的 Microsoft Visual Studio 解決方案包含在說明文件中。</span><span class="sxs-lookup"><span data-stu-id="5039f-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="5039f-135">這些檔案位於 AccChecker 安裝路徑中。</span><span class="sxs-lookup"><span data-stu-id="5039f-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="5039f-136">使用自訂驗證</span><span class="sxs-lookup"><span data-stu-id="5039f-136">Using a Custom Verification</span></span>

<span data-ttu-id="5039f-137">本節說明如何將自訂驗證併入 AccChecker 測試案例中。</span><span class="sxs-lookup"><span data-stu-id="5039f-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="5039f-138">AccChecker 圖形消費者介面 (GUI) </span><span class="sxs-lookup"><span data-stu-id="5039f-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="5039f-139">若要在 AccChecker 應用程式中包含自訂驗證常式，只要按一下 [檔案] 功能表中的 [開啟 DLL]，並找出常式的 DLL。</span><span class="sxs-lookup"><span data-stu-id="5039f-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="5039f-140">自訂常式會新增至 [選取驗證常式] 窗格中驗證清單的底部。</span><span class="sxs-lookup"><span data-stu-id="5039f-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="5039f-141">下列螢幕擷取畫面顯示新增至 AccChecker 的範例檢查樹深度自訂驗證。</span><span class="sxs-lookup"><span data-stu-id="5039f-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![新增至 accchecker ui 的範例檢查樹深度自訂驗證常式](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="5039f-143">如果未在自訂驗證常式中指定驗證屬性值，即使它未出現在 UI 中，仍會將驗證載入 AccChecker 中。</span><span class="sxs-lookup"><span data-stu-id="5039f-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="5039f-144">因為它不會顯示在 UI 中，所以無法取消核取，也無法從後續的驗證執行中排除。</span><span class="sxs-lookup"><span data-stu-id="5039f-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="5039f-145">AccChecker 自動化</span><span class="sxs-lookup"><span data-stu-id="5039f-145">AccChecker Automation</span></span>

<span data-ttu-id="5039f-146">將自訂驗證常式併入自動化的 AccChecker 架構，就像新增驗證 DLL 和啟用所需的驗證常式一樣簡單。</span><span class="sxs-lookup"><span data-stu-id="5039f-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="5039f-147">下列程式碼片段示範如何使用 AccChecker API，在 [Windows 防火牆] 控制台應用程式中測試 tab 鍵功能。</span><span class="sxs-lookup"><span data-stu-id="5039f-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> 說明文件中包含包含驗證範例程式碼的 Microsoft Visual Studio 2008 解決方案。 <span data-ttu-id="5039f-149">這些檔案位於 AccChecker 安裝路徑中。</span><span class="sxs-lookup"><span data-stu-id="5039f-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5039f-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="5039f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5039f-151">UI 協助工具檢查程式</span><span class="sxs-lookup"><span data-stu-id="5039f-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




