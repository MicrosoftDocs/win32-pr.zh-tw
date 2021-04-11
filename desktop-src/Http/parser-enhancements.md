---
title: 剖析器增強功能
description: 剖析器增強功能
ms.assetid: b520aebe-9182-4e60-9111-49af09cdbd79
keywords:
- 剖析器增強功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a22f4b4dced29e25662a6fc521057a055b56f70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372373"
---
# <a name="parser-enhancements"></a><span data-ttu-id="8cca5-104">剖析器增強功能</span><span class="sxs-lookup"><span data-stu-id="8cca5-104">Parser Enhancements</span></span>

<span data-ttu-id="8cca5-105">在 Windows Server 2003 （含 Service Pack 1） (SP1) 中，HTTP 伺服器 API 允許來自 HTTP 用戶端的下列要求。</span><span class="sxs-lookup"><span data-stu-id="8cca5-105">In Windows Server 2003 with Service Pack 1 (SP1), the HTTP Server API allows the following requests from HTTP clients.</span></span>

-   <span data-ttu-id="8cca5-106">使用單行換行 (LF) 為行結束字元的要求。</span><span class="sxs-lookup"><span data-stu-id="8cca5-106">Requests that use a single Line Feed (LF) as line terminators.</span></span>
-   <span data-ttu-id="8cca5-107">包含線性泛空白字元的要求 (LWS 在 HTTP 要求行與標頭開頭之間) 。</span><span class="sxs-lookup"><span data-stu-id="8cca5-107">Requests that contain linear white space (LWS) between the HTTP request line and start of headers.</span></span>

<span data-ttu-id="8cca5-108">預設會啟用這些行為，而且不受登錄設定控制。</span><span class="sxs-lookup"><span data-stu-id="8cca5-108">These behaviors are enabled by default and are not controlled by registry settings.</span></span>

 

 




