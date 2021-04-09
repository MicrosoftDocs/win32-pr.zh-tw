---
title: 關於自訂檔案和串流處理常式
description: 關於自訂檔案和串流處理常式
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Windows (VFW) 自訂檔案處理常式的影片
- Windows (VFW) 、自訂串流處理常式的影片
- Windows (VFW) 的影片，檔處理常式
- 適用于 Windows (VFW) 、串流處理常式的影片
- 適用于 Windows) 、自訂檔案處理常式的 VFW (影片
- 適用于 Windows) 、自訂串流處理常式的 VFW (影片
- 適用于 Windows) 的 VFW (影片，檔處理常式
- 適用于 Windows) 、串流處理常式的 VFW (影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840800"
---
# <a name="about-custom-file-and-stream-handlers"></a><span data-ttu-id="6cf95-111">關於自訂檔案和串流處理常式</span><span class="sxs-lookup"><span data-stu-id="6cf95-111">About Custom File and Stream Handlers</span></span>

<span data-ttu-id="6cf95-112">您的應用程式可以使用自訂檔案處理常式從檔案讀取或寫入至非標準格式的檔案。</span><span class="sxs-lookup"><span data-stu-id="6cf95-112">Your application can use a custom file handler to read from a file or write to a file that is in a nonstandard format.</span></span> <span data-ttu-id="6cf95-113">若要這樣做，您的應用程式只會在開啟檔案或設定檔案介面時，使用您的檔處理常式名稱。</span><span class="sxs-lookup"><span data-stu-id="6cf95-113">To do this, your application simply uses the name of your file handler when opening the file or allocating the file interface.</span></span> <span data-ttu-id="6cf95-114">AVIFile 程式庫接著會使用來自檔案處理常式的函式，而不是來自另一個檔案處理常式的函式。</span><span class="sxs-lookup"><span data-stu-id="6cf95-114">The AVIFile library then uses the functions from your file handler instead of those from another file handler.</span></span> <span data-ttu-id="6cf95-115">非標準格式會顯示為應用程式的標準 AVI 資料，或使用自訂檔案處理常式的任何其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="6cf95-115">The nonstandard format appears as standard AVI data to your application or to any other application using your custom file handler.</span></span>

<span data-ttu-id="6cf95-116">同樣地，您的應用程式可以使用自訂資料流程處理常式來讀取非標準格式的資料流程。</span><span class="sxs-lookup"><span data-stu-id="6cf95-116">Similarly, your application can use a custom stream handler to read a stream that is in a nonstandard format.</span></span> <span data-ttu-id="6cf95-117">資料流程（不論是構成音訊、影片、MIDI、文字或自訂資料）是 AVI 檔案的元件。</span><span class="sxs-lookup"><span data-stu-id="6cf95-117">A stream — whether it constitutes audio, video, MIDI, text, or custom data — is a component of an AVI file.</span></span> <span data-ttu-id="6cf95-118">例如，包含影片順序的 AVI 檔案、英文的聲段和法文的聲帶都包含三個數據流。</span><span class="sxs-lookup"><span data-stu-id="6cf95-118">For example, an AVI file that contains a video sequence, an English soundtrack, and a French soundtrack consists of three streams.</span></span> <span data-ttu-id="6cf95-119">您的應用程式可以指定 AVI 檔中的資料流程來處理，並將每個資料流程導向至可以最佳方式處理適當多媒體資料類型的處理常式。</span><span class="sxs-lookup"><span data-stu-id="6cf95-119">Your application can specify the streams in an AVI file to process and direct each of those streams to a handler that can optimally process the appropriate type of multimedia data.</span></span>

> [!Note]  
> <span data-ttu-id="6cf95-120">您必須將自訂資料流程和檔案處理常式放在一或多個 Dll 中，並與主要應用程式檔分開。</span><span class="sxs-lookup"><span data-stu-id="6cf95-120">You must place custom stream and file handlers in one or more DLLs, separated from main application files.</span></span>

 

 

 




