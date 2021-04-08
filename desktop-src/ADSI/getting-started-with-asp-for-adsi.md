---
title: 使用 ASP for ADSI 開始使用
description: ADSI 可以用來存取使用 ASP 頁面的目錄資料。 這可能是從網頁執行系統管理工作和查詢，或是將資訊提供給內部網路上的員工的便利方式。
ms.assetid: 2007257c-6c4e-415e-9ab5-e65d8d9e5dd4
ms.tgt_platform: multiple
keywords:
- ASP ADSI
- ADSI、ASP 頁面
- ADSI、ASP Pages、ASP Code 範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff5b18093c3817d7a6c3d0224b722f8dd4983c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671147"
---
# <a name="getting-started-with-asp-for-adsi"></a><span data-ttu-id="f7e1e-107">使用 ASP for ADSI 開始使用</span><span class="sxs-lookup"><span data-stu-id="f7e1e-107">Getting Started with ASP for ADSI</span></span>

<span data-ttu-id="f7e1e-108">ADSI 可以用來存取使用 ASP 頁面的目錄資料。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-108">ADSI can be used to access directory data using an ASP page.</span></span> <span data-ttu-id="f7e1e-109">這可能是從網頁執行系統管理工作和查詢，或是將資訊提供給內部網路上的員工的便利方式。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-109">This can be a convenient way to run administration tasks and queries from a webpage or provide information to employees on an intranet.</span></span>

<span data-ttu-id="f7e1e-110">使用 ADSI 搭配 ASP 的優點之一，是您可以建立更豐富的使用者經驗，因為您可以使用 Visual Basic 來建立 ADSI 應用程式，並透過標準網頁將它提供給使用者。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-110">One advantage of using ADSI with ASP is that you can create a richer user experience because you can use Visual Basic to create an ADSI application and offer it to a user through a standard webpage.</span></span> <span data-ttu-id="f7e1e-111">例如，您可以建立一個網頁，讓員工輸入員工的姓氏，然後取回該員工的電話號碼，或建立一個表單，讓員工更新公司人力資源資料庫中的個人資訊。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-111">For example, you could create a webpage that enables employees to enter the last name of an employee and get back a phone number for that employee, or create a form that allows employees to update personal information in a company human resources database.</span></span>

<span data-ttu-id="f7e1e-112">ASP 程式碼的開頭為 ' <% '，結尾為 '% > '。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-112">ASP code starts with '<%' and ends with '%>'.</span></span> <span data-ttu-id="f7e1e-113">您可以將 ADSI 程式碼加入 VBScript 或 Visual Basic。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-113">You can add ADSI code as VBScript or Visual Basic.</span></span>

<span data-ttu-id="f7e1e-114">若要建立 ASP 頁面，您可以使用網頁編輯器、記事本或其他文字編輯器，或 Microsoft Visual Studio .NET 程式開發系統。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-114">To create an ASP page, you can use a webpage editor, Notepad or other text editor, or the Microsoft Visual Studio .NET development system.</span></span>

<span data-ttu-id="f7e1e-115">執行 ASP 頁面之前，請根據 [ADSI 與 ASP 驗證問題](authentication-issues-for-adsi-with-asp.md)中的指示，設定您的應用程式或 IIS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-115">Before you run your ASP page, set up your application or IIS server according to the instructions found in [Authentication Issues for ADSI with ASP](authentication-issues-for-adsi-with-asp.md).</span></span>

## <a name="a-simple-asp-sample-enumerating-objects-in-a-container"></a><span data-ttu-id="f7e1e-116">簡單的 ASP 範例：列舉容器中的物件</span><span class="sxs-lookup"><span data-stu-id="f7e1e-116">A Simple ASP Sample: Enumerating Objects in a Container</span></span>

<span data-ttu-id="f7e1e-117">使用網頁編輯器建立新的 html 網頁，以接受容器物件的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-117">Using a webpage editor, create a new html page which accepts the distinguished name of a container object.</span></span> <span data-ttu-id="f7e1e-118">輸入下列程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-118">Enter the following code example.</span></span>


```HTML
<html>
<body>

<form method="POST" action="https://localhost/Enum.asp" ID="Form1">
<p>Distinguished name of container:<input type="text" name="inpContainer" size="100" ID="Text2"></p>
<p><input type="SUBMIT" value="GO" ID="Submit1" NAME="Submit1"></p>
</form>

</body>
</html>
```



<span data-ttu-id="f7e1e-119">此頁面現在可接受傳遞給它的容器名稱，並使用 ADSI 來列舉容器中的物件。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-119">This page can now accept a container name that is passed to it and use ADSI to enumerate objects in the container.</span></span>

<span data-ttu-id="f7e1e-120">建立新的 ASP 頁面，稱為列舉 .asp，然後輸入下列程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-120">Create a new ASP page called Enum.asp and enter the following code example.</span></span> <span data-ttu-id="f7e1e-121">將此頁面儲存在本機網頁伺服器的根目錄。</span><span class="sxs-lookup"><span data-stu-id="f7e1e-121">Save this page at the root of the local web server.</span></span>


```VB
<%@ Language=VBScript %>
<%
' Get the inputs.
containerName = Request.Form("inpContainer")
' Validate compName before using.

If Not ("" = containerName) Then
  ' Bind to the object.
  adsPath = "LDAP://" & containerName
  Set comp = GetObject(adsPath)

  ' Write the ADsPath of each of the child objects.
  Response.Write("<p>Enumeration:</p>")
  For Each obj in comp
    Response.Write(obj.ADsPath + "<BR>")
  Next
End If
%>
```



 

 




