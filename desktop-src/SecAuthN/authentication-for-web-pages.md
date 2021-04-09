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
# <a name="authentication-for-web-pages"></a>Web 網頁驗證

驗證正在證明您的身分。

**目標：** 讓 web 驗證訊息代理程式顯示為應用程式的一部分。

## <a name="prerequisites"></a>必要條件

無

**完成時間：** 15 分鐘。

## <a name="instructions"></a>指示

### <a name="1-getting-started"></a>1.開始使用

啟動安裝程式檔案，在本機電腦上的 Internet Information Services 8 中安裝 Contoso 網站，以裝載範例 HTML 和 CSS 檔案。

1.  範例 HTML 和 CSS 檔案將會安裝至 Microsoft Contoso 底下的 program files 目錄 \\ 。
2.  此外，「Fabrikam 社交」 Windows Store 應用程式將會解除封裝至桌面。

### <a name="2-getting-familiar"></a>2. 熟悉

若要瞭解範例頁面在 Web 驗證訊息代理程式中的外觀，請在桌面上的 "Fabrikam 社交" 資料夾中開啟 Fabrikam 社交 Visual Studio 11 方案檔。

1.  執行應用程式並按 [啟動]，以顯示 Web 驗證訊息代理程式中的範例頁面。
2.  您可以藉由將某些資料共用至應用程式，將應用程式調整為一側或啟用。

### <a name="3-authentication"></a>3. 驗證

基礎應用程式叫用 Web 驗證 API 來連線至提供者 "Contoso Social" 時，會顯示登入頁面。 此頁面的設計最適合快速且流暢的登入體驗。 它也提供一些其他常見使用者動作的進入點，例如：抓取密碼詳細資料、註冊帳戶，以及閱讀在瀏覽器中完成之隱私權和條款及條件的聲明。 ![contoso 登入頁面](images/wab-figure8.png)

## <a name="summary-and-next-steps"></a>摘要和後續步驟

[驗證網頁的摘要教學](tutorial-for-authenticating-web-pages.md)課程

[Web 網頁的](authorization-for-web-pages.md)下一個授權

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網頁開發的考量](considerations-for-the-web-page-development.md)
</dt> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web)
</dt> </dl>

 

 
