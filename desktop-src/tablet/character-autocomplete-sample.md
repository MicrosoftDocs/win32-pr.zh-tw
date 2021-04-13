---
description: 自動完成範例示範如何使用 (Api) 的辨識應用程式開發介面，以日文執行字元自動完成。
ms.assetid: 237e33bc-3708-4128-8749-d3d031f7237a
title: 字元自動完成範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4853cdef72a087aff3b9b726f0c83af9038ef5bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510761"
---
# <a name="character-autocomplete-sample"></a><span data-ttu-id="73c67-103">字元自動完成範例</span><span class="sxs-lookup"><span data-stu-id="73c67-103">Character Autocomplete Sample</span></span>

<span data-ttu-id="73c67-104">自動完成範例示範如何使用 (Api) 的辨識應用程式開發介面，以日文執行字元自動完成。</span><span class="sxs-lookup"><span data-stu-id="73c67-104">The Autocomplete sample demonstrates how to implement character Autocomplete in Japanese by using the recognition application programming interfaces (APIs).</span></span>

<span data-ttu-id="73c67-105">此範例使用下列功能：</span><span class="sxs-lookup"><span data-stu-id="73c67-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="73c67-106">使用 *筆墨收集器*</span><span class="sxs-lookup"><span data-stu-id="73c67-106">Using an *ink collector*</span></span>
-   <span data-ttu-id="73c67-107">使用辨識 *器內容*</span><span class="sxs-lookup"><span data-stu-id="73c67-107">Using a *recognizer context*</span></span>

## <a name="initializing-the-ink-collector-and-recognizer-context"></a><span data-ttu-id="73c67-108">初始化筆墨收集器和辨識器內容</span><span class="sxs-lookup"><span data-stu-id="73c67-108">Initializing the Ink Collector and Recognizer Context</span></span>

<span data-ttu-id="73c67-109">[**InkCollector**](inkcollector-class.md)和 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件會宣告為可引發事件的類別。</span><span class="sxs-lookup"><span data-stu-id="73c67-109">The [**InkCollector**](inkcollector-class.md) and [**InkRecognizerContext**](inkrecognizercontext-class.md) objects are declared as classes that can raise events.</span></span>


```C++
Dim WithEvents ic As InkCollector
Dim WithEvents rc As InkRecognizerContext
```



<span data-ttu-id="73c67-110">表單的 Load 事件處理常式會建立筆墨收集器、將筆墨收集器關聯至圖片方塊，以及啟用筆墨收集。</span><span class="sxs-lookup"><span data-stu-id="73c67-110">The form's Load event handler creates an ink collector, associates the ink collector to picture box, and enables ink collection.</span></span> <span data-ttu-id="73c67-111">接著，事件處理常式會載入預設的日文辨識器，並初始化辨識器內容的指南和筆觸屬性。</span><span class="sxs-lookup"><span data-stu-id="73c67-111">The event handler then loads the default Japanese recognizer, and initializes the recognizer context 's Guide and Strokes properties.</span></span>


```C++
Private Sub Form_Load()
   ' Set the ink collector to work in the small frame window
    Set ic = New InkCollector    ic.hWnd = fraBox.hWnd    ic.Enabled = True
    
    ' Get the Japanese recognizer
    LoadRecognizer

    ' Initialize the recognizer context
    Dim Guide As New InkRecognizerGuide
    Dim FrameRectangle As New InkRectangle
    Dim Top As Long
    Dim Bottom As Long
    Dim Left As Long
    Dim Right As Long
    Top = 0
    Left = 0
    Bottom = fraBox.ScaleHeight
    Right = fraBox.ScaleWidth
    ic.Renderer.PixelToInkSpace Me.hdc, Top, Left
    ic.Renderer.PixelToInkSpace Me.hdc, Bottom, Right
    FrameRectangle.Bottom = Bottom
    FrameRectangle.Top = Top
    FrameRectangle.Left = Left
    FrameRectangle.Right = Right
    Guide.Columns = 1
    Guide.Rows = 1
    Guide.Midline = -1 ' Do not use midline
    Guide.DrawnBox = FrameRectangle
    Guide.WritingBox = FrameRectangle
    Set rc.Guide = Guide
    
    ' Set the strokes collection on the recognizer context
    Set ink = ic.ink    Set rc.Strokes = ic.ink.Strokes
End Sub
```



## <a name="loading-the-default-japanese-recognizer"></a><span data-ttu-id="73c67-112">載入預設日文辨識器</span><span class="sxs-lookup"><span data-stu-id="73c67-112">Loading the Default Japanese Recognizer</span></span>

