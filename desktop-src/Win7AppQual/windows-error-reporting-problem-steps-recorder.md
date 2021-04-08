---
description: .
ms.assetid: ce5db84a-53b6-4a7f-bee4-d198d8a6781e
title: Windows 錯誤報告問題步驟收錄程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25fb70acef867b878063bd6011fde6867f7f0e75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695164"
---
# <a name="windows-error-reporting-problem-steps-recorder"></a><span data-ttu-id="f9405-103">Windows 錯誤報告問題步驟收錄程式</span><span class="sxs-lookup"><span data-stu-id="f9405-103">Windows Error Reporting Problem Steps Recorder</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f9405-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="f9405-104">Affected Platforms</span></span>

<span data-ttu-id="f9405-105">**用戶端** – Windows 7</span><span class="sxs-lookup"><span data-stu-id="f9405-105">**Clients** – Windows 7</span></span>  
<span data-ttu-id="f9405-106">**伺服器** – Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f9405-106">**Servers** – Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="f9405-107">Description</span><span class="sxs-lookup"><span data-stu-id="f9405-107">Description</span></span>

<span data-ttu-id="f9405-108">在 Windows 7 之前，Windows 錯誤報告 (WER) 收集到指出需要修復問題的錯誤報表。</span><span class="sxs-lookup"><span data-stu-id="f9405-108">Prior to Windows 7, Windows Error Reporting (WER) collected error reports that indicated problems in need of repair.</span></span> <span data-ttu-id="f9405-109">這些錯誤報表包含實用的資訊，描述問題的一般本質，但無法判斷其根本原因的資訊。</span><span class="sxs-lookup"><span data-stu-id="f9405-109">These error reports contain helpful information that describes the general nature of a problem, but not enough information to determine its root cause.</span></span> <span data-ttu-id="f9405-110">針對這一點，開發人員需要一個工具來重現當機/停止回應案例以進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="f9405-110">For that, developers need a tool to reproduce the crash/hang scenario for debugging.</span></span>

<span data-ttu-id="f9405-111">新的應用程式問題步驟收錄程式 (PSR.exe) ）會在所有的 Windows 7 組建上寄出。</span><span class="sxs-lookup"><span data-stu-id="f9405-111">A new application, Problem Steps Recorder (PSR.exe), is shipping on all builds of Windows 7.</span></span> <span data-ttu-id="f9405-112">這項功能可讓使用者在遇到損毀時，收集使用者所執行的動作，讓測試人員和開發人員可以重現分析和偵測的情況。</span><span class="sxs-lookup"><span data-stu-id="f9405-112">This feature enables the collection of the actions performed by a user while encountering a crash so that testers and developers can reproduce the situation for analysis and debugging.</span></span>

## <a name="usage"></a><span data-ttu-id="f9405-113">使用方式</span><span class="sxs-lookup"><span data-stu-id="f9405-113">Usage</span></span>

<span data-ttu-id="f9405-114">目前，Windows 錯誤報告服務開發人員必須要求應用程式的 PSR 啟用;Microsoft 支援組織也會在與終端使用者進行疑難排解時使用此工具。</span><span class="sxs-lookup"><span data-stu-id="f9405-114">Currently, a Windows Error Reporting service developer must request PSR enablement for an application; Microsoft support organizations also use this tool while troubleshooting with end users.</span></span> <span data-ttu-id="f9405-115">在 windows 7 發行之後，您可以在 Windows Quality Online Services (Winqual) PSR 提供方案。</span><span class="sxs-lookup"><span data-stu-id="f9405-115">Plans are in place to make PSR available at Windows Quality Online Services (Winqual) after the release of Windows 7.</span></span>

<span data-ttu-id="f9405-116">**注意：** 針對應用程式啟用 PSR 之後，應用程式可能會看到效能降低的情況。</span><span class="sxs-lookup"><span data-stu-id="f9405-116">**Note:** With PSR enabled for an application, the application may see some performance degradation.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f9405-117">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="f9405-117">Links to Other Resources</span></span>

-   [<span data-ttu-id="f9405-118">Windows 錯誤報告的 blog 專案</span><span class="sxs-lookup"><span data-stu-id="f9405-118">Windows Error Reporting blog entry</span></span>](/archive/blogs/wer/)
-   [<span data-ttu-id="f9405-119">Windows Quality Online Services (Winqual) </span><span class="sxs-lookup"><span data-stu-id="f9405-119">Windows Quality Online Services (Winqual)</span></span>](https://winqual.microsoft.com)

 

 
