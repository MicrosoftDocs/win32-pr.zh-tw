---
description: 這個範例示範如何建立啟用筆墨的控制項，以在網頁瀏覽器中使用。 此範例會採用原始的自動宣告表單範例，並將它轉換成放在網頁上的控制項。
ms.assetid: 7a9e304c-57ef-41a3-83be-2b2d31435da8
title: 筆墨 Web 控制項範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 101537c4cc7b42181cf8d9ff177a5854c5b84054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970983"
---
# <a name="ink-web-control-sample"></a><span data-ttu-id="86800-104">筆墨 Web 控制項範例</span><span class="sxs-lookup"><span data-stu-id="86800-104">Ink Web Control Sample</span></span>

<span data-ttu-id="86800-105">這個範例示範如何建立啟用筆墨的控制項，以在網頁瀏覽器中使用。</span><span class="sxs-lookup"><span data-stu-id="86800-105">This sample shows how to create an ink-enabled control for use in a Web browser.</span></span> <span data-ttu-id="86800-106">此範例會採用原始的 [自動宣告表單範例](auto-claims-form-sample.md) ，並將它轉換成放在網頁上的控制項。</span><span class="sxs-lookup"><span data-stu-id="86800-106">The sample takes the original [Auto Claims Form Sample](auto-claims-form-sample.md) and turns it into a control that is put on a Web page.</span></span>

<span data-ttu-id="86800-107">如需在 Web 上使用筆墨的詳細資訊，請參閱 [網路上的筆跡](ink-on-the-web.md)。</span><span class="sxs-lookup"><span data-stu-id="86800-107">For more information about using ink on the Web, see [Ink on the Web](ink-on-the-web.md).</span></span>

## <a name="modifications-to-the-original-sample-project"></a><span data-ttu-id="86800-108">原始範例專案的修改</span><span class="sxs-lookup"><span data-stu-id="86800-108">Modifications to the Original Sample Project</span></span>

<span data-ttu-id="86800-109">此範例包含包含兩個專案和一個 HTML 檔案的方案。</span><span class="sxs-lookup"><span data-stu-id="86800-109">This sample consists of a solution that includes two projects and an HTML file.</span></span> <span data-ttu-id="86800-110">第一個專案 AutoClaims 是 Microsoft Visual C \# 控制項程式庫專案， (使用者控制項) 。</span><span class="sxs-lookup"><span data-stu-id="86800-110">The first project, AutoClaims, is a Microsoft Visual C\# Control Library project (a User Control).</span></span> <span data-ttu-id="86800-111">此控制項的原始程式碼與 AutoClaims 範例的原始程式碼幾乎完全相同，但有兩項差異：</span><span class="sxs-lookup"><span data-stu-id="86800-111">The source code for this control is almost identical to that of the AutoClaims sample with two differences:</span></span>

-   <span data-ttu-id="86800-112">`AutoClaims`此範例中的類別繼承自[UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1)類別，而不是[Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1)類別。</span><span class="sxs-lookup"><span data-stu-id="86800-112">The `AutoClaims` class in this sample inherits from the [UserControl](/dotnet/api/system.windows.forms.usercontrol?view=netcore-3.1) class rather than the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class.</span></span>

    ```C++
    public class AutoClaims : System.Windows.Forms.UserControl 
    ```

    

-   <span data-ttu-id="86800-113">此範例中的 AutoClaims 類別具有新增的公用方法， `DisposeResources` 可處置用來收集筆墨的內部子控制項。</span><span class="sxs-lookup"><span data-stu-id="86800-113">The AutoClaims Class in this sample has an added public method, `DisposeResources` that disposes of the internal child controls used for collecting ink.</span></span> <span data-ttu-id="86800-114">當使用控制項完成該頁面時，thewebpageon 會使用此方法來呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="86800-114">This method must be called by thewebpageon which the control is used when that page is finished using the control.</span></span>

## <a name="referencing-the-control-in-html"></a><span data-ttu-id="86800-115">以 HTML 參考控制項</span><span class="sxs-lookup"><span data-stu-id="86800-115">Referencing the Control in HTML</span></span>

