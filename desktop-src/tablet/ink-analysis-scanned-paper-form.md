---
description: 這個範例示範如何使用筆墨分析來建立表單填滿應用程式，其中的表單是以掃描的紙張表單為基礎。
ms.assetid: 1eae5962-b4e0-4947-a6d2-63713a68198c
title: 筆跡分析掃描的紙張表單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94d366c77e19bd5c32d3d1e4efa286cb3b089ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191167"
---
# <a name="ink-analysis-scanned-paper-form"></a><span data-ttu-id="5feeb-103">筆跡分析掃描的紙張表單</span><span class="sxs-lookup"><span data-stu-id="5feeb-103">Ink Analysis Scanned Paper Form</span></span>

<span data-ttu-id="5feeb-104">這個範例示範如何使用筆墨分析來建立表單填滿應用程式，其中的表單是以掃描的紙張表單為基礎。</span><span class="sxs-lookup"><span data-stu-id="5feeb-104">This sample shows how to use Ink Analysis to create a form-filling application, where the form is based on a scanned paper form.</span></span>

## <a name="features-demonstrated"></a><span data-ttu-id="5feeb-105">示範的功能</span><span class="sxs-lookup"><span data-stu-id="5feeb-105">Features Demonstrated</span></span>

<span data-ttu-id="5feeb-106">這個範例應用程式示範筆墨分析 API 的下列功能，以及 Windows Forms 筆墨控制項：</span><span class="sxs-lookup"><span data-stu-id="5feeb-106">This sample application demonstrates the following features of the Ink Analysis API and the Windows Forms Ink Controls:</span></span>

