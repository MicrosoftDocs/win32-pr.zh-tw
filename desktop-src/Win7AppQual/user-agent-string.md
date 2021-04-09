---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: 使用者代理程式字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945485"
---
# <a name="user-agent-string"></a><span data-ttu-id="f7b4e-103">使用者代理程式字串</span><span class="sxs-lookup"><span data-stu-id="f7b4e-103">User Agent String</span></span>

<span data-ttu-id="f7b4e-104">*使用者代理程式字串* 包含瀏覽器身分識別的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-104">The *User Agent String* contains information about a browser's identity.</span></span> <span data-ttu-id="f7b4e-105">每次瀏覽器對 web 伺服器提出要求時，使用者代理字串會以 HTTP 標頭的形式回報給 web 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-105">The User Agent String is reported to the web server as an HTTP header every time that a browser makes a request to a web server.</span></span> <span data-ttu-id="f7b4e-106">您也可以透過用戶端腳本來存取它。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-106">You can also access it through a client-side script.</span></span> <span data-ttu-id="f7b4e-107">例如，您可以在 Windows Internet Explorer 8 的 [位址列] 中輸入下列 URL 來顯示使用者代理字串： "javascript： alert (userAgent) "。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-107">For example, you can display the User Agent String by typing the following URL into the Windows Internet Explorer 8 address bar: "javascript:alert(navigator.userAgent)".</span></span> <span data-ttu-id="f7b4e-108">下圖顯示在 Windows 7 上執行 Internet Explorer 8 的一般結果對話方塊。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-108">The following illustration shows the typical resulting dialog box from Internet Explorer 8 running on Windows 7.</span></span>

![具有使用者代理程式字串之 internet explorer diaog 方塊的螢幕擷取畫面](images/useragent-alert.png)

<span data-ttu-id="f7b4e-110">一般而言，會特別針對 MSIE 子字串剖析使用者代理字串。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-110">Typically, the User Agent String is parsed specifically for the MSIE substring.</span></span> <span data-ttu-id="f7b4e-111">根據報告的瀏覽器版本，用戶端或伺服器端程式設計邏輯會採取不同的動作。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-111">Based on the reported version of the browser, the client-side or server-side programming logic takes a different action.</span></span> <span data-ttu-id="f7b4e-112">如需有關使用者代理程式字串的詳細資訊，請參閱 MSDN Library 中的 [Windows Internet Explorer 會如何報告為 User-Agent 字串？](/previous-versions/cc817582(v=msdn.10)) 。</span><span class="sxs-lookup"><span data-stu-id="f7b4e-112">For more information about the User Agent String, see [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in the MSDN Library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f7b4e-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="f7b4e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7b4e-114">使用相容性檢視修正 Web 應用程式中的相容性問題</span><span class="sxs-lookup"><span data-stu-id="f7b4e-114">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