<span data-ttu-id="86800-116">解決方案包含 HTML 檔案 default.htm。</span><span class="sxs-lookup"><span data-stu-id="86800-116">The solution includes an HTML file, default.htm.</span></span> <span data-ttu-id="86800-117">此檔案是瀏覽器導覽的頁面，以便載入控制項。</span><span class="sxs-lookup"><span data-stu-id="86800-117">This file is the page that the browser navigates to in order to load the control.</span></span> <span data-ttu-id="86800-118">檔案包含 <object> 參考控制項的標記。</span><span class="sxs-lookup"><span data-stu-id="86800-118">The file contains an <object> tag that references the control.</span></span> <span data-ttu-id="86800-119">它也包含在頁面卸載時所呼叫的腳本，如中的 onload = "" 屬性是否存在。 `OnUnload()`</span><span class="sxs-lookup"><span data-stu-id="86800-119">It also includes a script that is called when the page unloads, as indicated by the presence of the onload=" `OnUnload()` " attribute in the</span></span> <body> <span data-ttu-id="86800-120">的相片或視訊。</span><span class="sxs-lookup"><span data-stu-id="86800-120">tag.</span></span> <span data-ttu-id="86800-121">此函式 `DisposeResources` 會在控制項上呼叫方法，以確保所有資源在關機時都能正確地釋放。</span><span class="sxs-lookup"><span data-stu-id="86800-121">This function calls the `DisposeResources` method on the control to make sure that all resources are properly released at shutdown.</span></span>


```C++
<html>
    <script language="jscript">
        // Release any resources held by the AutoClaims control
        function OnUnload()
        {
            autoClaimsControl.DisposeResources();
        }
    </script>
    <head>
        <title>AutoClaims (Web Control)</title>
    </head>
    <body onunload="OnUnload()">
        <object 
          id="autoClaimsControl" 
          classid="AutoClaims.dll#AutoClaims.AutoClaims">
        </object>
    </body>
</html> 
```



<span data-ttu-id="86800-122">請注意標記之 classid 屬性值的格式 <object> 。</span><span class="sxs-lookup"><span data-stu-id="86800-122">Notice the format of the classid attribute value for the <object> tag.</span></span> <span data-ttu-id="86800-123">它會將元件命名為，後面接著 \# 符號分隔符號，然後是包含控制項的命名空間，然後是控制項的類別名稱。</span><span class="sxs-lookup"><span data-stu-id="86800-123">It names the assembly, followed with a \# sign separator, and then the namespace that contains the control and then the class name of the control.</span></span>

<span data-ttu-id="86800-124">實際的使用者控制項可能包含用來保存或傳送在應用程式中收集之資料的其他方法。</span><span class="sxs-lookup"><span data-stu-id="86800-124">A real-world user control would likely include additional methods used to persist or send the data collected in the application.</span></span>

## <a name="the-autoclaims_webcontrol-project"></a><span data-ttu-id="86800-125">AutoClaims \_ WebControl 專案</span><span class="sxs-lookup"><span data-stu-id="86800-125">The AutoClaims\_WebControl Project</span></span>

<span data-ttu-id="86800-126">AutoClaims \_ WebControl 專案是部署專案，它會建立一個安裝程式，在安裝時將虛擬根目錄（AutoClaims \_ WebControl）新增至 Web 服務器。</span><span class="sxs-lookup"><span data-stu-id="86800-126">The AutoClaims\_WebControl project is a Deployment Project that creates a setup that adds a virtual root, AutoClaims\_WebControl, on the Web server when installed.</span></span> <span data-ttu-id="86800-127">控制項和 HTML 檔案都會放在這個虛擬根目錄中。</span><span class="sxs-lookup"><span data-stu-id="86800-127">The control and the HTML file are placed in this virtual root.</span></span>

> [!Note]  
> <span data-ttu-id="86800-128">SDK 的預設安裝選項不會安裝已編譯的 web 範例。</span><span class="sxs-lookup"><span data-stu-id="86800-128">The compiled web samples are not installed by the default installation option for the SDK.</span></span> <span data-ttu-id="86800-129">您必須完成自訂安裝，然後選取 [預先編譯的 Web 範例] 子選項來進行安裝。</span><span class="sxs-lookup"><span data-stu-id="86800-129">You must complete a custom installation and select the "Pre-compiled Web Samples" sub-option to install them.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="86800-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="86800-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86800-131">自動宣告表單範例</span><span class="sxs-lookup"><span data-stu-id="86800-131">Auto Claims Form Sample</span></span>](auto-claims-form-sample.md)
</dt> <dt>

[<span data-ttu-id="86800-132">Web 上的筆墨</span><span class="sxs-lookup"><span data-stu-id="86800-132">Ink on the Web</span></span>](ink-on-the-web.md)
</dt> </dl>

 

 
