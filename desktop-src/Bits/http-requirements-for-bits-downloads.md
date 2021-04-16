---
title: BITS 下載的 HTTP 需求
description: BITS 支援 HTTP 和 HTTPS 下載和上傳，而且需要伺服器支援 HTTP/1.1 通訊協定。
ms.assetid: 35af422b-62e4-41fd-8890-579ccf016c83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d130ab3e527b62f34f48e6df4695bf75f63dcd2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462069"
---
# <a name="http-requirements-for-bits-downloads"></a><span data-ttu-id="9681c-103">BITS 下載的 HTTP 需求</span><span class="sxs-lookup"><span data-stu-id="9681c-103">HTTP Requirements for BITS Downloads</span></span>

<span data-ttu-id="9681c-104">BITS 支援 HTTP 和 HTTPS 下載和上傳，而且需要伺服器支援 HTTP/1.1 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="9681c-104">BITS supports HTTP and HTTPS downloads and uploads and requires that the server supports the HTTP/1.1 protocol.</span></span> <span data-ttu-id="9681c-105">針對下載，HTTP 伺服器的 **Head** 方法必須傳回檔案大小，而其 **Get** 方法必須支援內容約制和內容長度的標頭。</span><span class="sxs-lookup"><span data-stu-id="9681c-105">For downloads, the HTTP server's **Head** method must return the file size and its **Get** method must support the Content-Range and Content-Length headers.</span></span> <span data-ttu-id="9681c-106">如此一來，BITS 只會傳送靜態檔案內容，並在您嘗試傳輸動態內容時產生錯誤，除非 ASP、ISAPI 或 CGI 腳本支援內容約制和內容長度的標頭。</span><span class="sxs-lookup"><span data-stu-id="9681c-106">As a result, BITS only transfers static file content and generates an error if you try to transfer dynamic content, unless the ASP, ISAPI, or CGI script supports the Content-Range and Content-Length headers.</span></span>

<span data-ttu-id="9681c-107">只要 BITS 符合 **Head** 和 **Get** 方法的需求，就可以使用 HTTP/1.0 伺服器。</span><span class="sxs-lookup"><span data-stu-id="9681c-107">BITS can use an HTTP/1.0 server as long as it meets the **Head** and **Get** method requirements.</span></span>

<span data-ttu-id="9681c-108">為了支援下載檔案範圍，伺服器必須支援下列需求：</span><span class="sxs-lookup"><span data-stu-id="9681c-108">To support downloading ranges of a file, the server must support the following requirements:</span></span>

-   <span data-ttu-id="9681c-109">允許 MIME 標頭包含標準內容約制和內容類型的標頭，以及最多180個位元組的其他標頭。</span><span class="sxs-lookup"><span data-stu-id="9681c-109">Allow MIME headers to include the standard Content-Range and Content-Type headers, plus a maximum of 180 bytes of other headers.</span></span>
-   <span data-ttu-id="9681c-110">在 HTTP 標頭與第一個界限字串之間，最多可有兩個 CR/LFs。</span><span class="sxs-lookup"><span data-stu-id="9681c-110">Allow a maximum of two CR/LFs between the HTTP headers and the first boundary string.</span></span>

 

 




