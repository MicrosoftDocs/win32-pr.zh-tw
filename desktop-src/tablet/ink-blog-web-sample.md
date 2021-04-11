---
description: 筆墨 Blog 範例應用程式示範如何建立具有筆墨功能的 managed UserControl 類別，並在 Microsoft Internet Explorer 中控制控制項。
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: 筆墨 Blog Web 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24f132d355a95c9cb8debebe074df3f976e3b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112320"
---
# <a name="ink-blog-web-sample"></a><span data-ttu-id="549cd-103">筆墨 Blog Web 範例</span><span class="sxs-lookup"><span data-stu-id="549cd-103">Ink Blog Web Sample</span></span>

<span data-ttu-id="549cd-104">筆墨 Blog 範例應用程式示範如何建立具有筆墨功能的 managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) 類別，並在 Microsoft Internet Explorer 中控制控制項。</span><span class="sxs-lookup"><span data-stu-id="549cd-104">The Ink Blog sample application demonstrates how to create a managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class that has inking capability and host that control in Microsoft Internet Explorer.</span></span> <span data-ttu-id="549cd-105">此範例也示範一種技術，可使用 HTTP 和在伺服器上保存筆墨來傳送資料到網路上。</span><span class="sxs-lookup"><span data-stu-id="549cd-105">The sample also demonstrates one technique for sending ink data across a network by using HTTP and for persisting ink on a server.</span></span>

> [!Note]  
> <span data-ttu-id="549cd-106">您必須有 Microsoft Internet Information Services (IIS) 安裝 ASP.NET，才能執行此範例。</span><span class="sxs-lookup"><span data-stu-id="549cd-106">You must have Microsoft Internet Information Services (IIS) with ASP.NET installed to run this sample.</span></span> <span data-ttu-id="549cd-107">請確定您的電腦符合 ASP.NET 應用程式在電腦上執行所需的需求。</span><span class="sxs-lookup"><span data-stu-id="549cd-107">Make sure that your computer meets the requirements necessary for ASP.NET applications to run on your computer.</span></span>

 

> [!Note]  
> <span data-ttu-id="549cd-108">如果您在已安裝 Microsoft Windows XP Tablet PC Edition 開發工具組1.7 的非平板電腦電腦上執行此範例，則筆墨標題的文字辨識功能將無法運作。</span><span class="sxs-lookup"><span data-stu-id="549cd-108">If you run this sample on a non-Tablet PC computer with the Microsoft Windows XP Tablet PC Edition Development Kit 1.7 installed the text recognition feature for the ink title will not function.</span></span> <span data-ttu-id="549cd-109">發生這種情況是因為安裝 Tablet PC SDK 1.7 的非 Tablet PC 電腦缺少辨識器。</span><span class="sxs-lookup"><span data-stu-id="549cd-109">This occurs because a non-Tablet PC computer with the Tablet PC SDK 1.7 installed lacks recognizers.</span></span> <span data-ttu-id="549cd-110">應用程式的其餘部分會依照所述的方式執行。</span><span class="sxs-lookup"><span data-stu-id="549cd-110">The rest of the application performs as described.</span></span>

 

## <a name="overview"></a><span data-ttu-id="549cd-111">概觀</span><span class="sxs-lookup"><span data-stu-id="549cd-111">Overview</span></span>

<span data-ttu-id="549cd-112">筆墨 Blog 範例會建立啟用筆墨的網路日誌。</span><span class="sxs-lookup"><span data-stu-id="549cd-112">The Ink Blog sample creates an ink-enabled Weblog.</span></span> <span data-ttu-id="549cd-113">InkBlogWeb 是 ASP.NET 應用程式。</span><span class="sxs-lookup"><span data-stu-id="549cd-113">InkBlogWeb is an ASP.NET application.</span></span> <span data-ttu-id="549cd-114">筆墨專案是透過從 ASP.NET 網頁參考的使用者控制項來完成。</span><span class="sxs-lookup"><span data-stu-id="549cd-114">Ink entry is accomplished by means of a user control that is referenced from an ASP.NET page.</span></span>

