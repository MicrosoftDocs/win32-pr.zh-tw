---
description: 授權會設定您有權存取的資源。
ms.assetid: DD6836EE-DF73-4A07-9DF1-0F5A959DDE8F
title: Web 網頁的授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88c26e9bc8333d74d18989c5c581cc54054a29ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848499"
---
# <a name="authorization-for-web-pages"></a><span data-ttu-id="85b9a-103">Web 網頁的授權</span><span class="sxs-lookup"><span data-stu-id="85b9a-103">Authorization for web pages</span></span>

<span data-ttu-id="85b9a-104">授權會設定您有權存取的資源。</span><span class="sxs-lookup"><span data-stu-id="85b9a-104">Authorization sets what resources you have access to.</span></span>

<span data-ttu-id="85b9a-105">**目標：** 允許使用者存取您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="85b9a-105">**Objective:** To allow users access to your app.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="85b9a-106">必要條件</span><span class="sxs-lookup"><span data-stu-id="85b9a-106">Prerequisites</span></span>

<span data-ttu-id="85b9a-107">無</span><span class="sxs-lookup"><span data-stu-id="85b9a-107">None</span></span>

<span data-ttu-id="85b9a-108">**完成時間：** 2 分鐘。</span><span class="sxs-lookup"><span data-stu-id="85b9a-108">**Time to complete:** 2 minutes.</span></span>

## <a name="instructions"></a><span data-ttu-id="85b9a-109">指示</span><span class="sxs-lookup"><span data-stu-id="85b9a-109">Instructions</span></span>

### <a name="1-authorization"></a><span data-ttu-id="85b9a-110">1. 授權</span><span class="sxs-lookup"><span data-stu-id="85b9a-110">1. Authorization</span></span>

<span data-ttu-id="85b9a-111">當使用者輸入其認證，並按一下 [登入] 按鈕時，會顯示 [許可權] 頁面。</span><span class="sxs-lookup"><span data-stu-id="85b9a-111">When the user enters their credentials and clicks the Login button, the permissions page is shown.</span></span> <span data-ttu-id="85b9a-112">此頁面最適合讓使用者控制授與應用程式存取 Contoso 資料的細微許可權。</span><span class="sxs-lookup"><span data-stu-id="85b9a-112">This page is best at allowing users to control granular permissions in granting the app to access to Contoso’s data.</span></span> ![contoso 許可權頁面](images/wab-figure9.png)

### <a name="2-how-to-use-the-sample"></a><span data-ttu-id="85b9a-114">2. 如何使用範例</span><span class="sxs-lookup"><span data-stu-id="85b9a-114">2. How to use the sample</span></span>

<span data-ttu-id="85b9a-115">您必須知道下列 HTML 和 CSS 檔案。</span><span class="sxs-lookup"><span data-stu-id="85b9a-115">You need to know about the following HTML and CSS files.</span></span>

1.  <span data-ttu-id="85b9a-116">下列 HTML 檔案會對應至 web 授權流程中的兩個頁面</span><span class="sxs-lookup"><span data-stu-id="85b9a-116">The following HTML files correspond to the two pages in the web authorization flow</span></span>
    -   <span data-ttu-id="85b9a-117">WebAuthLogin.html-登入頁面的範例 HTML</span><span class="sxs-lookup"><span data-stu-id="85b9a-117">WebAuthLogin.html – sample HTML for the login page</span></span>
    -   <span data-ttu-id="85b9a-118">WebAuthPermissions.html-許可權頁面的範例 HTML</span><span class="sxs-lookup"><span data-stu-id="85b9a-118">WebAuthPermissions.html – sample HTML for the permissions page</span></span>
2.  <span data-ttu-id="85b9a-119">CSS 檔案包含 Windows 8 的樣式，以協助建立 Windows Store 應用程式網頁。</span><span class="sxs-lookup"><span data-stu-id="85b9a-119">The CSS files contain Windows 8 styles to help create a Windows Store app web page.</span></span>
    -   <span data-ttu-id="85b9a-120">ui-light-這是衍生自 Windows 8 控制項的基底樣式表單。</span><span class="sxs-lookup"><span data-stu-id="85b9a-120">ui-light.css – this has been derived from the base style sheet for Windows 8 controls.</span></span>
    -   <span data-ttu-id="85b9a-121">ui-webauth：這會提供用於將 web 驗證頁面的版面配置優化的遞增樣式。</span><span class="sxs-lookup"><span data-stu-id="85b9a-121">ui-webauth.css – this provides incremental styling for optimizing layout for web auth pages.</span></span>
    -   <span data-ttu-id="85b9a-122">theme-colors：這會提供遞增樣式，以使用提供者的品牌色彩覆寫控制項的預設輔色。</span><span class="sxs-lookup"><span data-stu-id="85b9a-122">theme-colors.css – this provides the incremental styling to override default accent colors of controls with the provider’s brand color.</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="85b9a-123">摘要和後續步驟</span><span class="sxs-lookup"><span data-stu-id="85b9a-123">Summary and next steps</span></span>

<span data-ttu-id="85b9a-124">[驗證網頁的摘要教學](tutorial-for-authenticating-web-pages.md)課程</span><span class="sxs-lookup"><span data-stu-id="85b9a-124">Summary [Tutorial for authenticating web pages](tutorial-for-authenticating-web-pages.md)</span></span>

<span data-ttu-id="85b9a-125">[設計驗證網頁的下一個最佳作法](best-practices-for-designing-authentication-web-pages.md)</span><span class="sxs-lookup"><span data-stu-id="85b9a-125">Next [Best practices for designing authentication web pages](best-practices-for-designing-authentication-web-pages.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="85b9a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="85b9a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b9a-127">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="85b9a-127">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="85b9a-128">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="85b9a-128">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="85b9a-129">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="85b9a-129">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
