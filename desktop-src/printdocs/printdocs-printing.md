---
description: Windows 為應用程式提供一組完整的功能，讓您可以列印至各種裝置，例如雷射印表機、向量繪圖器、點陣印表機和傳真電腦。
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: '列印 (檔和列印) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974509"
---
# <a name="printing-documents-and-printing"></a><span data-ttu-id="64ab1-103">列印 (檔和列印) </span><span class="sxs-lookup"><span data-stu-id="64ab1-103">Printing (Documents and Printing)</span></span>

<span data-ttu-id="64ab1-104">Windows 為應用程式提供一組完整的功能，讓您可以列印至各種裝置，例如雷射印表機、向量繪圖器、點陣印表機和傳真電腦。</span><span class="sxs-lookup"><span data-stu-id="64ab1-104">Windows provides applications with a complete set of functions that allow printing to various devices, such as laser printers, vector plotters, raster printers, and fax machines.</span></span>

## <a name="desktop-app-printing"></a><span data-ttu-id="64ab1-105">桌面應用程式列印</span><span class="sxs-lookup"><span data-stu-id="64ab1-105">Desktop App Printing</span></span>

<span data-ttu-id="64ab1-106">Windows 程式設計人員可以從數種不同的技術中進行選取，以從應用程式進行列印。</span><span class="sxs-lookup"><span data-stu-id="64ab1-106">Windows programmers can select from several different technologies to print from their application.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64ab1-107">技術</span><span class="sxs-lookup"><span data-stu-id="64ab1-107">Technology</span></span></th>
<th><span data-ttu-id="64ab1-108">描述</span><span class="sxs-lookup"><span data-stu-id="64ab1-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="64ab1-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案套件 API</a></span><span class="sxs-lookup"><span data-stu-id="64ab1-109"><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a></span></span><br/></td>
<td><span data-ttu-id="64ab1-110">提供可讓應用程式存取和管理列印檔案封裝的介面。</span><span class="sxs-lookup"><span data-stu-id="64ab1-110">Provides an interface that allows an application to access and manage the print document package.</span></span> <span data-ttu-id="64ab1-111">此 API 適用于 Windows 8 和更新版本的 Windows。</span><span class="sxs-lookup"><span data-stu-id="64ab1-111">This API is available with Windows 8 and later versions of Windows.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64ab1-112"><a href="print-spooler-api.md">列印多工緩衝處理器 API</a></span><span class="sxs-lookup"><span data-stu-id="64ab1-112"><a href="print-spooler-api.md">Print Spooler API</a></span></span><br/></td>
<td><span data-ttu-id="64ab1-113">提供列印多工緩衝處理器的介面，讓應用程式可以管理印表機和列印工作。</span><span class="sxs-lookup"><span data-stu-id="64ab1-113">Provides an interface to the print spooler so that applications can manage printers and print jobs.</span></span><br/> <span data-ttu-id="64ab1-114">應用程式會使用「列印 <a href="print-spooler-api.md">幕後處理</a> 程式」 api 來啟動、停止、控制及設定列印多工緩衝處理器所管理的列印工作，不論它們是使用 <a href="/windows/desktop/printdocs/tailored-app-printing-api">列印檔案封裝 Api</a> 或 <a href="gdi-printing.md">GDI 列印 API</a> 來列印內容。</span><span class="sxs-lookup"><span data-stu-id="64ab1-114">Applications use the <a href="print-spooler-api.md">Print Spooler API</a> to start, stop, control, and configure print jobs managed by the print spooler whether they use the <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a> or the <a href="gdi-printing.md">GDI Print API</a> to print the content.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="64ab1-115"><a href="print-ticket-api.md">列印票證 API</a></span><span class="sxs-lookup"><span data-stu-id="64ab1-115"><a href="print-ticket-api.md">Print Ticket API</a></span></span><br/></td>
<td><span data-ttu-id="64ab1-116">為應用程式提供管理和轉換列印票證的功能。</span><span class="sxs-lookup"><span data-stu-id="64ab1-116">Provides applications with functions to manage and convert print tickets.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="64ab1-117"><a href="gdi-printing.md">GDI 列印 API</a></span><span class="sxs-lookup"><span data-stu-id="64ab1-117"><a href="gdi-printing.md">GDI Print API</a></span></span><br/></td>
<td><span data-ttu-id="64ab1-118">提供應用程式與裝置無關的列印介面。</span><span class="sxs-lookup"><span data-stu-id="64ab1-118">Provides applications with a device-independent printing interface.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="64ab1-119">針對 Windows Vista 和更新版本的 Windows 撰寫應用程式的開發人員，應該考慮在應用程式中使用 <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS 檔 API</a> 。</span><span class="sxs-lookup"><span data-stu-id="64ab1-119">Developers who are writing applications for Windows Vista and later versions of Windows should consider using the <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a> in their application.</span></span>
</blockquote>
<br/> <span data-ttu-id="64ab1-120"><a href="gdi-printing.md">GDI 列印 API</a>適用于必須在 windows XP 和較早版本的 windows 上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="64ab1-120">The <a href="gdi-printing.md">GDI Print API</a> is suitable for applications that must run on Windows XP and earlier versions of Windows.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="64ab1-121">下圖提供不同列印 Api 相關方式的高階觀點。</span><span class="sxs-lookup"><span data-stu-id="64ab1-121">The following illustration provides a high-level view of how the different printing APIs are related.</span></span>

