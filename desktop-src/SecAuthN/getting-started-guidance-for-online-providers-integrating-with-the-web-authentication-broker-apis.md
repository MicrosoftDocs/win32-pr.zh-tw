---
description: 適用于 網頁程式開發人員和線上提供者的指導方針，可針對 Windows 8 Web 驗證訊息代理程式 Api，建立專為單一登入 (SSO) 功能量身打造的網頁。
ms.assetid: E2AECE26-9649-41CB-9808-4F8171C707C3
title: 與 Web 驗證訊息代理程式 Api 整合之線上提供者的使用者入門指南
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842f3c562d2ad288efaecec82f8da8ca771886a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851148"
---
# <a name="getting-started-guidance-for-online-providers-integrating-with-the-web-authentication-broker-apis"></a><span data-ttu-id="2207b-103">與 Web 驗證訊息代理程式 Api 整合之線上提供者的使用者入門指南</span><span class="sxs-lookup"><span data-stu-id="2207b-103">Getting started guidance for online providers integrating with the Web Authentication Broker APIs</span></span>

<span data-ttu-id="2207b-104">本節將引導 網頁程式開發人員和線上提供者，以建立專為 Windows 8 Web Authentication Broker Api 量身打造的網頁。</span><span class="sxs-lookup"><span data-stu-id="2207b-104">This section guides web developers and online providers for creating web pages tailored for the Windows 8 Web Authentication Broker APIs.</span></span> <span data-ttu-id="2207b-105">它針對網頁的端對端使用者體驗提供視覺效果和互動式建議，以及如何啟用 (SSO) 功能的單一登入。</span><span class="sxs-lookup"><span data-stu-id="2207b-105">It provides the visual and interactive recommendations for an end-to-end user experience of the web page as well as how to enable single sign-on (SSO) capabilities.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2207b-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="2207b-106">In this section</span></span>



| <span data-ttu-id="2207b-107">主題</span><span class="sxs-lookup"><span data-stu-id="2207b-107">Topic</span></span>                                                                                                     | <span data-ttu-id="2207b-108">描述</span><span class="sxs-lookup"><span data-stu-id="2207b-108">Description</span></span>                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2207b-109">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="2207b-109">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)<br/> | <span data-ttu-id="2207b-110">Web 驗證訊息代理程式建置於與 Windows Internet Explorer 的相同技術之上。</span><span class="sxs-lookup"><span data-stu-id="2207b-110">Web Authentication Broker is built on the top of the same technologies that power Internet Explorer in Windows.</span></span> <span data-ttu-id="2207b-111">不過，由於此元件的特殊用途，Internet Explorer 的某些功能已停用或鎖定特定的設定。</span><span class="sxs-lookup"><span data-stu-id="2207b-111">However, due to a very special purpose of this component some features of the Internet Explorer were disabled or locked to specific configuration.</span></span> <br/> |
| [<span data-ttu-id="2207b-112">如何自訂 UI 元素</span><span class="sxs-lookup"><span data-stu-id="2207b-112">How to customize the UI elements</span></span>](how-to-customize-the-ui-elements.md)<br/>                       | <span data-ttu-id="2207b-113">網頁會使用網頁上定義的元資料標記，利用標題、圖示和標題色彩，自訂使用者介面 (UI) 。</span><span class="sxs-lookup"><span data-stu-id="2207b-113">A web page customizes the user interface (UI) with the title, icon, and header color by using metadata tags defined on the web page.</span></span><br/>                                                                                                                                |
| [<span data-ttu-id="2207b-114">驗證網頁的教學課程</span><span class="sxs-lookup"><span data-stu-id="2207b-114">Tutorial for authenticating web pages</span></span>](tutorial-for-authenticating-web-pages.md)<br/>             |                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="2207b-115">Web 驗證問題</span><span class="sxs-lookup"><span data-stu-id="2207b-115">Web authentication problems</span></span>](web-authentication-problems.md)<br/>                                 | <span data-ttu-id="2207b-116">本主題說明針對您的網頁使用 Web 驗證訊息代理程式 Api 的疑難排解秘訣。</span><span class="sxs-lookup"><span data-stu-id="2207b-116">This topic describes troubleshooting tips for using the Web Authentication Broker APIs for your web pages.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="2207b-117">Web 驗證訊息代理程式的常見問題</span><span class="sxs-lookup"><span data-stu-id="2207b-117">FAQ for Web Authentication Broker</span></span>](faq-for-web-authentication-broker.md)<br/>                     | <span data-ttu-id="2207b-118">Web 驗證訊息代理程式的常見問題。</span><span class="sxs-lookup"><span data-stu-id="2207b-118">Frequently asked questions for Web Authentication Broker.</span></span><br/>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="2207b-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="2207b-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2207b-120">[Web 驗證訊息代理程式總覽](/previous-versions/windows/apps/hh750287(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="2207b-120">[Web authentication broker overview](/previous-versions/windows/apps/hh750287(v=win.10))</span></span>
</dt> <dt>

[<span data-ttu-id="2207b-121">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="2207b-121">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="2207b-122">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="2207b-122">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

