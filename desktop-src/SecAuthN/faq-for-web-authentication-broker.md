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
# <a name="faq-for-web-authentication-broker"></a>Web 驗證訊息代理程式的常見問題

Web 驗證訊息代理程式的常見問題。



| 問題                                                                                                    | Answer                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 我要如何確定我的 HTTPs://頁面可以與 Web 驗證訊息代理程式搭配使用？                         | 先嘗試在 Windows Internet Explorer 載入頁面，然後再嘗試使用 Web 驗證訊息代理程式。 如果您的網頁載入時沒有錯誤，Web 驗證訊息代理程式也會正確地將它轉譯。 |
| 如果發生錯誤，將會向使用者顯示錯誤碼嗎？                                         | 當使用者顯示錯誤頁面時，不會顯示基礎錯誤碼。 它只會傳回給應用程式。 或者，您也可以使用操作記錄。                                    |
| 如何找到更多有關所遇到錯誤的詳細資料？                                                       | 使用操作記錄以取得詳細資料。                                                                                                                                                                             |
| 單一登入 (SSO) 應用程式容器是否與 Internet Explorer 或其他瀏覽器共用其 cookie？ | 不會。                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網頁開發的考量](considerations-for-the-web-page-development.md)
</dt> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
