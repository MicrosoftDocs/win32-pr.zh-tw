---
title: 為何要使用文字服務架構
description: 為何要使用文字服務架構
ms.assetid: 64b3b0a1-7740-49fa-b0a6-f80040147280
keywords:
- 文字服務架構 (TSF) ，關於
- TSF (文字服務架構) ，關於
- 文字服務，關於
- 啟用 TSF 的應用程式，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6647981b890bd1fcdf488b18bffad587f49ed9b5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965160"
---
# <a name="why-use-text-services-framework"></a><span data-ttu-id="ed35a-107">為何要使用文字服務架構？</span><span class="sxs-lookup"><span data-stu-id="ed35a-107">Why Use Text Services Framework?</span></span>

<span data-ttu-id="ed35a-108">文字服務架構 (TSF) 啟用啟用 TSF 的應用程式，以接收來自任何數目之裝置或來源的文字輸入。</span><span class="sxs-lookup"><span data-stu-id="ed35a-108">Text Services Framework (TSF) enables a TSF-enabled application to receive text input from any number of devices or sources.</span></span> <span data-ttu-id="ed35a-109">因為 TSF 是可擴充的，所以應用程式可以從其他文字來源接收文字輸入，幾乎不需要修改。</span><span class="sxs-lookup"><span data-stu-id="ed35a-109">Because TSF is extensible, the application can receive text input from additional text sources with little or no modification.</span></span>

<span data-ttu-id="ed35a-110">文字服務會從任何 TSF 啟用的應用程式取得文字，而不需要任何應用程式的相關知識。</span><span class="sxs-lookup"><span data-stu-id="ed35a-110">A text service obtains text from, and provides text to, any TSF-enabled application without requiring any knowledge about the application.</span></span> <span data-ttu-id="ed35a-111">此結構可讓文字服務可供任何啟用 TSF 的應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="ed35a-111">This structure enables the text service to be available to any TSF-enabled application.</span></span> <span data-ttu-id="ed35a-112">文字服務可以安裝或更新為個別的模組，而且與任何特定的應用程式無關。</span><span class="sxs-lookup"><span data-stu-id="ed35a-112">The text service can be installed or updated as a separate module and is independent of any specific application.</span></span> <span data-ttu-id="ed35a-113">TSF 也可讓文字服務使用檔、文字片段或檔內的物件來儲存中繼資料。</span><span class="sxs-lookup"><span data-stu-id="ed35a-113">TSF also enables a text service to store metadata with a document, a piece of text, or an object within the document.</span></span> <span data-ttu-id="ed35a-114">例如，語音輸入文字服務可以儲存與文字區塊相關聯的音效資訊。</span><span class="sxs-lookup"><span data-stu-id="ed35a-114">For example, a speech input text service can store sound information associated with a block of text.</span></span>

<span data-ttu-id="ed35a-115">TSF 可讓文字服務透過連續存取檔案緩衝區，提供精確且完整的文字轉換。</span><span class="sxs-lookup"><span data-stu-id="ed35a-115">TSF enables text services to provide accurate and complete text conversion, with continuous access to the document buffer.</span></span> <span data-ttu-id="ed35a-116">使用 TSF 的文字服務可以避免將它們的功能分隔成輸入和模式的模式，以進行編輯。</span><span class="sxs-lookup"><span data-stu-id="ed35a-116">Text services using TSF can avoid separating their functionality into modes for input and modes for editing.</span></span> <span data-ttu-id="ed35a-117">此輸入架構可讓緩衝和累積的文字資料流程以動態方式變更，藉此啟用更有效率的鍵盤輸入和文字編輯。</span><span class="sxs-lookup"><span data-stu-id="ed35a-117">This input architecture enables the buffered and accumulating text stream to change dynamically, thereby enabling more efficient keyboard input and text editing.</span></span>

<span data-ttu-id="ed35a-118">TSF 與裝置無關，而且可為多個輸入裝置（包括鍵盤、畫筆和麥克風）啟用文字服務。</span><span class="sxs-lookup"><span data-stu-id="ed35a-118">TSF is device-independent and enables text services for multiple input devices including keyboard, pen, and microphone.</span></span>

 

 




