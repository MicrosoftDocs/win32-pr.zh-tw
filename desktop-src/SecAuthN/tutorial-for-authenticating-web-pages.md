---
description: 本教學課程強調 網頁程式開發人員針對 Windows 8 的 web 授權流程設計網頁時，應該在意的不同層面。 這個範例會示範兩頁的授權流程。
ms.assetid: A26E09EF-6C7A-4F75-89A7-76086F63F3B1
title: 驗證網頁的教學課程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6fc6482c5e6dfaf89a9fc9732783f5f088b4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998522"
---
# <a name="tutorial-for-authenticating-web-pages"></a><span data-ttu-id="37f6a-104">驗證網頁的教學課程</span><span class="sxs-lookup"><span data-stu-id="37f6a-104">Tutorial for authenticating web pages</span></span>

<span data-ttu-id="37f6a-105">本教學課程強調 網頁程式開發人員針對 Windows 8 的 web 授權流程設計網頁時，應該在意的不同層面。</span><span class="sxs-lookup"><span data-stu-id="37f6a-105">This tutorial highlights the different aspects that web developers should care about when designing pages for the web authorization flow for Windows 8.</span></span> <span data-ttu-id="37f6a-106">這個範例會示範兩頁的授權流程。</span><span class="sxs-lookup"><span data-stu-id="37f6a-106">This section This sample demonstrates a two-page authorization flow.</span></span>

<span data-ttu-id="37f6a-107">**目標：** 此範例的目標不是要對每個提供者絕對有獨特觀點的版面配置或視覺設計產生規範，但要特別注意一些值得投資的領域，以取得 Windows 8 的頂級 Microsoft 設計樣式體驗。</span><span class="sxs-lookup"><span data-stu-id="37f6a-107">**Objective:** The goal of the sample is not to be prescriptive about the layout or visual design that each provider will certainly have a unique point of view on, but to call out a few areas worth investing in to have a first-class Microsoft design style experience for Windows 8.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37f6a-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="37f6a-108">Prerequisites</span></span>

<span data-ttu-id="37f6a-109">若要使用 web 驗證訊息代理程式 Api，您需要：</span><span class="sxs-lookup"><span data-stu-id="37f6a-109">In order to use web authentication broker APIs, you need:</span></span>

-   <span data-ttu-id="37f6a-110">Windows 8 只 (x86 或 amd64) </span><span class="sxs-lookup"><span data-stu-id="37f6a-110">Windows 8 (x86 or amd64 only)</span></span>
-   <span data-ttu-id="37f6a-111">您應從 [程式和功能] 下的主控台安裝 Microsoft Internet Information Services (IIS) ，並使用 [開啟或關閉 Windows 功能] 選項。</span><span class="sxs-lookup"><span data-stu-id="37f6a-111">Microsoft Internet Information Services (IIS) should be installed from the Control Panel under "Programs and Features" and using the "Turn Windows features on or off" option.</span></span>

<span data-ttu-id="37f6a-112">**完成的總時間：** 2 分鐘。</span><span class="sxs-lookup"><span data-stu-id="37f6a-112">**Total time to complete:** 2 minutes.</span></span>

## <a name="where-to-go-from-here"></a><span data-ttu-id="37f6a-113">現在該如何開始</span><span class="sxs-lookup"><span data-stu-id="37f6a-113">Where to go from here</span></span>

<span data-ttu-id="37f6a-114">[Web 網頁的](authentication-for-web-pages.md)下一個驗證</span><span class="sxs-lookup"><span data-stu-id="37f6a-114">Next [Authentication for web pages](authentication-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="37f6a-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="37f6a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="37f6a-116">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="37f6a-116">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="37f6a-117">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="37f6a-117">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="37f6a-118">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="37f6a-118">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041)
</dt> </dl>

 

 
