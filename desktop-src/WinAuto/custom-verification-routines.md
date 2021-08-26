---
title: 自訂驗證常式
description: 本節說明如何建立 UI 協助工具檢查程式 (AccChecker) tool 的自訂驗證常式。
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 245865a0ab4aa6848d4a4361a30febbb341742208586ebf4ec5b35c34fa30534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030880"
---
# <a name="custom-verification-routines"></a>自訂驗證常式

本節說明如何建立 UI 協助工具檢查程式 (AccChecker) tool 的自訂驗證常式。

-   [建立自訂驗證](#creating-a-custom-verification)
    -   [自訂驗證範例](#sample-custom-verification)
-   [使用自訂驗證](#using-a-custom-verification)
    -   [AccChecker 圖形消費者介面 (GUI) ](#the-accchecker-graphical-user-interface-gui)
    -   [AccChecker 自動化](#accchecker-automation)
-   [相關主題](#related-topics)

UI 協助工具檢查程式 (AccChecker) 是一種輔助功能測試工具，其設計目的是要驗證控制項或應用程式 UI 中 Microsoft Active Accessibility (MSAA) 的執行。 使用一組內建的自動化驗證常式來測試 MSAA 執行可能公開的高影響協助工具問題。 您可以使用可延伸的 AccChecker 平臺，利用自訂常式來增強這些原生驗證常式。

## <a name="creating-a-custom-verification"></a>建立自訂驗證

自訂驗證是以類別庫 (DLL) 來建立的，它會 (`IVerificationRoutine`) 包含一個成員 () 的單一介面 `Execute` ：


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



**參數**

*hwnd*

類型： **system.object**

要驗證之元素的 HWND。

*記錄*

類型： **AccCheck。 ILogger**

選取的記錄方法。 可能的類型包括 **AccumulatingLogger** (由 AccChecker 用來快取所有記錄專案，直到驗證完成為止) 、 **ConsoleLogger**、 **TextFileLogger** 和 **XMLSerializingLogger**。

*AllowUI*

類型： **bool**

指出驗證常式是否顯示正在測試的 UI。 通常會在自動化測試案例中設為 false。

*圖形*

類型： **AccCheck. GraphicsHelper**

用於 AccChecker 中的螢幕擷取畫面和其他視覺效果。

### <a name="sample-custom-verification"></a>自訂驗證範例

下列範例是 c # 自訂驗證，可執行簡單的元素樹深度檢查。 如果專案樹狀結構的深度大於50層級，則會記錄錯誤，如果元素樹狀結構是深度20到50層級，則會記錄警告，否則會記錄資訊訊息。


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
> 包含驗證範例程式碼的 Microsoft Visual Studio 解決方案包含在說明文件中。 這些檔案位於 AccChecker 安裝路徑中。

 

## <a name="using-a-custom-verification"></a>使用自訂驗證

本節說明如何將自訂驗證併入 AccChecker 測試案例中。

### <a name="the-accchecker-graphical-user-interface-gui"></a>AccChecker 圖形消費者介面 (GUI) 

若要在 AccChecker 應用程式中包含自訂驗證常式，只要按一下 [檔案] 功能表中的 [開啟 DLL]，並找出常式的 DLL。 自訂常式會新增至 [選取驗證常式] 窗格中驗證清單的底部。

下列螢幕擷取畫面顯示新增至 AccChecker 的範例檢查樹深度自訂驗證。

![新增至 accchecker ui 的範例檢查樹深度自訂驗證常式](images/accchecker-sample-custom-verification.png)

> [!Note]  
> 如果未在自訂驗證常式中指定驗證屬性值，即使它未出現在 UI 中，仍會將驗證載入 AccChecker 中。 因為它不會顯示在 UI 中，所以無法取消核取，也無法從後續的驗證執行中排除。

 

### <a name="accchecker-automation"></a>AccChecker 自動化

將自訂驗證常式併入自動化的 AccChecker 架構，就像新增驗證 DLL 和啟用所需的驗證常式一樣簡單。

下列程式碼片段示範如何使用 AccChecker API，在 Windows 防火牆控制台應用程式中測試 tab 鍵功能。


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
> 說明文件中包含包含驗證範例程式碼的 Microsoft Visual Studio 2008 解決方案。 這些檔案位於 AccChecker 安裝路徑中。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 協助工具檢查程式](ui-accessibility-checker.md)
</dt> </dl>

 

 




