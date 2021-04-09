---
description: 驗證正在證明您的身分。
ms.assetid: 5B058197-67B3-40DD-80D8-7BD8EE084CC9
title: Web 網頁驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7c7bd37334f345ae16074c050b6b06c5fd644f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944886"
---
# <a name="authentication-for-web-pages"></a><span data-ttu-id="c8516-103">Web 網頁驗證</span><span class="sxs-lookup"><span data-stu-id="c8516-103">Authentication for web pages</span></span>

<span data-ttu-id="c8516-104">驗證正在證明您的身分。</span><span class="sxs-lookup"><span data-stu-id="c8516-104">Authentication is proving who you are.</span></span>

<span data-ttu-id="c8516-105">**目標：** 讓 web 驗證訊息代理程式顯示為應用程式的一部分。</span><span class="sxs-lookup"><span data-stu-id="c8516-105">**Objective:** To have the web authentication broker appear as part of your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8516-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="c8516-106">Prerequisites</span></span>

<span data-ttu-id="c8516-107">無</span><span class="sxs-lookup"><span data-stu-id="c8516-107">None</span></span>

<span data-ttu-id="c8516-108">**完成時間：** 15 分鐘。</span><span class="sxs-lookup"><span data-stu-id="c8516-108">**Time to complete:** 15 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="c8516-109">指示</span><span class="sxs-lookup"><span data-stu-id="c8516-109">Instructions</span></span>

### <a name="1-getting-started"></a><span data-ttu-id="c8516-110">1.開始使用</span><span class="sxs-lookup"><span data-stu-id="c8516-110">1. Getting started</span></span>

<span data-ttu-id="c8516-111">啟動安裝程式檔案，在本機電腦上的 Internet Information Services 8 中安裝 Contoso 網站，以裝載範例 HTML 和 CSS 檔案。</span><span class="sxs-lookup"><span data-stu-id="c8516-111">Launch the setup file to install a Contoso website in Internet Information Services 8 on the local machine to host the sample HTML and CSS files.</span></span>

1.  <span data-ttu-id="c8516-112">範例 HTML 和 CSS 檔案將會安裝至 Microsoft Contoso 底下的 program files 目錄 \\ 。</span><span class="sxs-lookup"><span data-stu-id="c8516-112">Sample HTML and CSS files will be installed to the program files directory under Microsoft\\Contoso.</span></span>
2.  <span data-ttu-id="c8516-113">此外，「Fabrikam 社交」 Windows Store 應用程式將會解除封裝至桌面。</span><span class="sxs-lookup"><span data-stu-id="c8516-113">In addition a "Fabrikam Social"Windows Store app will be unpackaged to the desktop.</span></span>

### <a name="2-getting-familiar"></a><span data-ttu-id="c8516-114">2. 熟悉</span><span class="sxs-lookup"><span data-stu-id="c8516-114">2. Getting familiar</span></span>

<span data-ttu-id="c8516-115">若要瞭解範例頁面在 Web 驗證訊息代理程式中的外觀，請在桌面上的 "Fabrikam 社交" 資料夾中開啟 Fabrikam 社交 Visual Studio 11 方案檔。</span><span class="sxs-lookup"><span data-stu-id="c8516-115">To get a feel for what the sample pages look like in the Web Authentication Broker, open the Fabrikam Social Visual Studio 11 solution file in the "Fabrikam Social" folder on the desktop.</span></span>

1.  <span data-ttu-id="c8516-116">執行應用程式並按 [啟動]，以顯示 Web 驗證訊息代理程式中的範例頁面。</span><span class="sxs-lookup"><span data-stu-id="c8516-116">Run the application and hit "Launch" to bring up the sample pages in the Web Authentication Broker.</span></span>
2.  <span data-ttu-id="c8516-117">您可以藉由將某些資料共用至應用程式，將應用程式調整為一側或啟用。</span><span class="sxs-lookup"><span data-stu-id="c8516-117">The app can be resized to one side or activated by sharing some data to the application.</span></span>

### <a name="3-authentication"></a><span data-ttu-id="c8516-118">3. 驗證</span><span class="sxs-lookup"><span data-stu-id="c8516-118">3. Authentication</span></span>

<span data-ttu-id="c8516-119">基礎應用程式叫用 Web 驗證 API 來連線至提供者 "Contoso Social" 時，會顯示登入頁面。</span><span class="sxs-lookup"><span data-stu-id="c8516-119">When the Web Auth API is invoked by the underlying app to connect to the provider, "Contoso Social", the login page is shown.</span></span> <span data-ttu-id="c8516-120">此頁面的設計最適合快速且流暢的登入體驗。</span><span class="sxs-lookup"><span data-stu-id="c8516-120">This page is designed to be best at a fast and fluid login experience.</span></span> <span data-ttu-id="c8516-121">它也提供一些其他常見使用者動作的進入點，例如：抓取密碼詳細資料、註冊帳戶，以及閱讀在瀏覽器中完成之隱私權和條款及條件的聲明。</span><span class="sxs-lookup"><span data-stu-id="c8516-121">It also provides entry points to some other common user actions such as retrieving password details, signing up for an account, and reading statements on privacy and terms and conditions that are completed in the browser.</span></span> ![contoso 登入頁面](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a><span data-ttu-id="c8516-123">摘要和後續步驟</span><span class="sxs-lookup"><span data-stu-id="c8516-123">Summary and next steps</span></span>

<span data-ttu-id="c8516-124">[驗證網頁的摘要教學](tutorial-for-authenticating-web-pages.md)課程</span><span class="sxs-lookup"><span data-stu-id="c8516-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="c8516-125">[Web 網頁的](authorization-for-web-pages.md)下一個授權</span><span class="sxs-lookup"><span data-stu-id="c8516-125">Next [Authorization for web pages](authorization-for-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8516-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="c8516-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8516-127">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="c8516-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="c8516-128">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="c8516-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="c8516-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="c8516-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