<span data-ttu-id="549cd-115">使用者控制項會偵測是否已在用戶端電腦上安裝 Tablet PC 平臺元件。</span><span class="sxs-lookup"><span data-stu-id="549cd-115">The user control detects whether the Tablet PC platform components are installed on the client computer.</span></span> <span data-ttu-id="549cd-116">如果是這樣，使用者控制項會在網頁上為使用者提供兩個啟用筆墨的區域：一個用來為 blog 專案的標題加上筆跡，另一個則是專案的主體。</span><span class="sxs-lookup"><span data-stu-id="549cd-116">If so, the user control presents the user with two ink-enabled areas on the Web page: one for inking a title for the blog entry and one for the body of the entry.</span></span> <span data-ttu-id="549cd-117">如果未安裝 Tablet PC 平臺元件，則會為使用者提供專案標題和主體的標準文字方塊控制項。</span><span class="sxs-lookup"><span data-stu-id="549cd-117">If the Tablet PC Platform components are not installed, then the user is given a standard text box control for the title and body of the entry.</span></span>

<span data-ttu-id="549cd-118">當使用者完成專案的建立時，她按一下按鈕、加入 Blog，然後將 post 傳送至 Web 服務器以進行儲存。</span><span class="sxs-lookup"><span data-stu-id="549cd-118">When the user finishes creating the entry, she clicks a button, Add Blog, and the post is sent to the Web server for storage.</span></span> <span data-ttu-id="549cd-119">在伺服器上，應用程式會儲存標題文字和張貼日期，以及圖形交換格式 (GIF) 檔的參考。</span><span class="sxs-lookup"><span data-stu-id="549cd-119">On the server, the application saves the title text and posting date, as well as a reference to a Graphics Interchange Format (GIF) file.</span></span> <span data-ttu-id="549cd-120">GIF 檔案也儲存在伺服器中，包含嚴加防禦 GIF 檔案內文的筆墨資料。</span><span class="sxs-lookup"><span data-stu-id="549cd-120">The GIF file, also saved to the server, contains the ink data from the body in a fortified GIF file.</span></span> <span data-ttu-id="549cd-121">如需嚴加防禦 GIF 格式的詳細資訊，請參閱將 [筆墨儲存為 HTML](storing-ink-in-html.md)。</span><span class="sxs-lookup"><span data-stu-id="549cd-121">For more information about the fortified GIF format, see [Storing Ink in HTML](storing-ink-in-html.md).</span></span>

<span data-ttu-id="549cd-122">InkBlog 方案中有兩個專案： **InkBlogControls** 專案和 **InkBlogWeb** 專案。</span><span class="sxs-lookup"><span data-stu-id="549cd-122">There are two projects in the InkBlog solution: the **InkBlogControls** project and the **InkBlogWeb** project.</span></span>

## <a name="inkblogcontrols-project"></a><span data-ttu-id="549cd-123">InkBlogControls 專案</span><span class="sxs-lookup"><span data-stu-id="549cd-123">InkBlogControls Project</span></span>

<span data-ttu-id="549cd-124">**InkBlogControls** 專案是 [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)專案，其中包含使用者控制項的程式碼，可在網頁上啟用筆跡。</span><span class="sxs-lookup"><span data-stu-id="549cd-124">The **InkBlogControls** project is a [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) project that contains the code for the user control that enables inking on the Web page.</span></span> <span data-ttu-id="549cd-125">此控制項的程式碼（InkArea 控制項）位於 InkArea .cs 檔案中。</span><span class="sxs-lookup"><span data-stu-id="549cd-125">The code for this control, the InkArea control, is in the InkArea.cs file.</span></span>

<span data-ttu-id="549cd-126">`InkArea`類別繼承自[UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)類別。</span><span class="sxs-lookup"><span data-stu-id="549cd-126">The `InkArea` Class inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class.</span></span> <span data-ttu-id="549cd-127">控制項的函式會 `InkArea` 呼叫 helper 方法 `CreateInkCollectionSurface` 。</span><span class="sxs-lookup"><span data-stu-id="549cd-127">The constructor for the `InkArea` control calls a helper method, `CreateInkCollectionSurface`.</span></span>


```C++
public InkArea()
{
    // Standard template code

    try
    {
        inputArea = CreateInkCollectionSurface();
    }
    catch (FileNotFoundException)
    { 
        inputArea = new TextBox();
        ((TextBox)inputArea).Multiline = true;
    }

    inputArea.Size = this.Size;

    // Add the control used for collecting blog input
    this.Controls.Add(inputArea);
}
```



