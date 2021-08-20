---
description: 筆墨 Blog 範例應用程式示範如何建立具有筆墨功能的 managed UserControl 類別，並在 Microsoft Internet Explorer 中控制控制項。
ms.assetid: b6c3ad92-3ab1-4311-b318-13939e1a1a5a
title: 筆墨 Blog Web 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8796a05861d278015205b5ba0d3775e2e47af6a57ce1fee426c5c0c5011dacd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032356"
---
# <a name="ink-blog-web-sample"></a>筆墨 Blog Web 範例

筆墨 Blog 範例應用程式示範如何建立具有筆墨功能的 managed [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) 類別，並在 Microsoft Internet Explorer 中控制控制項。 此範例也示範一種技術，可使用 HTTP 和在伺服器上保存筆墨來傳送資料到網路上。

> [!Note]  
> 您必須有 Microsoft Internet Information Services (IIS) 安裝 ASP.NET，才能執行此範例。 請確定您的電腦符合 ASP.NET 應用程式在電腦上執行所需的需求。

 

> [!Note]  
> 如果您在已安裝 Microsoft Windows XP Tablet pc Edition 開發工具組1.7 的非平板電腦電腦上執行此範例，則筆墨標題的文字辨識功能將無法運作。 發生這種情況是因為安裝 Tablet PC SDK 1.7 的非 Tablet PC 電腦缺少辨識器。 應用程式的其餘部分會依照所述的方式執行。

 

## <a name="overview"></a>概觀

筆墨 Blog 範例會建立啟用筆墨的網路日誌。 InkBlogWeb 是 ASP.NET 的應用程式。 筆墨專案是透過 ASP.NET 網頁所參考的使用者控制項來完成。

使用者控制項會偵測是否已在用戶端電腦上安裝 Tablet PC 平臺元件。 如果是這樣，使用者控制項會在網頁上為使用者提供兩個啟用筆墨的區域：一個用來為 blog 專案的標題加上筆跡，另一個則是專案的主體。 如果未安裝 Tablet PC 平臺元件，則會為使用者提供專案標題和主體的標準文字方塊控制項。

當使用者完成專案的建立時，她按一下按鈕、加入 Blog，然後將 post 傳送至 Web 服務器以進行儲存。 在伺服器上，應用程式會儲存標題文字和張貼日期，以及圖形交換格式 (GIF) 檔的參考。 GIF 檔案也儲存在伺服器中，包含嚴加防禦 GIF 檔案內文的筆墨資料。 如需嚴加防禦 GIF 格式的詳細資訊，請參閱將 [筆墨儲存為 HTML](storing-ink-in-html.md)。

InkBlog 方案中有兩個專案： **InkBlogControls** 專案和 **InkBlogWeb** 專案。

## <a name="inkblogcontrols-project"></a>InkBlogControls Project

**InkBlogControls** 專案是 [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)專案，其中包含使用者控制項的程式碼，可在網頁上啟用筆跡。 此控制項的程式碼（InkArea 控制項）位於 InkArea .cs 檔案中。

`InkArea`類別繼承自[UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)類別。 控制項的函式會 `InkArea` 呼叫 helper 方法 `CreateInkCollectionSurface` 。


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



`CreateInkCollectionSurface`方法會嘗試建立[InkCollector](/previous-versions/ms583683(v=vs.100))類別的實例，以判斷是否可以在用戶端上使用 Tablet PC 筆跡元件。 如果 `CreateInkCollectionSurface` 方法呼叫成功，則方法會傳回 [Panel](/dotnet/api/system.windows.forms.panel?view=netcore-3.1) 物件做為控制項。


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



如果因為找不到筆墨平臺檔案而導致函式失敗，則 `InputArea` 控制項會將控制項具現化為 [TextBox](/dotnet/api/system.windows.forms.textbox?view=netcore-3.1) 控制項，而不是 [InkCollector](/previous-versions/ms583683(v=vs.100)) 控制項。 然後，此函式會將控制項的大小調整為父使用者控制項的大小，並將它加入父系的控制項集合。

InkArea 控制項類別會執行三個有趣的公用屬性： InkData、TextData 和 WebEnabled。