-   <span data-ttu-id="5feeb-107">正在載入掃描的紙張表單。</span><span class="sxs-lookup"><span data-stu-id="5feeb-107">Loading a scanned paper form.</span></span> <span data-ttu-id="5feeb-108">此範例會從 .png 格式的影像匯入表單。</span><span class="sxs-lookup"><span data-stu-id="5feeb-108">The sample imports the form from an image in .png format.</span></span>
-   <span data-ttu-id="5feeb-109">在掃描的表單上方收集和轉譯筆墨。</span><span class="sxs-lookup"><span data-stu-id="5feeb-109">Collecting and rendering ink on top of the scanned form.</span></span>
-   <span data-ttu-id="5feeb-110">使用 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 物件來剖析手寫。</span><span class="sxs-lookup"><span data-stu-id="5feeb-110">Using an [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object to parse handwriting.</span></span>
-   <span data-ttu-id="5feeb-111">產生 [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) 物件以改善手寫結果。</span><span class="sxs-lookup"><span data-stu-id="5feeb-111">Generating [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects to improve handwriting results.</span></span>
-   <span data-ttu-id="5feeb-112">從分析提示填入文字方塊。</span><span class="sxs-lookup"><span data-stu-id="5feeb-112">Populating text boxes from analysis hints.</span></span>
-   <span data-ttu-id="5feeb-113">建立基本文字修正體驗。</span><span class="sxs-lookup"><span data-stu-id="5feeb-113">Creating a basic text correction experience.</span></span>

## <a name="project-references"></a><span data-ttu-id="5feeb-114">專案參考</span><span class="sxs-lookup"><span data-stu-id="5feeb-114">Project References</span></span>

<span data-ttu-id="5feeb-115">此範例可作為 Windows Forms 或 Windows Presentation Foundation 應用程式。</span><span class="sxs-lookup"><span data-stu-id="5feeb-115">The sample is available as a Windows Forms or Windows Presentation Foundation application.</span></span> <span data-ttu-id="5feeb-116">Windows Forms 版本參考：</span><span class="sxs-lookup"><span data-stu-id="5feeb-116">The Windows Forms version references:</span></span>

-   <span data-ttu-id="5feeb-117">Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="5feeb-117">Microsoft.Ink.dll</span></span>
-   <span data-ttu-id="5feeb-118">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="5feeb-118">Microsoft.Ink.Analysis.dll</span></span>

<span data-ttu-id="5feeb-119">除了核心 Windows Presentation Foundation dll 之外，Windows Presentation Foundation 版本參考 IAWinFX.dll。</span><span class="sxs-lookup"><span data-stu-id="5feeb-119">The Windows Presentation Foundation version references IAWinFX.dll in addition to the core Windows Presentation Foundation dlls.</span></span>

> [!Note]  
> <span data-ttu-id="5feeb-120">此範例的 Windows Presentation Foundation 版本 (可在 XAML 目錄中找到) 必須在系統上安裝 Microsoft Visual Studio 2005 的 Windows Presentation Foundation 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="5feeb-120">The Windows Presentation Foundation version of this sample (found in the XAML directory) requires that the Windows Presentation Foundation extensions for Microsoft Visual Studio 2005 is installed on the system.</span></span>

 

## <a name="user-interface"></a><span data-ttu-id="5feeb-121">使用者介面</span><span class="sxs-lookup"><span data-stu-id="5feeb-121">User Interface</span></span>

<span data-ttu-id="5feeb-122">此應用程式的 UI 是由具有兩個相關聯之[TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1)物件的[TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1)所組成：筆墨表單和轉換的文字形式。</span><span class="sxs-lookup"><span data-stu-id="5feeb-122">The UI for this application consists of a [TabControl](/dotnet/api/system.windows.forms.tabcontrol?view=netcore-3.1) with two [TabPage](/dotnet/api/system.windows.forms.tabpage?view=netcore-3.1) objects associated with it: Ink Form and Converted Text Form.</span></span> <span data-ttu-id="5feeb-123">[筆跡表單] 索引標籤包含</span><span class="sxs-lookup"><span data-stu-id="5feeb-123">The Ink Form tab contains</span></span>

-   <span data-ttu-id="5feeb-124">面板，其中包含用來取得電話郵件的掃描紙張表單影像。</span><span class="sxs-lookup"><span data-stu-id="5feeb-124">A panel that contains an image of a scanned paper form used for taking telephone messages.</span></span>
-   <span data-ttu-id="5feeb-125">當選取時，具有應用程式的核取方塊會顯示分析提示界限。</span><span class="sxs-lookup"><span data-stu-id="5feeb-125">A check box that has the application show the analysis hint bounds when selected.</span></span>
-   <span data-ttu-id="5feeb-126">一組按鈕、清除和分析，會從表單中清除筆墨，並將筆墨分析初始化。</span><span class="sxs-lookup"><span data-stu-id="5feeb-126">A pair of buttons, Clear and Analyze, that clear the ink from the form and initialize ink analysis.</span></span>

<span data-ttu-id="5feeb-127">轉換過的文字形式包含相同的影像，而是應用程式顯示已辨識文字的頁面。</span><span class="sxs-lookup"><span data-stu-id="5feeb-127">The Converted Text Form contains the same image and is the page on which the application displays the recognized text.</span></span> <span data-ttu-id="5feeb-128">當您按一下 [分析] 時，應用程式會以同步方式執行筆墨分析，而辨識結果會出現在 [已轉換的文字格式] 索引標籤上</span><span class="sxs-lookup"><span data-stu-id="5feeb-128">When you click Analyze, the application performs ink analysis synchronously, and the recognition results appear on the Converted Text Form tab.</span></span>

## <a name="functionality"></a><span data-ttu-id="5feeb-129">功能</span><span class="sxs-lookup"><span data-stu-id="5feeb-129">Functionality</span></span>

<span data-ttu-id="5feeb-130">此應用程式會使用 [InkOverlay](/previous-versions/ms552322(v=vs.100)) 來啟用寫入。</span><span class="sxs-lookup"><span data-stu-id="5feeb-130">This application uses an [InkOverlay](/previous-versions/ms552322(v=vs.100)) to enable writing.</span></span> <span data-ttu-id="5feeb-131">InkOverlay 物件非常適合用於拍攝和基本 scribbling。</span><span class="sxs-lookup"><span data-stu-id="5feeb-131">The InkOverlay object is well suited for note taking and basic scribbling.</span></span> <span data-ttu-id="5feeb-132">這個物件的主要用途是將筆墨顯示為筆跡。</span><span class="sxs-lookup"><span data-stu-id="5feeb-132">The primary intended use of this object is to display ink as ink.</span></span> <span data-ttu-id="5feeb-133">筆跡分析的主要類別是 [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) 類別。</span><span class="sxs-lookup"><span data-stu-id="5feeb-133">The main class for ink analysis is the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class.</span></span> <span data-ttu-id="5feeb-134">當您呼叫 InkAnalyzer 物件的 [分析](/previous-versions/ms568971(v=vs.100)) 方法時，筆墨分析會以同步方式進行。</span><span class="sxs-lookup"><span data-stu-id="5feeb-134">When you call the InkAnalyzer object's [Analyze](/previous-versions/ms568971(v=vs.100)) method, the ink analysis occurs synchronously.</span></span>

<span data-ttu-id="5feeb-135">應用程式會初始化兩個數組，一個字串和一個矩形。</span><span class="sxs-lookup"><span data-stu-id="5feeb-135">The application initializes two arrays, one of strings and one of rectangles.</span></span> <span data-ttu-id="5feeb-136">字串陣列 `factoidStrings` 是由以[AnalysisHintNode](/previous-versions/ms573018(v=vs.100))物件的形式傳遞至[InkAnalyzer](/previous-versions/ms583671(v=vs.100))中的[智慧](/previous-versions/ms583657(v=vs.100))標記物件所組成。</span><span class="sxs-lookup"><span data-stu-id="5feeb-136">The string array, `factoidStrings`, is made of [Factoid](/previous-versions/ms583657(v=vs.100)) objects that are passed into the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) as [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) objects.</span></span> <span data-ttu-id="5feeb-137">AnalysisHintNode 物件會針對特定輸入偏差 InkAnalyzer。</span><span class="sxs-lookup"><span data-stu-id="5feeb-137">The AnalysisHintNode objects bias the InkAnalyzer toward particular input.</span></span> <span data-ttu-id="5feeb-138">此範例會使用日期、時間和電話提示，以及其他部分。</span><span class="sxs-lookup"><span data-stu-id="5feeb-138">This sample uses the date, time, and telephone hints, as well as some others.</span></span>

<span data-ttu-id="5feeb-139">每個 [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) 都與表單的特定區域相關聯。</span><span class="sxs-lookup"><span data-stu-id="5feeb-139">Each [AnalysisHintNode](/previous-versions/ms573018(v=vs.100)) is associated with a specific area of the form.</span></span> <span data-ttu-id="5feeb-140">這些區域會以矩形的陣列表示 `rects` 。</span><span class="sxs-lookup"><span data-stu-id="5feeb-140">The areas are represented by the array of rectangles, `rects`.</span></span> <span data-ttu-id="5feeb-141">藉由為每個矩形建立 [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) ，此範例會將已辨識的文字輸出到正確的位置。</span><span class="sxs-lookup"><span data-stu-id="5feeb-141">By creating a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) for each rectangle, the sample outputs the recognized text in the correct location.</span></span>