<span data-ttu-id="73c67-113">呼叫 [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85))的 [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer)方法，以取得日文語言的預設辨識器。</span><span class="sxs-lookup"><span data-stu-id="73c67-113">The [**GetDefaultRecognizer**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizers-getdefaultrecognizer) method of the [**InkRecognizers**](/previous-versions/windows/desktop/legacy/ms702438(v=vs.85)) is called to retrieve the default recognizer for the Japanese language.</span></span> <span data-ttu-id="73c67-114">接下來，會檢查 IInkRecognizer 物件的 [ [**語言**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) ] 屬性，以判斷辨識器是否支援日文語言。</span><span class="sxs-lookup"><span data-stu-id="73c67-114">Next, the IInkRecognizer object's [**Languages**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-get_languages) property is checked to determine if the recognizer supports the Japanese language.</span></span> <span data-ttu-id="73c67-115">如果有，則會使用辨識器的 [**CreateRecognizerCoNtext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) 方法來產生表單的辨識器內容。</span><span class="sxs-lookup"><span data-stu-id="73c67-115">If it does, then the recognizer's [**CreateRecognizerContext**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizer-createrecognizercontext) method is used to generate a recognizer context for the form.</span></span>


```C++
Private Sub LoadRecognizer()
    On Error GoTo NoRecognizer
    ' Get a Japanese recognizer context
    Dim recos As New InkRecognizers
    Dim JapaneseReco As IInkRecognizer
    Set JapaneseReco = recos.GetDefaultRecognizer(&H411)
    If JapaneseReco Is Nothing Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    
    ' Check that this is indeed a Japanese recognizer
    Dim IsJapanese As Boolean
    Dim lan As Integer
    IsJapanese = False
    For lan = LBound(JapaneseReco.Languages) To UBound(JapaneseReco.Languages)
        If JapaneseReco.Languages(lan) = &H411 Then
            IsJapanese = True
        End If
    Next lan
    If Not IsJapanese Then
        MsgBox "Japanese Recognizers are not installed on this system. Exiting."
        End
    End If
    Set rc = JapaneseReco.CreateRecognizerContext
    Exit Sub
NoRecognizer:
    MsgBox "Japanese Recognizers are not installed on this system. Exiting."
    End
End Sub
```



## <a name="handling-the-stroke-event"></a><span data-ttu-id="73c67-116">處理筆觸事件</span><span class="sxs-lookup"><span data-stu-id="73c67-116">Handling the Stroke Event</span></span>

<span data-ttu-id="73c67-117">[**筆劃**](inkcollector-stroke.md)事件處理常式會先在辨識器內容上停止背景辨識。</span><span class="sxs-lookup"><span data-stu-id="73c67-117">The [**Stroke**](inkcollector-stroke.md) event handler first halts background recognition on the recognizer context.</span></span> <span data-ttu-id="73c67-118">然後，它會將新的筆劃新增至辨識器內容的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) 屬性。</span><span class="sxs-lookup"><span data-stu-id="73c67-118">Then, it adds the new stroke to the recognizer context's [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property.</span></span> <span data-ttu-id="73c67-119">最後，它會設定辨識器內容的 [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) 屬性，並針對三個字元自動完成模式中的每一個，呼叫辨識器內容的 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) 方法。</span><span class="sxs-lookup"><span data-stu-id="73c67-119">Finally, it sets the recognizer context's [**InkRecognizerCharacterAutoCompletionMode**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognizercharacterautocompletionmode) property and calls the recognizer context's [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method for each of the three character Autocomplete modes.</span></span> <span data-ttu-id="73c67-120">**BackgroundRecognizeWithAlternates** 方法呼叫的 *CustomData* 參數是用來識別 [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md)事件中所傳回的辨識結果。</span><span class="sxs-lookup"><span data-stu-id="73c67-120">The *CustomData* parameter of the **BackgroundRecognizeWithAlternates** method call is used to identify which recognition results are returned in the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event.</span></span>


```C++
Private Sub ic_Stroke(ByVal Cursor As MSINKAUTLib.IInkCursor, ByVal Stroke As MSINKAUTLib.IInkStrokeDisp, Cancel As Boolean)

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' Add the new stroke
    rc.Strokes.Add Stroke

    ' Get a result for all three CAC modes
    rc.CharacterAutoCompletionMode = IRCACM_Full rc.BackgroundRecognizeWithAlternates 0 rc.CharacterAutoCompletionMode = IRCACM_Prefix rc.BackgroundRecognizeWithAlternates 1 rc.CharacterAutoCompletionMode = IRCACM_Random rc.BackgroundRecognizeWithAlternates 2
End Sub
```



## <a name="handling-the-recognition-with-alternates-event"></a><span data-ttu-id="73c67-121">使用替代事件處理辨識</span><span class="sxs-lookup"><span data-stu-id="73c67-121">Handling the Recognition with Alternates Event</span></span>

