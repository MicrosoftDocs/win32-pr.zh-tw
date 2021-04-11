---
description: .
ms.assetid: D721167E-B04B-4B06-A9EE-56711A7A1942
title: Internet Explorer 8 開發人員工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a184b513717655ee0a738be6318b4c8f2515ca3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115712"
---
# <a name="internet-explorer-8-developer-tools"></a><span data-ttu-id="4b29a-103">Internet Explorer 8 開發人員工具</span><span class="sxs-lookup"><span data-stu-id="4b29a-103">Internet Explorer 8 Developer Tools</span></span>

<span data-ttu-id="4b29a-104">Windows Internet Explorer 8 包含「開發人員工具」功能。</span><span class="sxs-lookup"><span data-stu-id="4b29a-104">Windows Internet Explorer 8 includes the Developer Tools feature.</span></span> <span data-ttu-id="4b29a-105">這項功能可讓您快速地進行 Microsoft JScript 的偵測、調查 Windows Internet Explorer 特定的行為，或迅速反覆運算以建立原型或測試新的設計解決方案。</span><span class="sxs-lookup"><span data-stu-id="4b29a-105">This feature enables you to debug Microsoft JScript quickly, investigate a Windows Internet Explorer-specific behavior, or iterate rapidly to prototype or test a new design solution.</span></span>

<span data-ttu-id="4b29a-106">下列各節說明 Internet Explorer 8 的開發人員工具的重要特性。</span><span class="sxs-lookup"><span data-stu-id="4b29a-106">The following sections describe the important characteristics of the Developer Tools in Internet Explorer 8.</span></span>

## <a name="integrated-and-simple-to-use"></a><span data-ttu-id="4b29a-107">整合式且便於使用</span><span class="sxs-lookup"><span data-stu-id="4b29a-107">Integrated and Simple to Use</span></span>

<span data-ttu-id="4b29a-108">每個安裝的 Internet Explorer 8 都包含開發人員工具，因此您可以在任何執行 Internet Explorer 8 的電腦上進行問題的偵測。</span><span class="sxs-lookup"><span data-stu-id="4b29a-108">The Developer Tools are included with every installation of Internet Explorer 8, so you can debug issues on any computer that is running Internet Explorer 8.</span></span> <span data-ttu-id="4b29a-109">此外，工具只會在您需要時載入，以限制其對瀏覽器效能的影響。</span><span class="sxs-lookup"><span data-stu-id="4b29a-109">In addition, the tools load only when you need them to limit how they impact the browser's performance.</span></span> <span data-ttu-id="4b29a-110">使用開發人員工具，您可以快速地只針對目前的 Internet Explorer 處理常式進行偵錯工具，而不是所有 Internet Explorer 的偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="4b29a-110">By using the Developer Tools, you can rapidly debug only the current Internet Explorer process, instead of debugging for all of Internet Explorer.</span></span>

## <a name="provide-a-visual-interface-to-the-platform"></a><span data-ttu-id="4b29a-111">提供平臺的視覺化介面</span><span class="sxs-lookup"><span data-stu-id="4b29a-111">Provide a Visual Interface to the Platform</span></span>

<span data-ttu-id="4b29a-112">開發人員工具可讓您查看 Internet Explorer 來查看您網站的呈現方式，而不是反向工程您的網站如何運作或修改您的網站以輸出 debug 資訊。</span><span class="sxs-lookup"><span data-stu-id="4b29a-112">Instead of reverse engineering how your website works or modifying your site to output debug information, the Developer Tools let you look into Internet Explorer to view its representation of your site.</span></span> <span data-ttu-id="4b29a-113">此視圖可減少您花在偵測動態網站、來源檢查不實用或調查 Internet Explorer 特定行為（一般 authoring tool 無法協助）的時間。</span><span class="sxs-lookup"><span data-stu-id="4b29a-113">This view reduces the time that you spend debugging dynamic sites, where source inspection is not useful, or investigating an Internet Explorer-specific behavior, where a generic authoring tool cannot help.</span></span>

## <a name="enable-fast-experimentation"></a><span data-ttu-id="4b29a-114">啟用快速實驗</span><span class="sxs-lookup"><span data-stu-id="4b29a-114">Enable Fast Experimentation</span></span>

<span data-ttu-id="4b29a-115">當您在舊版 Internet Explorer 中建立新設計或測試修正的原型時，您可能會在瀏覽器中編輯來源、儲存、重新整理頁面，然後重複。</span><span class="sxs-lookup"><span data-stu-id="4b29a-115">When you are prototyping a new design or testing fixes in previous versions of Internet Explorer, you likely edit your source, save it, refresh your page in the browser, and repeat.</span></span> <span data-ttu-id="4b29a-116">開發人員工具可讓您在瀏覽器內編輯網站並立即查看變更，藉此簡化這個案例。</span><span class="sxs-lookup"><span data-stu-id="4b29a-116">The Developer Tools streamline this scenario by enabling you to edit your site within the browser and see changes immediately.</span></span>

## <a name="optimize-application-performance"></a><span data-ttu-id="4b29a-117">優化應用程式效能</span><span class="sxs-lookup"><span data-stu-id="4b29a-117">Optimize Application Performance</span></span>

<span data-ttu-id="4b29a-118">若要找出並修正效能問題，您可能會在一次將焦點放在一個案例時進行逐一查看。</span><span class="sxs-lookup"><span data-stu-id="4b29a-118">To identify and fix performance issues, you likely iterate by focusing on one scenario at a time.</span></span> <span data-ttu-id="4b29a-119">藉由在開發人員工具中使用腳本分析工具，您可以收集統計資料，包括執行時間以及呼叫 JavaScript 函數的次數。</span><span class="sxs-lookup"><span data-stu-id="4b29a-119">By using the script profiler in the Developer Tools, you can collect statistics, including execution time and the number of times that a JavaScript function is called.</span></span> <span data-ttu-id="4b29a-120">您可以在測試應用程式時使用此資訊，並使用設定檔報表來快速找出並修正效能瓶頸。</span><span class="sxs-lookup"><span data-stu-id="4b29a-120">You can use this information as you test your application and use the profile report to quickly identify and fix performance bottlenecks.</span></span>

<span data-ttu-id="4b29a-121">若要存取開發人員工具，請在您流覽網頁時按下 F12，或按一下 [**工具**] 功能表上的 [**開發人員工具**]。</span><span class="sxs-lookup"><span data-stu-id="4b29a-121">To access the Developer Tools, press F12 while you are viewing a webpage or click **Developer Tools** on the **Tools** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b29a-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="4b29a-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b29a-123">用於調試 Web 應用程式和附加元件的工具</span><span class="sxs-lookup"><span data-stu-id="4b29a-123">Tools for Debugging Web Applications and Add-Ons</span></span>](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 



