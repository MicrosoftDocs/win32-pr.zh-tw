---
description: 在開始開發 Microsoft Windows HTTP 服務 (WinHTTP) 應用程式之前，您必須先決定要使用 C/c + + API 或 COM 介面。
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: 選擇 WinHTTP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989454"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="53f8a-103">選擇 WinHTTP 介面</span><span class="sxs-lookup"><span data-stu-id="53f8a-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="53f8a-104">在開始開發 Microsoft Windows HTTP 服務 (WinHTTP) 應用程式之前，您必須先決定要使用 C/c + + API 或 COM 介面。</span><span class="sxs-lookup"><span data-stu-id="53f8a-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="53f8a-105">下表摘要說明每個方法的相關優點和缺點。</span><span class="sxs-lookup"><span data-stu-id="53f8a-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="53f8a-106">C/C + + API</span><span class="sxs-lookup"><span data-stu-id="53f8a-106">C/C++ API</span></span></th>
<th><span data-ttu-id="53f8a-107">COM 介面</span><span class="sxs-lookup"><span data-stu-id="53f8a-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="53f8a-108">優點</span><span class="sxs-lookup"><span data-stu-id="53f8a-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="53f8a-109">您可以在區塊中處理回應，這會更有效率。</span><span class="sxs-lookup"><span data-stu-id="53f8a-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="53f8a-110">POST 作業也可以在區塊中處理，以加速處理時間。</span><span class="sxs-lookup"><span data-stu-id="53f8a-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="53f8a-111">自動代理支援。</span><span class="sxs-lookup"><span data-stu-id="53f8a-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="53f8a-112">存取 WinHTTP 的完整功能集。</span><span class="sxs-lookup"><span data-stu-id="53f8a-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="53f8a-113">您可以輕鬆地處理二進位資料。</span><span class="sxs-lookup"><span data-stu-id="53f8a-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="53f8a-114">建立應用程式很容易，而且需要比 C/c + + API 更少的程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="53f8a-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="53f8a-115">指令碼語言可以使用此介面。</span><span class="sxs-lookup"><span data-stu-id="53f8a-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="53f8a-116">缺點</span><span class="sxs-lookup"><span data-stu-id="53f8a-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="53f8a-117">處理更為複雜。</span><span class="sxs-lookup"><span data-stu-id="53f8a-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="53f8a-118">C/c + + API 需要的步驟多於 COM 介面，才能執行相同的動作。</span><span class="sxs-lookup"><span data-stu-id="53f8a-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="53f8a-119">設定要求需要更多程式碼。</span><span class="sxs-lookup"><span data-stu-id="53f8a-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="53f8a-120">COM 介面不提供對 WinHTTP 完整功能集的存取權。</span><span class="sxs-lookup"><span data-stu-id="53f8a-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="53f8a-121">在某些指令碼語言（如 VBScript 和 JScript）中，很難處理二進位資料類型。</span><span class="sxs-lookup"><span data-stu-id="53f8a-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="53f8a-122">COM 介面不支援自動代理。</span><span class="sxs-lookup"><span data-stu-id="53f8a-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="53f8a-123">應用程式必須使用 COM APARTMENT_THREADED 模型。</span><span class="sxs-lookup"><span data-stu-id="53f8a-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="53f8a-124">在開始處理回應之前，必須先接收和緩衝處理整個回應。</span><span class="sxs-lookup"><span data-stu-id="53f8a-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



