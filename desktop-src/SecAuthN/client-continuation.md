---
description: 某些通訊協定需要多個驗證訊息。
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: 用戶端接續
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848667"
---
# <a name="client-continuation"></a><span data-ttu-id="7fb10-103">用戶端接續</span><span class="sxs-lookup"><span data-stu-id="7fb10-103">Client Continuation</span></span>

<span data-ttu-id="7fb10-104">某些通訊協定需要多個驗證訊息。</span><span class="sxs-lookup"><span data-stu-id="7fb10-104">Some protocols require multiple authentication messages.</span></span> <span data-ttu-id="7fb10-105">在此情況下，用戶端會剖析伺服器的回應，並使用上一個呼叫的 [繼續] 狀態，再次呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 。</span><span class="sxs-lookup"><span data-stu-id="7fb10-105">In this case, the client parses the response from the server and calls [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) again using the continue status from the previous call.</span></span> <span data-ttu-id="7fb10-106">用戶端會檢查此呼叫的傳回狀態，而且可能需要繼續進行額外的腿。</span><span class="sxs-lookup"><span data-stu-id="7fb10-106">The client checks the return status from this call and might be required to continue for additional legs.</span></span> <span data-ttu-id="7fb10-107">它會使用 *pOutput* 中的資訊來建立訊息，並將它傳送至伺服器。</span><span class="sxs-lookup"><span data-stu-id="7fb10-107">It uses the information in *pOutput* to construct a message and sends it to the server.</span></span>

 

 