如果用戶端支援筆墨，InkData 屬性會是唯讀的，並提供對序列化筆墨資料的存取。 如果用戶端不支援筆跡，InkData 屬性會取得空字串。 InkData 屬性會呼叫 helper 方法（SerializeInkData），以判斷用戶端是否支援手寫。


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



在 `SerializeInkData` 方法中，取得[Ink](/previous-versions/ms583670(v=vs.100))物件時需要轉換為[InkCollector](/previous-versions/ms583683(v=vs.100)) ，因為 `inputArea` 已宣告為[控制項](/dotnet/api/system.windows.forms.control?view=netcore-3.1)。 如果筆跡物件包含任何筆劃，則會使用 PersistenceFormat 列舉值) ，將筆墨資料儲存在 `inkDataBytes` 位元組陣列中，做[](/previous-versions/ms552503(v=vs.100))為 GIF (指定。 方法接著會將位元組陣列轉換為 Base64 編碼的字串，並傳回這個字串。

假設用戶端可以執行辨識，則屬性會傳回 `TextData` [RecognitionResult](/previous-versions/ms552537(v=vs.100)) 物件，使其無法將筆墨資料傳遞給手寫辨識器。 如果用戶端不是筆墨感知，則會傳回文字方塊內容，如下列程式碼所示。


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



`TextData`屬性會呼叫 helper 方法（如 `RecognizeInkData` 下列程式碼所示）來執行辨識。 當系統上有辨識引擎時，方法會傳回 `RecognizeInkData` 包含 [RecognitionResult](/previous-versions/ms552537(v=vs.100)) 物件之 [TopString](/previous-versions/ms572009(v=vs.100)) 屬性的字串。 否則將傳回空字串。


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



`InkEnabled`屬性是唯讀的布林值，指出用戶端電腦是否支援筆跡。

Control 類別的另一個重要 public 成員 `InkArea` 是 `DisposeResources` 方法。 這個方法會在內部呼叫 `Dispose` 方法，以確保會清除使用者控制項所利用的所有資源。 使用控制項的任何應用程式都 `InkArea` 必須在 `DisposeResources` 完成使用控制項時呼叫方法。

## <a name="inkblogweb-project"></a>InkBlogWeb Project

InkBlogWeb 專案是 Web 安裝程式的部署專案，它會參考 `InkArea` 控制項以提供博客功能。 如需有關 Web 安裝程式部署專案的詳細資訊，請參閱[Web 安裝程式的部署 Project](https://msdn.microsoft.com/library/k8kzx145(v=VS.71).aspx)。

有兩個 .aspx 檔案可執行「日誌」範例： default.aspx 和 AddBlog .aspx。 預設的 .aspx 是 InkBlogWeb 應用程式的預設頁面。 此頁面的程式碼後置於檔案為 default.aspx。 此頁面提供包含新的 blog 專案表單之頁面的連結，並顯示任何現有的 blog 專案。 這項程式稍後會在下列新的 blog 專案表單頁面 AddBlog 之後描述。

AddBlog .aspx 及其程式碼後端檔案（AddBlog .aspx）包含用來建立新的 blog 專案的邏輯和使用者介面程式碼。 AddBlox 會使用 HTML 物件專案，參考 InkBlogControls 專案中建立之 InkArea 控制項類別的兩個實例，如下列範例所示。 一個實例有 `id` inkBlogTitle 的屬性，另一個實例具有 inkBlogBody 的 id 屬性。

`<OBJECT id="inkBlogTitle" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="48" VIEWASTEXT>``</OBJECT>``<br/>``<OBJECT id="inkBlogBody" classid="InkBlogControls.dll#InkBlog.InkArea" width="400" height="296" VIEWASTEXT>``</OBJECT>`

InkBlogControls.dll 的元件必須存在於參考該元件的 .aspx 頁面所在的目錄中。 Web 安裝程式部署專案可確保發生這種情況，因為部署 Project 中的「主要輸出來源 InkBlogControls」專案證明。

標題控制項只會有48圖元的高度，以方便輸入標題的一行筆跡。 內文控制項的高度為296圖元，可騰出空間給多行或繪圖的大型 blog 專案。

InkArea 控制項會透過標準 HTML 按鈕元素的 onclick 事件處理常式，連接到用戶端腳本函式 AddBlog。

`<button id="BUTTON1" type="button" onclick="AddBlog()">Add Blog</button>`

頁面上也有包含三個隱藏輸入元素的 HTML 表單： BlogTitleText、BlogBodyText 和 BlogBodyInkData。 此表單用來將 blog 專案資料張貼回伺服器。 AddBlog 是針對表單定義的後端處理常式。

AddBlog 函式是以 Microsoft 撰寫 JScript <entity type="reg"/> -將 InkArea 控制項中的 blog 資料解壓縮，並將結果張貼至伺服器。


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



當資料抵達伺服器時，AddBlog 中的程式碼會檢查頁面 \_ 載入事件處理常式，以查看 HttpRequest 物件的表單內容是否包含任何資料。 若是如此，它會根據目前的系統時間建立檔案名、將表單資料放入三個字串變數中，然後將資料寫出至 HTML 檔案和包含筆墨資料的 GIF 檔案（如果有的話），如下列程式碼所示。


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



如需 helper 方法的詳細資訊，請參閱範例原始程式碼。

## <a name="running-the-sample"></a>執行範例

Tablet PC SDK 1.7 預設會安裝 Ink Blog Web 範例。 若要執行範例，請在 Internet Explorer 中，流覽至 https://localhost/TabletPCSDK\_WebSamples/InkBlogWeb/Default.aspx 。 如果您正在執行 Windows Server 2003，請以您的電腦名稱稱取代 "localhost"。

> [!Note]  
> SDK 的預設安裝選項不會安裝已編譯的 web 範例。 您必須完成自訂安裝，然後選取 [預先編譯的 Web 範例] 子選項來進行安裝。

 

您也可以在 Microsoft Visual Studio .net 中開啟並建立專案，然後將 <entity type="reg"/> 它部署到執行 IIS 的另一部電腦，藉以執行此範例。

## <a name="troubleshooting-the-sample"></a>範例疑難排解

執行或裝載範例時，可能會造成困難的三個區域是許可權和辨識。

### <a name="permissions"></a>權限

此範例需要嘗試建立新的 blog 專案之帳戶的虛擬根資料夾內的寫入權限。 根據預設，Tablet PC SDK 1.7 中提供的範例編譯版本已設定正確的許可權，以符合此需求。

如果您使用提供的 Web 安裝部署專案來建立和部署範例，您必須為% MACHINENAME% \\ Users 群組授與 InkBlogWeb 虛擬 (根目錄所指向之檔系統資料夾的寫入權限，例如 C： \\ InetPub \\ WWWRoot \\ InkBlogWeb) 。 Users 群組包含 IIS 使用的匿名帳戶，因此可讓 ASP.NET 應用程式將新的 blog 專案寫入檔案系統。 替代方法是移除虛擬根目錄的匿名存取，並強制執行驗證。

### <a name="recognition"></a>辨識

必須安裝手寫辨識器，才能辨識 blog 標題中的筆跡。 如果您從 Windows XP Tablet pc Edition 以外的作業系統存取 InkBlog 應用程式，但安裝 Tablet pc SDK 1.7，您可以在 InkArea 控制項中撰寫筆墨，但辨識引擎不會出現，而且您的 blog 專案將不會顯示任何標題。 不過，主體中的筆墨內容仍然會出現。

### <a name="machine-configuration"></a>電腦設定

如果您已在電腦上安裝 ASP.NET 和 .NET Framework，然後卸載並重新安裝 IIS，則腳本對應將會中斷，而且 ASP.NET 將無法運作。 如果發生這種情況，您可以使用 ASP.NET IIS 註冊工具 (Aspnet \_regiis.exe-i) 來修復 ASP.NET 腳本對應。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[InkCollector](/previous-versions/ms583683(v=vs.100))
</dt> <dt>

[Web 上的筆墨](ink-on-the-web.md)
</dt> <dt>

[筆墨資料格式](ink-data-formats.md)
</dt> <dt>

[系統。Windows。Forms/UserControl 類別](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)
</dt> </dl>

 

 
