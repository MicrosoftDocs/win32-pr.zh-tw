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
# <a name="ui-automation-test-library"></a><span data-ttu-id="5a384-103">消費者介面自動化測試程式庫</span><span class="sxs-lookup"><span data-stu-id="5a384-103">UI Automation Test Library</span></span>

<span data-ttu-id="5a384-104">消費者介面自動化測試程式庫 (UIA 測試程式庫) 是在自動化測試案例中，由 *驅動* 程式應用程式所呼叫的 API。</span><span class="sxs-lookup"><span data-stu-id="5a384-104">The UI Automation Test Library (UIA Test Library) is an API that is called by the *driver* application in an automated testing scenario.</span></span> <span data-ttu-id="5a384-105">驅動程式是從需要驗證的控制項取得 automation 元素 ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 物件) ，並將它提供給消費者介面自動化測試程式庫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="5a384-105">The driver is the application that obtains an automation element ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from a control that requires verification, and provides it to the UI Automation Test Library.</span></span> <span data-ttu-id="5a384-106">然後，測試程式庫會檢查並驗證消費者介面自動化的執行。</span><span class="sxs-lookup"><span data-stu-id="5a384-106">Then, the test library checks and validates the UI Automation implementation.</span></span> <span data-ttu-id="5a384-107">若要深入瞭解消費者介面自動化和 Automation 元素，請參閱 [消費者介面自動化基礎](entry-uiautocore-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="5a384-107">To learn more about UI Automation and automation elements, see [UI Automation Fundamentals](entry-uiautocore-overview.md).</span></span>

-   [<span data-ttu-id="5a384-108">消費者介面自動化測試程式庫工作流程</span><span class="sxs-lookup"><span data-stu-id="5a384-108">UI Automation Test Library Workflow</span></span>](#ui-automation-test-library-workflow)
-   [<span data-ttu-id="5a384-109">使用消費者介面自動化測試程式庫進行記錄</span><span class="sxs-lookup"><span data-stu-id="5a384-109">Logging with the UI Automation Test Library</span></span>](#logging-with-the-ui-automation-test-library)
    -   [<span data-ttu-id="5a384-110">XML 記錄</span><span class="sxs-lookup"><span data-stu-id="5a384-110">XML Logging</span></span>](#xml-logging)
    -   [<span data-ttu-id="5a384-111">主控台記錄</span><span class="sxs-lookup"><span data-stu-id="5a384-111">Console Logging</span></span>](#console-logging)
    -   [<span data-ttu-id="5a384-112">記錄的程式碼需求</span><span class="sxs-lookup"><span data-stu-id="5a384-112">Code Requirements for Logging</span></span>](#code-requirements-for-logging)
    -   [<span data-ttu-id="5a384-113">記錄範例</span><span class="sxs-lookup"><span data-stu-id="5a384-113">Logging Examples</span></span>](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a><span data-ttu-id="5a384-114">消費者介面自動化測試程式庫工作流程</span><span class="sxs-lookup"><span data-stu-id="5a384-114">UI Automation Test Library Workflow</span></span>

<span data-ttu-id="5a384-115">下圖顯示使用主控台應用程式做為驅動程式來併入消費者介面自動化測試程式庫的測試工作流程。</span><span class="sxs-lookup"><span data-stu-id="5a384-115">The following diagram shows a test workflow that incorporates the UI Automation Test Library by using a console application as the driver.</span></span> <span data-ttu-id="5a384-116">在此情況下，驅動程式會啟動 Notepad.exe 的實例，並取得自動化元素， (也就是從編輯控制項) 的 [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) 物件。</span><span class="sxs-lookup"><span data-stu-id="5a384-116">In this case, the driver starts an instance of Notepad.exe and obtains an automation element (that is, a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from the edit control.</span></span> <span data-ttu-id="5a384-117">接下來，驅動程式會根據所測試的 UI 平臺建立消費者介面自動化測試程式庫物件，然後將 Automation 元素當作參數傳遞。</span><span class="sxs-lookup"><span data-stu-id="5a384-117">Next, the driver creates a UI Automation Test Library object based on the UI platform being tested, and then passes in the automation element as a parameter.</span></span> <span data-ttu-id="5a384-118">消費者介面自動化測試程式庫會判斷 Automation 元素是 [檔](uiauto-supportdocumentcontroltype.md) 控制項類型，然後執行檔控制項測試、 [文字](uiauto-implementingtextandtextrange.md) 和 [滾動](uiauto-implementingscroll.md) 條控制項模式測試，以及一般 Automation 元素測試。</span><span class="sxs-lookup"><span data-stu-id="5a384-118">The UI Automation Test Library determines that the automation element is a [Document](uiauto-supportdocumentcontroltype.md) control type, and then executes the Document control tests, the [Text](uiauto-implementingtextandtextrange.md) and [Scroll](uiauto-implementingscroll.md) control pattern tests, and generic automation element tests.</span></span>

![此圖顯示使用紅色箭號 UIATestLibrary 的驅動程式至驅動程式至驅動程式的流程。](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a><span data-ttu-id="5a384-120">使用消費者介面自動化測試程式庫進行記錄</span><span class="sxs-lookup"><span data-stu-id="5a384-120">Logging with the UI Automation Test Library</span></span>

<span data-ttu-id="5a384-121">消費者介面自動化測試程式庫會使用外部 Dll 來記錄測試回合的結果。</span><span class="sxs-lookup"><span data-stu-id="5a384-121">The UI Automation Test Library uses external DLLs to log results from test runs.</span></span> <span data-ttu-id="5a384-122">它支援以 XML 記錄和記錄至主控台。</span><span class="sxs-lookup"><span data-stu-id="5a384-122">It supports logging as XML and logging to the console.</span></span>

### <a name="xml-logging"></a><span data-ttu-id="5a384-123">XML 記錄</span><span class="sxs-lookup"><span data-stu-id="5a384-123">XML Logging</span></span>

<span data-ttu-id="5a384-124">XML 記錄通常是由 Visual 消費者介面自動化 Verify 使用，但也可以併入命令列工作流程中。</span><span class="sxs-lookup"><span data-stu-id="5a384-124">XML logging is typically used by Visual UI Automation Verify, but it can also be incorporated into a command-line workflow.</span></span>

<span data-ttu-id="5a384-125">如果指定 XML 記錄，驅動程式應用程式必須建立 **XmlWriter** 物件，並將它傳遞至 **XmlLog. GetTestRunXml** 方法，以將輸出序列化。</span><span class="sxs-lookup"><span data-stu-id="5a384-125">If XML logging is specified, the driver application must serialize the output by creating an **XmlWriter** object and passing it to the **XmlLog.GetTestRunXml** method.</span></span> <span data-ttu-id="5a384-126">然後，驅動程式就可以在內部使用序列化的 XML，或將它寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="5a384-126">The driver can then use the serialized XML internally or write it to a file.</span></span>

<span data-ttu-id="5a384-127">以下是 XML 記錄所需的 Dll。</span><span class="sxs-lookup"><span data-stu-id="5a384-127">The following DLLs are required for XML logging.</span></span>

-   <span data-ttu-id="5a384-128">WUIALogging.dll</span><span class="sxs-lookup"><span data-stu-id="5a384-128">WUIALogging.dll</span></span>
-   <span data-ttu-id="5a384-129">WUIALoggerXml.dll</span><span class="sxs-lookup"><span data-stu-id="5a384-129">WUIALoggerXml.dll</span></span>

### <a name="console-logging"></a><span data-ttu-id="5a384-130">主控台記錄</span><span class="sxs-lookup"><span data-stu-id="5a384-130">Console Logging</span></span>

<span data-ttu-id="5a384-131">根據預設，消費者介面自動化測試程式庫會使用主控台記錄，其中所有記錄輸出都會以純文字形式輸送至主控台視窗。</span><span class="sxs-lookup"><span data-stu-id="5a384-131">By default, the UI Automation Test Library uses console logging, where all logging output is piped as plain text to the console window.</span></span> <span data-ttu-id="5a384-132">主控台記錄需要 WUIALogging.dll。</span><span class="sxs-lookup"><span data-stu-id="5a384-132">WUIALogging.dll is required for console logging.</span></span>

### <a name="code-requirements-for-logging"></a><span data-ttu-id="5a384-133">記錄的程式碼需求</span><span class="sxs-lookup"><span data-stu-id="5a384-133">Code Requirements for Logging</span></span>

<span data-ttu-id="5a384-134">驅動程式應用程式必須包含下列程式碼片段，才能使用消費者介面自動化測試程式庫記錄。</span><span class="sxs-lookup"><span data-stu-id="5a384-134">A driver application must include the following code snippets to use UI Automation Test Library logging.</span></span>


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



### <a name="logging-examples"></a><span data-ttu-id="5a384-135">記錄範例</span><span class="sxs-lookup"><span data-stu-id="5a384-135">Logging Examples</span></span>

<span data-ttu-id="5a384-136">下列範例示範基本的記錄功能，並示範如何在基本的測試自動化驅動程式應用程式中使用消費者介面自動化測試程式庫 API。</span><span class="sxs-lookup"><span data-stu-id="5a384-136">The following examples demonstrate basic logging functionality and show how to use the UI Automation Test Library API in a basic test automation driver application.</span></span>


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



 

 




