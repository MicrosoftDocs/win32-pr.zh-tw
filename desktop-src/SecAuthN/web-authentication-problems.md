---
description: 本主題說明針對您的網頁使用 Web 驗證訊息代理程式 Api 的疑難排解秘訣。
ms.assetid: 25A024AA-9A70-40A5-BF5E-452FD148D0D2
title: Web 驗證問題
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f996527c58b9620b8417ac3e6cdd6e0f61bd5217
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353661"
---
# <a name="web-authentication-problems"></a>Web 驗證問題

本主題說明針對您的網頁使用 Web 驗證訊息代理程式 Api 的疑難排解秘訣。

-   [操作記錄](#operational-logs)
-   [使用 Fiddler 搭配 Web 驗證訊息代理程式](#using-fiddler-with-web-authentication-broker)
-   [相關主題](#related-topics)

## <a name="operational-logs"></a>作業記錄

通常您可以透過使用作業記錄來判斷哪裡出問題。 Microsoft Windows WebAuth 作業有專屬的事件記錄檔通道，可 \\ 讓網站開發人員瞭解 web 驗證訊息代理程式處理網頁的方式。 若要啟用它，請啟動 eventvwr.exe，並在應用程式和服務 \\ Microsoft \\ Windows WebAuth 下啟用操作記錄 \\ 。 此外，Web 驗證訊息代理程式會將唯一字串附加至使用者代理字串，以在 Web 服務器上識別其本身。 這個字串是 "MSAuthHost/1.0"。 請注意，版本號碼在日後可能會有變更，因此在程式碼中不應該依據該版本號碼。 完整使用者代理程式字串的範例如下：

`User-Agent: Mozilla/5.0 (compatible; MSIE 10.0; Windows NT 6.2; Win64; x64; Trident/6.0; MSAuthHost/1.0)`

使用操作記錄的範例

1.  啟用操作記錄
2.  執行 Contoso 社交應用程式![顯示 WebAuth 作業記錄的事件檢視器](images/wab-figure15.png)
3.  產生的記錄專案可以用來更詳細地瞭解 Web 驗證訊息代理程式的行為。 在此情況下，這些可能包括：
    -   瀏覽開始：記錄 AuthHost 何時啟動，並且包含開始和終止 URL 的相關資訊。
    -   ![說明「瀏覽開始」的詳細資料](images/wab-figure16.png)
    -   瀏覽完成：記錄網頁載入完成。
    -   Meta 標記：記錄何時遇到 meta-tag，包含詳細資料。
    -   瀏覽終止：使用者終止瀏覽。
    -   瀏覽錯誤：AuthHost 在 URL 遇到瀏覽錯誤，包含 HttpStatusCode。
    -   瀏覽結束：遇到終止 URL。

## <a name="using-fiddler-with-web-authentication-broker"></a>使用 Fiddler 搭配 Web 驗證訊息代理程式

Fiddler web 偵錯工具可以與 Windows 8 apps 搭配使用。

1.  由於 AuthHost 是在自己的 App 容器中執行以給予私人網路功能，因此您必須設定登錄機碼：Windows Registry Editor Version 5.00

    **HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **影像檔執行選項** \\ **authhost.exe** \\ **EnablePrivateNetwork** = 00000001<dl> <dt>

                     Data type
</dt> <dd>                     DWORD</dd> </dl>

2.  為 AuthHost 新增一個規則，因為它負責產生輸出流量。
    ```cmd
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.a.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
    CheckNetIsolation.exe LoopbackExempt -a -n=microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
    D:\Windows\System32>CheckNetIsolation.exe LoopbackExempt -s
    List Loopback Exempted AppContainers
    [1] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.c_8wekyb3d8bbwe
        SID:  S-1-15-2-1973105767-3975693666-32999980-3747492175-1074076486-3102532000-500629349
    [2] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.sso.p_8wekyb3d8bbwe
        SID:  S-1-15-2-166260-4150837609-3669066492-3071230600-3743290616-3683681078-2492089544
    [3] -----------------------------------------------------------------
        Name: microsoft.windows.authhost.a.p_8wekyb3d8bbwe
        SID:  S-1-15-2-3506084497-1208594716-3384433646-2514033508-1838198150-1980605558-3480344935
    ```

    

3.  將連入流量防火牆規則新增到 Fiddler。

如需詳細資訊，請參閱[使用 Fiddler web 偵錯工具搭配 Windows Store 應用程式的 Blog](/archive/blogs/fiddler/revisiting-fiddler-and-win8-immersive-applications)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[網頁開發的考量](considerations-for-the-web-page-development.md)
</dt> <dt>

[Web 驗證訊息代理程式的常見問題](faq-for-web-authentication-broker.yml)
</dt> <dt>

[Web Authentication Broker SDK 範例應用程式](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/WebAuthenticationBroker)
</dt> <dt>

[**Windows.Security.Authentication.Web**](/uwp/api/Windows.Security.Authentication.Web?view=winrt-19041&preserve-view=true)
</dt> </dl>

 

 