<span data-ttu-id="73c67-122">[**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md)事件的處理常式會先檢查 *RecognitionStatus* 參數。</span><span class="sxs-lookup"><span data-stu-id="73c67-122">The handler for the [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) event first checks the *RecognitionStatus* parameter.</span></span> <span data-ttu-id="73c67-123">如果辨識錯誤，事件處理常式會忽略辨識結果。</span><span class="sxs-lookup"><span data-stu-id="73c67-123">If there is an error in recognition, the event handler ignores the recognition results.</span></span> <span data-ttu-id="73c67-124">否則，事件處理常式會將 *RecognitionResult* 參數加入至適當的圖片方塊，並儲存結果字串。</span><span class="sxs-lookup"><span data-stu-id="73c67-124">Otherwise, the event handler adds the *RecognitionResult* parameter to the appropriate picture box and saves the result string.</span></span> <span data-ttu-id="73c67-125">*CustomData* 參數會在 [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates)方法的呼叫中設定，並識別辨識器內容所使用的字元自動完成模式。</span><span class="sxs-lookup"><span data-stu-id="73c67-125">The *CustomData* parameter is set in the call to the [**BackgroundRecognizeWithAlternates**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-backgroundrecognizewithalternates) method and identifies which character Autocomplete mode was used by the recognizer context.</span></span>


```C++
Private Sub rc_RecognitionWithAlternates(ByVal RecognitionResult As MSINKAUTLib.IInkRecognitionResult, ByVal vCustomParam As Variant, ByVal RecognitionStatus As MSINKAUTLib.InkRecognitionStatus)
    ' Get the alternates from the recognition result
    ' and display them in the right place
    Dim ResultString As String
    Dim alts As IInkRecognitionAlternates
    Dim alt As IInkRecognitionAlternate
        
    On Error GoTo EndFunc

    If RecognitionStatus = IRS_NoError Then
        ' Fill a string with all the characters for this CAC mode
        Set alts = RecognitionResult.AlternatesFromSelection
        For Each alt In alts
            ResultString = ResultString + alt.String
        Next alt
        ' Display the string
        Dim r As RECT
        r.Left = 0
        r.Top = 0
        r.Right = 1000
        r.Bottom = 1000
        PctResult(vCustomParam).Cls
        DrawText PctResult(vCustomParam).hdc, StrPtr(ResultString), Len(ResultString), r, 0
        If vCustomParam = 0 Then
            FullCACText = ResultString
        Else
            If vCustomParam = 1 Then
                PrefixCACText = ResultString
            Else
                If vCustomParam = 2 Then
                    RandomCACText = ResultString
                End If
            End If
        End If
    End If
    Exit Sub
EndFunc:
    MsgBox Err.Description
End Sub
```



## <a name="painting-the-form"></a><span data-ttu-id="73c67-126">繪製表單</span><span class="sxs-lookup"><span data-stu-id="73c67-126">Painting the Form</span></span>

<span data-ttu-id="73c67-127">油漆事件處理常式會清除結果圖片方塊，並將儲存的辨識結果新增至其中。</span><span class="sxs-lookup"><span data-stu-id="73c67-127">The Paint event handler clears the results picture boxes and adds the saved recognition results to them.</span></span>

## <a name="deleting-the-strokes"></a><span data-ttu-id="73c67-128">刪除筆劃</span><span class="sxs-lookup"><span data-stu-id="73c67-128">Deleting the Strokes</span></span>

<span data-ttu-id="73c67-129">表單的 `CmdClear_Click` 方法會處理 Clear 命令。</span><span class="sxs-lookup"><span data-stu-id="73c67-129">The form's `CmdClear_Click` method handles the Clear command.</span></span> <span data-ttu-id="73c67-130">如果 [**InkCollector**](inkcollector-class.md) 目前正在收集筆跡，則會顯示訊息方塊，並忽略命令。</span><span class="sxs-lookup"><span data-stu-id="73c67-130">If the [**InkCollector**](inkcollector-class.md) is currently collecting ink, then a message box is displayed and the command is ignored.</span></span> <span data-ttu-id="73c67-131">否則，事件處理常式會停止背景識別、清除辨識器內容的 [**筆觸**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) 屬性，並從表單的 [**InkDisp**](inkdisp-class.md) 物件刪除筆觸。</span><span class="sxs-lookup"><span data-stu-id="73c67-131">Otherwise, the event handler stops background recognition, clears the [**Strokes**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-get_strokes) property of the recognizer context, and deletes the strokes from the form's [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="73c67-132">然後，事件處理常式會重繪筆墨收集器所關聯的圖片方塊，並清除辨識字串和圖片方塊。</span><span class="sxs-lookup"><span data-stu-id="73c67-132">Then, the event handler redraws the picture box to which the ink collector is associated, and clears the recognition strings and picture boxes.</span></span>


```C++
If Not (ic.CollectingInk) Then

    ' Stop the unfinished recognition processes
    rc.StopBackgroundRecognition

    ' ...
    Set rc.Strokes = Nothing

    ' Delete all the strokes from the ink object
    ic.Ink.DeleteStrokes strokesToDelete

    ' Refresh the window
    fraBox.Refresh

    ' refresh the recognizer context
    Set rc.Strokes = ic.Ink.Strokes

    ' Clear the result strings
    FullCACText = ""
    PrefixCACText = ""
    RandomCACText = ""

    ' Clear the result windows
    PctResult(0).Cls
    PctResult(1).Cls
    PctResult(2).Cls

Else
    MsgBox "Cannot clear ink while the ink collector is busy."
End If
```



 

 
