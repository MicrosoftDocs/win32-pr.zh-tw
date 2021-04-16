---
title: 消費者介面自動化測試程式庫
description: 消費者介面自動化測試程式庫 (UIA 測試程式庫) 是在自動化測試案例中，由驅動程式應用程式所呼叫的 API。
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "104551865"
---
# <a name="ui-automation-test-library"></a>消費者介面自動化測試程式庫

消費者介面自動化測試程式庫 (UIA 測試程式庫) 是在自動化測試案例中，由 *驅動* 程式應用程式所呼叫的 API。 驅動程式是從需要驗證的控制項取得 automation 元素 ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 物件) ，並將它提供給消費者介面自動化測試程式庫的應用程式。 然後，測試程式庫會檢查並驗證消費者介面自動化的執行。 若要深入瞭解消費者介面自動化和 Automation 元素，請參閱 [消費者介面自動化基礎](entry-uiautocore-overview.md)。

-   [消費者介面自動化測試程式庫工作流程](#ui-automation-test-library-workflow)
-   [使用消費者介面自動化測試程式庫進行記錄](#logging-with-the-ui-automation-test-library)
    -   [XML 記錄](#xml-logging)
    -   [主控台記錄](#console-logging)
    -   [記錄的程式碼需求](#code-requirements-for-logging)
    -   [記錄範例](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>消費者介面自動化測試程式庫工作流程

下圖顯示使用主控台應用程式做為驅動程式來併入消費者介面自動化測試程式庫的測試工作流程。 在此情況下，驅動程式會啟動 Notepad.exe 的實例，並取得自動化元素， (也就是從編輯控制項) 的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 物件。 接下來，驅動程式會根據所測試的 UI 平臺建立消費者介面自動化測試程式庫物件，然後將 Automation 元素當作參數傳遞。 消費者介面自動化測試程式庫會判斷 Automation 元素是 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型，然後執行檔控制項測試、 [文字](uiauto-implementingtextandtextrange.md) 和 [滾動](uiauto-implementingscroll.md) 條控制項模式測試，以及一般 Automation 元素測試。

![此圖顯示使用紅色箭號 UIATestLibrary 的驅動程式至驅動程式至驅動程式的流程。](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>使用消費者介面自動化測試程式庫進行記錄

消費者介面自動化測試程式庫會使用外部 Dll 來記錄測試回合的結果。 它支援以 XML 記錄和記錄至主控台。

### <a name="xml-logging"></a>XML 記錄

XML 記錄通常是由 Visual 消費者介面自動化 Verify 使用，但也可以併入命令列工作流程中。

如果指定 XML 記錄，驅動程式應用程式必須建立 **XmlWriter** 物件，並將它傳遞至 **XmlLog. GetTestRunXml** 方法，以將輸出序列化。 然後，驅動程式就可以在內部使用序列化的 XML，或將它寫入檔案。

以下是 XML 記錄所需的 Dll。

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>主控台記錄

根據預設，消費者介面自動化測試程式庫會使用主控台記錄，其中所有記錄輸出都會以純文字形式輸送至主控台視窗。 主控台記錄需要 WUIALogging.dll。

### <a name="code-requirements-for-logging"></a>記錄的程式碼需求

驅動程式應用程式必須包含下列程式碼片段，才能使用消費者介面自動化測試程式庫記錄。


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a>記錄範例

下列範例示範基本的記錄功能，並示範如何在基本的測試自動化驅動程式應用程式中使用消費者介面自動化測試程式庫 API。


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