<span data-ttu-id="549cd-128">`CreateInkCollectionSurface`方法會嘗試建立[InkCollector](/previous-versions/ms583683(v=vs.100))類別的實例，以判斷是否可以在用戶端上使用 Tablet PC 筆跡元件。</span><span class="sxs-lookup"><span data-stu-id="549cd-128">The `CreateInkCollectionSurface` method determines whether the Tablet PC inking components are available on the client by attempting to create an instance of the [InkCollector](/previous-versions/ms583683(v=vs.100)) class.</span></span> <span data-ttu-id="549cd-129">如果 `CreateInkCollectionSurface` 方法呼叫成功，則方法會傳回 [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) 物件做為控制項。</span><span class="sxs-lookup"><span data-stu-id="549cd-129">If the call to the `CreateInkCollectionSurface` method succeeds, the method returns a [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) object as the control.</span></span>


```C++
protected Control CreateInkCollectionSurface()
{
    try
    {
        Panel inkPanel = new Panel();
        inkPanel.BorderStyle = BorderStyle.Fixed3D;
        inkCollector = new InkCollector(inkPanel);
        ((InkCollector)inkCollector).Enabled = true;
        return inkPanel;
    }
    catch
    {
        throw;
    }
}
```



<span data-ttu-id="549cd-130">如果因為找不到筆墨平臺檔案而導致函式失敗，則 `InputArea` 控制項會將控制項具現化為 [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) 控制項，而不是 [InkCollector](/previous-versions/ms583683(v=vs.100)) 控制項。</span><span class="sxs-lookup"><span data-stu-id="549cd-130">If the constructor fails because the inking platform files are not found, then the `InputArea` control is instantiated as a [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) control rather than a [InkCollector](/previous-versions/ms583683(v=vs.100)) control.</span></span> <span data-ttu-id="549cd-131">然後，此函式會將控制項的大小調整為父使用者控制項的大小，並將它加入父系的控制項集合。</span><span class="sxs-lookup"><span data-stu-id="549cd-131">The constructor then sizes the control to the size of the parent user control and adds it to the parent's Controls collection.</span></span>

<span data-ttu-id="549cd-132">InkArea 控制項類別會執行三個有趣的公用屬性： InkData、TextData 和 WebEnabled。</span><span class="sxs-lookup"><span data-stu-id="549cd-132">The InkArea control class implements three interesting public properties: InkData, TextData, and WebEnabled.</span></span>

<span data-ttu-id="549cd-133">如果用戶端支援筆墨，InkData 屬性會是唯讀的，並提供對序列化筆墨資料的存取。</span><span class="sxs-lookup"><span data-stu-id="549cd-133">The InkData property is read-only and provides access to the serialized ink data, if the client supports inking.</span></span> <span data-ttu-id="549cd-134">如果用戶端不支援筆跡，InkData 屬性會取得空字串。</span><span class="sxs-lookup"><span data-stu-id="549cd-134">If the client does not support inking, the InkData property gets an empty string.</span></span> <span data-ttu-id="549cd-135">InkData 屬性會呼叫 helper 方法（SerializeInkData），以判斷用戶端是否支援手寫。</span><span class="sxs-lookup"><span data-stu-id="549cd-135">The InkData property calls a helper method, SerializeInkData, to determine if the client supports inking.</span></span>


```C++
protected String SerializeInkData()
{
    Debug.Assert(InkEnabled, null, "Client must be ink-enabled");

    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    // Serialize the ink
    if (ink.Strokes.Count > 0) 
    {
        byte[] inkDataBytes = ink.Save(PersistenceFormat.Gif);
        return Convert.ToBase64String(inkDataBytes);
    }

    // Default to returning the empty string.
    return String.Empty;
}
```