```C++
        private void InitHints()
        {
            // Instantiate the collection of TextBoxes.
            this.textBoxes = new ArrayList();

            // For each Rectangle in Rectangles
            for (int i = 0; i < rects.Length; i++)
            {

                Rectangle rectangle = rects[i];

                // Create an AnalysisHintNode with the bounds of the Rectangle.  The bounds
                // of an AnalysisHintNode gives clues to the handwriting recognizer about
                // the way Strokes are grouped together.
                AnalysisHintNode hint = this.analyzer.CreateAnalysisHint(rectangle);

                // Set the corresponding Factoid on the AnalysisHintNode.  This gives the 
                // recognizer clues about the meaning of the strokes within the 
                // AnalysisHintNode's region.
                hint.Factoid = factoidStrings[i];

                // Create a corresponding TextBox where the results of the analysis
                // associated with this AnalysisHintNode will be displayed.  Store the reference
                // to the TextBox in the textBoxes Collection.
                this.textBoxes.Add(InitTextBox(hint));
            }
        }
```



<span data-ttu-id="5feeb-142">之後，只要建立事件處理常式，在使用者按一下 [分析] 時，就會觸發筆墨分析。</span><span class="sxs-lookup"><span data-stu-id="5feeb-142">After that, it is merely a matter of creating an event handler that triggers the ink analysis when the user clicks Analyze.</span></span>


```C++
        private void UpdateTextBoxes()
        {
            // Get the AnalysisHintNodes that we previously added to the InkAnalyzer.
            ContextNodeCollection hints = this.analyzer.GetAnalysisHints();

            for (int i = 0; i < hints.Count; i++)
            {
                // Get the recognized string from the AnalysisHintNode
                string analyzedString = ((AnalysisHintNode)hints[i]).GetRecognizedString();

                // If we found a string, set the contents of the TextBox
                // to that string.
                if (analyzedString != null)
                {
                    ((TextBox)this.textBoxes[i]).Text = analyzedString;
                }
            }
        }
```



 

 