![顯示原生 windows 應用程式如何使用列印 api 的圖表](images/print-apis.png)

 

<span data-ttu-id="64ab1-123">本節中的 [列印檔案套件 API](./tailored-app-printing-api.md)會說明您可以搭配 Windows 8 和更新版本的 Windows desktop 使用的列印檔案套件和預覽列印介面。</span><span class="sxs-lookup"><span data-stu-id="64ab1-123">The [Print Document Package API](./tailored-app-printing-api.md)s in this section describe the print document package and print preview interfaces that you can use with Windows 8 and later versions of Windows desktop.</span></span>

<span data-ttu-id="64ab1-124">如需從以 JavaScript 和 HTML 撰寫的 Windows Store 應用程式進行列印的詳細資訊，請參閱 [使用 javascript 和 html) 列印 (Windows store 應用程式 ](/previous-versions/windows/apps/hh465225(v=win.10))。</span><span class="sxs-lookup"><span data-stu-id="64ab1-124">For more info about printing from Windows Store apps that are written in JavaScript and HTML, see [Printing (Windows Store apps using JavaScript and HTML)](/previous-versions/windows/apps/hh465225(v=win.10)).</span></span> <span data-ttu-id="64ab1-125">如需從以 c #、Microsoft Visual Basic 或 c + + 和 XAML 撰寫的 Windows Store 應用程式進行列印的詳細資訊，請參閱 [使用 c) 列印 (Windows store 應用程式 ](/previous-versions/windows/apps/hh465196(v=win.10))。</span><span class="sxs-lookup"><span data-stu-id="64ab1-125">For more info about printing from Windows Store apps that are written in C#, Microsoft Visual Basic, or C++ and XAML, see [Printing (Windows Store apps using C)](/previous-versions/windows/apps/hh465196(v=win.10)).</span></span>

> [!Note]  
> <span data-ttu-id="64ab1-126">如需可在 Windows Store 應用程式中使用的桌面應用程式列印 Api 清單，請參閱 [適用于 Windows store 應用程式的 Win32 和 COM (列印和檔) ](/uwp/win32-and-com/win32-and-com-for-uwp-apps) 。</span><span class="sxs-lookup"><span data-stu-id="64ab1-126">See [Win32 and COM for Windows Store apps (printing and documents)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) for the list of the Desktop App Printing APIs that can also be used in Windows Store apps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="64ab1-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="64ab1-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="64ab1-128">[XPS 檔 API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="64ab1-128">[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="64ab1-129">雙向列印機通訊 (硬體開發人員中心) </span><span class="sxs-lookup"><span data-stu-id="64ab1-129">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

