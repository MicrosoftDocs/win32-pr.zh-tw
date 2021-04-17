---
description: Web 驗證訊息代理程式的常見問題。
ms.assetid: 49ACB2E3-CF57-4D8E-9670-E7C18A06F76A
title: Web 驗證訊息代理程式的常見問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95942a32bba86f7b2ccb12264cc1a50419b248a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513593"
---
# <a name="faq-for-web-authentication-broker"></a><span data-ttu-id="13d71-103">Web 驗證訊息代理程式的常見問題</span><span class="sxs-lookup"><span data-stu-id="13d71-103">FAQ for Web Authentication Broker</span></span>

<span data-ttu-id="13d71-104">Web 驗證訊息代理程式的常見問題。</span><span class="sxs-lookup"><span data-stu-id="13d71-104">Frequently asked questions for Web Authentication Broker.</span></span>



| <span data-ttu-id="13d71-105">問題</span><span class="sxs-lookup"><span data-stu-id="13d71-105">Question</span></span>                                                                                                    | <span data-ttu-id="13d71-106">Answer</span><span class="sxs-lookup"><span data-stu-id="13d71-106">Answer</span></span>                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13d71-107">我要如何確定我的 HTTPs://頁面可以與 Web 驗證訊息代理程式搭配使用？</span><span class="sxs-lookup"><span data-stu-id="13d71-107">How can I make sure that my https:// page works with the Web Authentication Broker?</span></span>                         | <span data-ttu-id="13d71-108">先嘗試在 Windows Internet Explorer 載入頁面，然後再嘗試使用 Web 驗證訊息代理程式。</span><span class="sxs-lookup"><span data-stu-id="13d71-108">Try loading the page in Windows Internet Explorer before trying it with Web Authentication Broker.</span></span> <span data-ttu-id="13d71-109">如果您的網頁載入時沒有錯誤，Web 驗證訊息代理程式也會正確地將它轉譯。</span><span class="sxs-lookup"><span data-stu-id="13d71-109">If your web page loads with no errors, it will be rendered correctly by the Web Authentication Broker as well.</span></span> |
| <span data-ttu-id="13d71-110">如果發生錯誤，將會向使用者顯示錯誤碼嗎？</span><span class="sxs-lookup"><span data-stu-id="13d71-110">In case of an error, will the error codes be displayed to the user?</span></span>                                         | <span data-ttu-id="13d71-111">當使用者顯示錯誤頁面時，不會顯示基礎錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="13d71-111">While an error page will be displayed to the user, the underlying error code is not shown.</span></span> <span data-ttu-id="13d71-112">它只會傳回給應用程式。</span><span class="sxs-lookup"><span data-stu-id="13d71-112">It is only returned to the app.</span></span> <span data-ttu-id="13d71-113">或者，您也可以使用操作記錄。</span><span class="sxs-lookup"><span data-stu-id="13d71-113">Alternately, you can also use the operational logs.</span></span>                                    |
| <span data-ttu-id="13d71-114">如何找到更多有關所遇到錯誤的詳細資料？</span><span class="sxs-lookup"><span data-stu-id="13d71-114">How can I find more details on the error encountered?</span></span>                                                       | <span data-ttu-id="13d71-115">使用操作記錄以取得詳細資料。</span><span class="sxs-lookup"><span data-stu-id="13d71-115">Use the operational logs for details.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="13d71-116">單一登入 (SSO) 應用程式容器是否與 Internet Explorer 或其他瀏覽器共用其 cookie？</span><span class="sxs-lookup"><span data-stu-id="13d71-116">Does the single sign-on (SSO) app container share its cookies with the Internet Explorer or other browsers?</span></span> | <span data-ttu-id="13d71-117">不會。</span><span class="sxs-lookup"><span data-stu-id="13d71-117">No.</span></span>                                                                                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="13d71-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="13d71-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13d71-119">網頁開發的考量</span><span class="sxs-lookup"><span data-stu-id="13d71-119">Considerations for the web page development</span></span>](considerations-for-the-web-page-development.md)
</dt> <dt>

[<span data-ttu-id="13d71-120">Web Authentication Broker SDK 範例應用程式</span><span class="sxs-lookup"><span data-stu-id="13d71-120">Web Authentication Broker SDK sample app</span></span>](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[<span data-ttu-id="13d71-121">**Windows.Security.Authentication.Web**</span><span class="sxs-lookup"><span data-stu-id="13d71-121">**Windows.Security.Authentication.Web**</span></span>](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