<span data-ttu-id="549cd-136">在 `SerializeInkData` 方法中，取得[Ink](/previous-versions/ms583670(v=vs.100))物件時需要轉換為[InkCollector](/previous-versions/ms583683(v=vs.100)) ，因為 `inputArea` 已宣告為[控制項](/dotnet/api/system.windows.forms.control?view=netcore-3.1)。</span><span class="sxs-lookup"><span data-stu-id="549cd-136">In the `SerializeInkData` method, the cast to [InkCollector](/previous-versions/ms583683(v=vs.100)) is necessary when obtaining the [Ink](/previous-versions/ms583670(v=vs.100)) object, because `inputArea` is declared as a [Control](/dotnet/api/system.windows.forms.control?view=netcore-3.1).</span></span> <span data-ttu-id="549cd-137">如果筆跡物件包含任何筆劃，則會使用 PersistenceFormat 列舉值) ，將筆墨資料儲存在 `inkDataBytes` 位元組陣列中，做[](/previous-versions/ms552503(v=vs.100))為 GIF (指定。</span><span class="sxs-lookup"><span data-stu-id="549cd-137">If the Ink object contains any strokes, the ink data is saved into the `inkDataBytes` byte array as a GIF (specified by using the [PersistenceFormat](/previous-versions/ms552503(v=vs.100)) enumeration value).</span></span> <span data-ttu-id="549cd-138">方法接著會將位元組陣列轉換為 Base64 編碼的字串，並傳回這個字串。</span><span class="sxs-lookup"><span data-stu-id="549cd-138">The method then converts the byte array to a Base64-encoded string and returns this string.</span></span>

<span data-ttu-id="549cd-139">假設用戶端可以執行辨識，則屬性會傳回 `TextData` [RecognitionResult](/previous-versions/ms552537(v=vs.100)) 物件，使其無法將筆墨資料傳遞給手寫辨識器。</span><span class="sxs-lookup"><span data-stu-id="549cd-139">Assuming that the client can perform recognition, the `TextData` property returns the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object from passing the ink data to a handwriting recognizer.</span></span> <span data-ttu-id="549cd-140">如果用戶端不是筆墨感知，則會傳回文字方塊內容，如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="549cd-140">If the client is not ink-aware, the text box contents are returned, as shown in the following code.</span></span>


```C++
public string TextData
{
    get
    {
        if (this.WebEnabled) 
        {
            return RecognizeInkData();
        }
        else
        {
            return ((TextBox)inputArea).Text;
        }
    }
}
```



<span data-ttu-id="549cd-141">`TextData`屬性會呼叫 helper 方法（如 `RecognizeInkData` 下列程式碼所示）來執行辨識。</span><span class="sxs-lookup"><span data-stu-id="549cd-141">The `TextData` property calls a helper method, `RecognizeInkData`, shown in the following code, to carry out the recognition.</span></span> <span data-ttu-id="549cd-142">當系統上有辨識引擎時，方法會傳回 `RecognizeInkData` 包含 [RecognitionResult](/previous-versions/ms552537(v=vs.100)) 物件之 [TopString](/previous-versions/ms572009(v=vs.100)) 屬性的字串。</span><span class="sxs-lookup"><span data-stu-id="549cd-142">When recognition engines are present on the system, the `RecognizeInkData` method returns a string containing the [RecognitionResult](/previous-versions/ms552537(v=vs.100)) object's [TopString](/previous-versions/ms572009(v=vs.100)) property.</span></span> <span data-ttu-id="549cd-143">否則將傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="549cd-143">Otherwise, it returns an empty string.</span></span>


```C++
protected String RecognizeInkData()
{
    // Obtain the ink associated with this control
    Ink ink = ((InkCollector)inkCollector).Ink;

    if (ink.Strokes.Count > 0) 
    {

        // Attempt to create a recognition context and use it to
        // retrieve the top alternate.
        try 
        {
            RecognizerContext recognizerContext = new RecognizerContext();
            RecognitionStatus recognitionStatus;
            recognizerContext.Strokes = ink.Strokes;
            RecognitionResult recognitionResult = recognizerContext.Recognize(out recognitionStatus);
            if (recognitionStatus == RecognitionStatus.NoError) && ( null != recognitionResult) )
            {
                return recognitionResult.TopString;
            }
        }
        catch (Exception)
        {
            // An exception will occur if the client does not have
            // any handwriting recognizers installed on their system.
            // In this case, we default to returning an empty string. 
        }
    }

    return String.Empty;
}
```



<span data-ttu-id="549cd-144">`InkEnabled`屬性是唯讀的布林值，指出用戶端電腦是否支援筆跡。</span><span class="sxs-lookup"><span data-stu-id="549cd-144">The `InkEnabled` property is a read-only Boolean value that indicates whether inking is supported on the client machine.</span></span>

<span data-ttu-id="549cd-145">Control 類別的另一個重要 public 成員 `InkArea` 是 `DisposeResources` 方法。</span><span class="sxs-lookup"><span data-stu-id="549cd-145">Another important public member of the `InkArea` control class is the `DisposeResources` method.</span></span> <span data-ttu-id="549cd-146">這個方法會在內部呼叫 `Dispose` 方法，以確保會清除使用者控制項所利用的所有資源。</span><span class="sxs-lookup"><span data-stu-id="549cd-146">This method internally calls the `Dispose` method to ensure that all resources leveraged by the user control are cleaned up.</span></span> <span data-ttu-id="549cd-147">使用控制項的任何應用程式都 `InkArea` 必須在 `DisposeResources` 完成使用控制項時呼叫方法。</span><span class="sxs-lookup"><span data-stu-id="549cd-147">Any application that uses the `InkArea` control must call the `DisposeResources` method when it is finished using the control.</span></span>

## <a name="inkblogweb-project"></a><span data-ttu-id="549cd-148">InkBlogWeb 專案</span><span class="sxs-lookup"><span data-stu-id="549cd-148">InkBlogWeb Project</span></span>

<span data-ttu-id="549cd-149">InkBlogWeb 專案是 Web 安裝程式的部署專案，它會參考 `InkArea` 控制項以提供博客功能。</span><span class="sxs-lookup"><span data-stu-id="549cd-149">The InkBlogWeb project is a Web Setup deployment project that references the `InkArea` control to provide the blogging functionality.</span></span> <span data-ttu-id="549cd-150">如需有關 Web 安裝程式部署專案的詳細資訊，請參閱 [部署 Web 安裝專案](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx)。</span><span class="sxs-lookup"><span data-stu-id="549cd-150">For more information about Web Setup deployment projects, see [Deployment of a Web Setup Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx).</span></span>

<span data-ttu-id="549cd-151">有兩個 .aspx 檔案可執行「日誌」範例： default.aspx 和 AddBlog .aspx。</span><span class="sxs-lookup"><span data-stu-id="549cd-151">There are two .aspx files that implement the blogging sample: Default.aspx and AddBlog.aspx.</span></span> <span data-ttu-id="549cd-152">預設的 .aspx 是 InkBlogWeb 應用程式的預設頁面。</span><span class="sxs-lookup"><span data-stu-id="549cd-152">Default.aspx is the default page for the InkBlogWeb application.</span></span> <span data-ttu-id="549cd-153">此頁面的程式碼後置於檔案為 default.aspx。</span><span class="sxs-lookup"><span data-stu-id="549cd-153">The code behind file for this page is Default.aspx.cs.</span></span> <span data-ttu-id="549cd-154">此頁面提供包含新的 blog 專案表單之頁面的連結，並顯示任何現有的 blog 專案。</span><span class="sxs-lookup"><span data-stu-id="549cd-154">This page provides a link to the page containing the new blog entry form and displays any existing blog entries.</span></span> <span data-ttu-id="549cd-155">這項程式稍後會在下列新的 blog 專案表單頁面 AddBlog 之後描述。</span><span class="sxs-lookup"><span data-stu-id="549cd-155">This process is described later, after the following examination of the new blog entry form page, AddBlog.aspx.</span></span>

<span data-ttu-id="549cd-156">AddBlog .aspx 及其程式碼後端檔案（AddBlog .aspx）包含用來建立新的 blog 專案的邏輯和使用者介面程式碼。</span><span class="sxs-lookup"><span data-stu-id="549cd-156">AddBlog.aspx and its code-behind file, AddBlog.aspx.cs, contain the logic and user interface code for creating new blog entries.</span></span> <span data-ttu-id="549cd-157">AddBlox 會使用 HTML 物件專案，參考 InkBlogControls 專案中建立之 InkArea 控制項類別的兩個實例，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="549cd-157">AddBlox.aspx references two instances of the InkArea control class created in the InkBlogControls project by using the HTML OBJECT element as shown in the following example.</span></span> <span data-ttu-id="549cd-158">一個實例有 `id` inkBlogTitle 的屬性，另一個實例具有 inkBlogBody 的 id 屬性。</span><span class="sxs-lookup"><span data-stu-id="549cd-158">One instance has an `id` attribute of inkBlogTitle and the other has an id attribute of inkBlogBody.</span></span>

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

<span data-ttu-id="549cd-159">InkBlogControls.dll 的元件必須存在於參考該元件的 .aspx 頁面所在的目錄中。</span><span class="sxs-lookup"><span data-stu-id="549cd-159">The InkBlogControls.dll assembly must be present in the same directory as the .aspx page that is referencing it.</span></span> <span data-ttu-id="549cd-160">Web 安裝程式部署專案可確保發生這種情況，因為部署專案中的「主要輸出來自 InkBlogControls」專案證明。</span><span class="sxs-lookup"><span data-stu-id="549cd-160">The Web Setup deployment project ensures that this is the case, as evidenced by the presence of the "Primary output from InkBlogControls" item in the Deployment Project.</span></span>

<span data-ttu-id="549cd-161">標題控制項只會有48圖元的高度，以方便輸入標題的一行筆跡。</span><span class="sxs-lookup"><span data-stu-id="549cd-161">The title control is only 48 pixels high to facilitate the entry of a single line of ink for the title.</span></span> <span data-ttu-id="549cd-162">內文控制項的高度為296圖元，可騰出空間給多行或繪圖的大型 blog 專案。</span><span class="sxs-lookup"><span data-stu-id="549cd-162">The body control is 296 pixels high to make room for larger blog entries of multiple lines or perhaps drawings.</span></span>

<span data-ttu-id="549cd-163">InkArea 控制項會透過標準 HTML 按鈕元素的 onclick 事件處理常式，連接到用戶端腳本函式 AddBlog。</span><span class="sxs-lookup"><span data-stu-id="549cd-163">The InkArea controls are connected to a client-side script function, AddBlog, by means of a standard HTML BUTTON element's onclick event handler.</span></span>

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

<span data-ttu-id="549cd-164">頁面上也有包含三個隱藏輸入元素的 HTML 表單： BlogTitleText、BlogBodyText 和 BlogBodyInkData。</span><span class="sxs-lookup"><span data-stu-id="549cd-164">There is also an HTML form on the page that contains three hidden INPUT elements: BlogTitleText, BlogBodyText, and BlogBodyInkData.</span></span> <span data-ttu-id="549cd-165">此表單用來將 blog 專案資料張貼回伺服器。</span><span class="sxs-lookup"><span data-stu-id="549cd-165">This form is used to post the blog entry data back to the server.</span></span> <span data-ttu-id="549cd-166">AddBlog 是針對表單定義的後端處理常式。</span><span class="sxs-lookup"><span data-stu-id="549cd-166">AddBlog.aspx is the post-back handler defined for the form.</span></span>

<span data-ttu-id="549cd-167">AddBlog 函式是以 Microsoft JScript 撰寫的 <entity type="reg"/> -從 InkArea 控制項中解壓縮出 blog 資料，然後將結果張貼至伺服器。</span><span class="sxs-lookup"><span data-stu-id="549cd-167">The AddBlog function-written in Microsoft JScript<entity type="reg"/>-extracts the blog data from the InkArea controls and posts the results to the server.</span></span>


```C++
function AddBlog() 
{
    // Extract the blog's title data as ink and text
    form.BlogTitleText.value  = inkBlogTitle.TextData;
    
    // Extract the blog's body data as ink and text
    form.BlogBodyText.value = inkBlogBody.TextData;
    form.BlogBodyInkData.value = inkBlogBody.InkData;   

    form.submit();
}
```



<span data-ttu-id="549cd-168">當資料抵達伺服器時，AddBlog 中的程式碼會檢查頁面 \_ 載入事件處理常式，以查看 HttpRequest 物件的表單內容是否包含任何資料。</span><span class="sxs-lookup"><span data-stu-id="549cd-168">When the data arrives at the server, the code in AddBlog.aspx.cs checks the Page\_Load event handler to see if the HttpRequest object's Form property contains any data.</span></span> <span data-ttu-id="549cd-169">若是如此，它會根據目前的系統時間建立檔案名、將表單資料放入三個字串變數中，然後將資料寫出至 HTML 檔案和包含筆墨資料的 GIF 檔案（如果有的話），如下列程式碼所示。</span><span class="sxs-lookup"><span data-stu-id="549cd-169">If so, it creates a file name based on the current system time, puts the form data into three string variables and writes the data out to an HTML file and a GIF file containing the ink data, if present, as shown in the following code.</span></span>


```C++
if ( (String.Empty != inkBody) )
{           
    // Use helper method to create a GIF image file from ink data 
    CreateGif(imagePath, fileName, inkBody);
    
    // Create an HTML fragment to reference the image file
    content = "<img src=\"Blogs/Images/" + fileName + ".gif\"></img>";
}                
else 
{
    // If no ink data is available create an HTML fragment that contains
    // the blog's text directly.
    content = "<P>" + textBody + "</P>";
}

// Use helper method to create the blog web page on the server
CreateHtm(blogPath, fileName, blogTitle, content);
```



<span data-ttu-id="549cd-170">如需 helper 方法的詳細資訊，請參閱範例原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="549cd-170">For more details about the helper methods, refer to the sample source code.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="549cd-171">執行範例</span><span class="sxs-lookup"><span data-stu-id="549cd-171">Running the Sample</span></span>

<span data-ttu-id="549cd-172">Tablet PC SDK 1.7 預設會安裝 Ink Blog Web 範例。</span><span class="sxs-lookup"><span data-stu-id="549cd-172">The Tablet PC SDK 1.7 installs the Ink Blog Web sample by default.</span></span> <span data-ttu-id="549cd-173">若要執行範例，請在 Internet Explorer 中，流覽至 https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx 。</span><span class="sxs-lookup"><span data-stu-id="549cd-173">To run the sample, in Internet Explorer, navigate to https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx.</span></span> <span data-ttu-id="549cd-174">如果您執行的是 Windows Server 2003，請以您的電腦名稱稱取代 "localhost"。</span><span class="sxs-lookup"><span data-stu-id="549cd-174">If you are running Windows Server 2003, substitute your computer name for "localhost".</span></span>

> [!Note]  
> <span data-ttu-id="549cd-175">SDK 的預設安裝選項不會安裝已編譯的 web 範例。</span><span class="sxs-lookup"><span data-stu-id="549cd-175">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="549cd-176">您必須完成自訂安裝，然後選取 [預先編譯的 Web 範例] 子選項來進行安裝。</span><span class="sxs-lookup"><span data-stu-id="549cd-176">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

<span data-ttu-id="549cd-177">您也可以在 Microsoft Visual Studio .Net 中開啟並建立專案，然後將 <entity type="reg"/> 它部署到執行 IIS 的另一部電腦，藉以執行此範例。</span><span class="sxs-lookup"><span data-stu-id="549cd-177">You can also run the sample by opening and building the project in Microsoft Visual Studio<entity type="reg"/> .NET and then deploying it to a separate computer running IIS.</span></span>

## <a name="troubleshooting-the-sample"></a><span data-ttu-id="549cd-178">範例疑難排解</span><span class="sxs-lookup"><span data-stu-id="549cd-178">Troubleshooting the Sample</span></span>

<span data-ttu-id="549cd-179">執行或裝載範例時，可能會造成困難的三個區域是許可權和辨識。</span><span class="sxs-lookup"><span data-stu-id="549cd-179">Three areas that may cause difficulty when running or hosting the sample are permissions and recognition.</span></span>

### <a name="permissions"></a><span data-ttu-id="549cd-180">權限</span><span class="sxs-lookup"><span data-stu-id="549cd-180">Permissions</span></span>

<span data-ttu-id="549cd-181">此範例需要嘗試建立新的 blog 專案之帳戶的虛擬根資料夾內的寫入權限。</span><span class="sxs-lookup"><span data-stu-id="549cd-181">The sample requires write permissions within the virtual root folder for the account that is attempting to create a new blog entry.</span></span> <span data-ttu-id="549cd-182">根據預設，Tablet PC SDK 1.7 中提供的範例編譯版本已設定正確的許可權，以符合此需求。</span><span class="sxs-lookup"><span data-stu-id="549cd-182">By default, the compiled version of the sample provided in the Tablet PC SDK 1.7 has the correct permissions set to meet this requirement.</span></span>

<span data-ttu-id="549cd-183">如果您使用提供的 Web 安裝部署專案來建立和部署範例，您必須為% MACHINENAME% \\ Users 群組授與 InkBlogWeb 虛擬 (根目錄所指向之檔系統資料夾的寫入權限，例如 C： \\ InetPub \\ WWWRoot \\ InkBlogWeb) 。</span><span class="sxs-lookup"><span data-stu-id="549cd-183">If you build and deploy the sample by using the provided Web Setup deployment project, you must give the %MACHINENAME%\\Users group write-access to the file system folder pointed to by the InkBlogWeb virtual root (for example, C:\\InetPub\\WWWRoot\\InkBlogWeb).</span></span> <span data-ttu-id="549cd-184">Users 群組包含 IIS 使用的匿名帳戶，因此可讓 ASP.NET 應用程式將新的 blog 專案寫入檔案系統。</span><span class="sxs-lookup"><span data-stu-id="549cd-184">The Users group includes the Anonymous account used by IIS, thus allowing the ASP.NET application to write the new blog entries to the file system.</span></span> <span data-ttu-id="549cd-185">替代方法是移除虛擬根目錄的匿名存取，並強制執行驗證。</span><span class="sxs-lookup"><span data-stu-id="549cd-185">An alternative is to remove anonymous access to the virtual root and force authentication.</span></span>

### <a name="recognition"></a><span data-ttu-id="549cd-186">辨識</span><span class="sxs-lookup"><span data-stu-id="549cd-186">Recognition</span></span>

<span data-ttu-id="549cd-187">必須安裝手寫辨識器，才能辨識 blog 標題中的筆跡。</span><span class="sxs-lookup"><span data-stu-id="549cd-187">The handwriting recognizers must be installed in order to recognize the ink in the title of the blog.</span></span> <span data-ttu-id="549cd-188">如果您從 Windows XP Tablet PC Edition 以外的作業系統存取 InkBlog 應用程式，但安裝 Tablet PC SDK 1.7，您可以在 InkArea 控制項中撰寫筆墨，但辨識引擎不會出現，而且您的 blog 專案將不會顯示任何標題。</span><span class="sxs-lookup"><span data-stu-id="549cd-188">If you access the InkBlog application from a computer with an operating system other than Windows XP Tablet PC Edition but with the Tablet PC SDK 1.7 installed, you can write in ink in the InkArea controls, but the recognition engines will not be present and no titles will appear for your blog entries.</span></span> <span data-ttu-id="549cd-189">不過，主體中的筆墨內容仍然會出現。</span><span class="sxs-lookup"><span data-stu-id="549cd-189">The ink content in the body still appears, though.</span></span>

### <a name="machine-configuration"></a><span data-ttu-id="549cd-190">電腦設定</span><span class="sxs-lookup"><span data-stu-id="549cd-190">Machine Configuration</span></span>

<span data-ttu-id="549cd-191">如果您已在電腦上安裝 ASP.NET 和 .NET Framework，然後卸載並重新安裝 IIS，則腳本對應將會中斷，而且 ASP.NET 將無法運作。</span><span class="sxs-lookup"><span data-stu-id="549cd-191">If you have installed ASP.NET and the .NET Framework on a computer and you then uninstall and reinstall IIS, the script maps will break and ASP.NET will not work.</span></span> <span data-ttu-id="549cd-192">如果發生這種情況，您可以使用 ASP.NET IIS 註冊工具 (Aspnet \_regiis.exe-i) 來修復 ASP.NET 腳本對應。</span><span class="sxs-lookup"><span data-stu-id="549cd-192">If this happens, you can repair the ASP.NET script maps with the ASP.NET IIS Registration tool (Aspnet\_regiis.exe -i).</span></span>

## <a name="related-topics"></a><span data-ttu-id="549cd-193">相關主題</span><span class="sxs-lookup"><span data-stu-id="549cd-193">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="549cd-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="549cd-194">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="549cd-195">Web 上的筆墨</span><span class="sxs-lookup"><span data-stu-id="549cd-195">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> <dt>

[<span data-ttu-id="549cd-196">筆墨資料格式</span><span class="sxs-lookup"><span data-stu-id="549cd-196">Ink Data Formats</span></span>](ink-data-formats.md)
</dt> <dt>

[<span data-ttu-id="549cd-197">System.object 類類別</span><span class="sxs-lookup"><span data-stu-id="549cd-197">System.Windows.Forms.UserControl Class</span></span>](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
