---
title: 遠端桌面 ActiveX 控制項隨附的範例網頁
description: 遠端桌面網頁連線安裝所在的目錄中 (Default.htm) 的範例網頁。
ms.assetid: 3137f58b-1aec-4bd6-a3b2-d1db6c8b96e4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c175bafe1ebde3367c20529a6d76d7933a42f343de56216649735c942105aa65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058536"
---
# <a name="sample-webpage-included-with-the-remote-desktop-activex-control"></a>遠端桌面 ActiveX 控制項隨附的範例網頁

當您安裝遠端桌面網頁連線的遠端桌面 ActiveX 控制項時，會將範例網頁 (Default.htm) 複製到已安裝遠端桌面網頁連線的目錄。 此頁面可以依原樣執行或自訂，以符合使用者或組織的需求。

範例網頁必須安裝在執行 Windows server 和 Internet information server 4.0 或更新版本的 web 伺服器上。 此外，用戶端電腦上的瀏覽器應該 Internet Explorer 4.0 版或更新版本。 如需詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。

Default.htm 是預設的登入網頁，會收集使用者的連接資訊。 登入頁面包含一個必要欄位，使用者可在其中輸入要連接的遠端桌面工作階段主機 (RD 工作階段主機) 伺服器或遠端電腦的名稱。 登入頁面也包含螢幕大小和使用者登入資訊的選擇性欄位，包括使用者名稱和網域。

收集使用者資料之後，Default.htm 會將它傳遞到遠端桌面 ActiveX 控制項 () Msrdp，以起始遠端桌面會話。 初始化會話所需的步驟如下：

1.  如有必要，Internet Explorer 下載 .cab 檔案，並將它安裝在使用者的電腦上。
2.  使用者會在適當的欄位中輸入遠端電腦的完整功能變數名稱或 IP 位址。

    -   使用者可以選擇性地指定連接的螢幕大小。 如果使用者未指定螢幕大小，則會話會在全螢幕模式中開啟（如果使用者位於受信任的 URL 安全性區域中）。 否則，會話會在視窗模式中開啟。
    -   使用者可以選擇性地為遠端會話 (的使用者名稱、網域) 提供自動登入資訊。

3.  當使用者按一下 [**連線**] 按鈕時，Default.htm 會將使用者提供的資料做為參數傳遞到遠端桌面 ActiveX 控制項。
4.  遠端桌面會在瀏覽器視窗中開啟，或在全螢幕模式中開啟（由使用者所指定）。

當 Default.htm 第一次使用 Internet Explorer 開啟時，會出現一個對話方塊，讓使用者可以選擇下載遠端桌面 ActiveX 控制項 (Msrdp .ocx) 。 此對話方塊會在下列條件下出現：

-   存取網頁的電腦未完整安裝遠端桌面網頁連線用戶端 (或遠端桌面服務進階用戶端) 有 Web 支援。
-   用戶端電腦上安裝的 .cab 檔案版本比 Default.htm 網頁上的版本還舊。

顯示在瀏覽器視窗中的遠端桌面會話大小是 Default.htm 網頁中指定的大小。 若要變更螢幕大小，使用者必須從會話中斷連線、回到 Default.htm 網頁，然後編輯連接資訊。 如果未指定任何螢幕大小，則會話會在預設全螢幕模式的瀏覽器視窗中開啟。 在此解決方案中，遠端桌面會展開以符合使用者畫面的完整尺寸，而不會顯示 Internet Explorer 瀏覽器工具列和視窗框架。 如同 full 遠端桌面連線用戶端，使用者可以按全螢幕模式 [快速鍵](terminal-services-shortcut-keys.md) 組合 (CTRL + ALT + BREAK) 來切換全螢幕和視窗模式。

基於安全性理由，遠端桌面服務連線管理員中的某些可用選項會限制在遠端桌面 ActiveX 控制特定 Internet Explorer URL 安全性區域。 請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 的詳細資訊，以取得有關這些選項的詳細資訊，以及指定在連接時要執行的程式。

 

 




