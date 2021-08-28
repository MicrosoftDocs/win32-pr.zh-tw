---
title: 安裝和頁面載入問題
description: 安裝和頁面載入問題
ms.assetid: 1611c3f1-0411-4631-a64c-e7637fc7edd9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77fb7a41578463364837281dffcdfb22177e9785673049a65f05e9d0e33240e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119358858"
---
# <a name="installation-and-page-loading-problems"></a>安裝和頁面載入問題

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

### <a name="when-i-attempt-to-install-microsoft-agent-on-microsoft-windows-nt-i-get-a-message-indicating-that-i-need-to-be-an-administrator"></a>當我嘗試在 microsoft Windows NT 上安裝 microsoft Agent 時，我收到一則訊息，指出我必須是系統管理員。

因為 Microsoft 代理程式在安裝時將檔案寫入您的系統目錄，所以您必須擁有系統管理員 (而不是使用者) 的許可權才能安裝。

### <a name="when-i-attempt-to-install-microsoft-agent-i-get-one-of-the-following-errors-process-regsvr32-s-windowsmsagentagentctldll-error-while-creating-this-file-cannot-find-this-file-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows-a-required-dll-msvcrtdll-was-not-found-error-creating-process-cwindowsmsagentagentsvrexe-regserver-reason-one-of-the-library-files-needed-to-run-this-application-cannot-be-found-note-the-directory-location-cited-in-the-error-message-varies-depending-on-how-you-installed-windows"></a>當我嘗試安裝 Microsoft Agent 時，出現下列其中一個錯誤：進程 (Regsvr32/s windows \\ msagent \\AgentCtl.dll) 。 建立此檔案時發生錯誤。 找不到此檔案。  (注意：錯誤訊息中所述的目錄位置會根據您安裝 Windows 的方式而有所不同。 ) 找不到必要的 DLL MSVCRT.DLL。 建立進程時發生錯誤 <c： \\ windows \\ msagent \\agentsvr.exe/regserver>。 原因：找不到執行此應用程式所需的程式庫檔案之一。  (附注：錯誤訊息中所提及的目錄位置會根據您安裝 Windows 的方式而有所不同。 ) 

安裝 Microsoft Agent 需要適當安裝 Regsvr32.exe、Msvcrt.dll (Microsoft C 執行時間程式庫) ，以及最新的 OLE dll。 請參閱 DCOM update： (<https://docs.microsoft.com/openspecs/windows_protocols/ms-dcom/4a893f3d-bd29-48cd-9f43-d9777a4415b0>) 。 確保所有正確的系統檔案都存在的最佳方式，就是安裝 [Microsoft Internet Explorer 4.0](https://www.microsoft.com/ie/download) 或更新版本。

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-a-scripting-error-vbscript-runtime-error-object-required"></a>當我嘗試載入為 Microsoft Agent 編寫腳本的頁面時，出現腳本錯誤：「VBScript 執行時間錯誤，需要物件。」

下列其中一種情況可能會導致訊息顯示：

-   您必須設定 Microsoft Internet Explorer 的安全性選項，才能啟用 ActiveX 控制項和外掛程式。檢查瀏覽器的安全性頁面。 在 Microsoft Internet Explorer 中，開啟 [View] 功能表，選擇 [選項]，按一下 [[安全性] 索引標籤]，並確定已核取 [啟用 ActiveX 控制項和 Plug-Ins] 核取方塊。
-   您正在雙開機 Windows 9x 或 Windows NT 系統上執行，而且您已在一個作業系統上安裝 Microsoft 代理程式，但嘗試從其他作業系統存取該頁面。 雖然作業系統可能會共用目錄和檔案，但 Microsoft 代理程式所使用的登錄資訊並不是共用的，所以您必須在用來存取以該字元編寫腳本之網頁的作業系統上安裝 Microsoft 代理程式。

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-nothing-happens"></a>當我嘗試載入為 Microsoft Agent 編寫腳本的頁面時，不會發生任何事。

如果下列其中一個條件存在，就會發生這種情況：

-   檢查瀏覽器的安全性選項。 您必須設定瀏覽器來啟用 ActiveX 腳本的載入，以及 ActiveX 控制項的播放。
-   如果您要存取使用 Microsoft Agent 編寫腳本的頁面，並使用 Microsoft Internet Explorer，您必須擁有3.02 版或更新版本， (在) 下載最新版的 Internet Explorer [https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx) <https://www.microsoft.com/windows/ie/> 。 在 Microsoft Internet Explorer 中，開啟 [View] 功能表，選擇 [選項]，按一下 [[安全性] 索引標籤]，然後選取 [所有活動內容] 核取方塊。
-   頁面上的 JAVA applet 也會造成這個錯誤。 若要在與 JAVA 小程式相同的頁面上執行 Microsoft 代理程式，必須有2.0 版的 Microsoft 虛擬機器 (VM) 。 如需詳細資訊，請參閱程式 [設計/腳本常見問題](programming-scripting-faq.yml)。

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-unable-to-initialize-microsoft-agent"></a>當我嘗試載入為 Microsoft Agent 編寫腳本的頁面時，出現「無法初始化 Microsoft Agent」訊息。

當您沒有 Microsoft Agent 或頁面使用的其他控制項時，通常會發生這種情況，當系統提示您安裝控制項時，請選擇 [否]。 請嘗試重新整理頁面，但只有在您安裝所需的所有元件時，頁面才能運作。

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-i-get-the-message-the-component-has-been-digitally-signed-by-its-publisher-but-the-signature-does-not-match-the-component-it-is-possible-that-this-component-has-been-damaged-or-tampered-with-do-you-want-to-continue"></a>當我嘗試載入為 Microsoft Agent 編寫腳本的頁面時，我收到「元件已經過數位簽署」的發行者，但簽章不符合元件的訊息。 此元件可能已損毀或遭篡改？ 您要繼續嗎？」

如果您嘗試在 Microsoft Internet Explorer 3.02 上安裝 Microsoft 代理程式，可能會出現這種情況。 您可以繼續安裝，或將您的瀏覽器更新為 Internet Explorer 4.0 或更新版本。

### <a name="when-i-attempt-to-load-a-page-scripted-for-microsoft-agent-using-netscape-navigator-or-other-internet-browsers-i-get-errors"></a>當我嘗試使用 Netscape Navigator (或其他網際網路瀏覽器) 來為 Microsoft Agent 載入腳本時，我收到錯誤。

Microsoft 代理程式是使用 ActiveX 介面來執行。 您只能將它用於瀏覽器 (例如，支援透過頁面上的腳本內嵌 ActiveX 物件的 microsoft Internet Explorer) ，且僅適用于執行 Microsoft Windows 95、Windows 98 和 Windows NT 4.0 (或更新版本) 的系統。 如果您不是使用 Microsoft Internet Explorer ([https://www.microsoft.com/windows/ie/](https://www.microsoft.com/windows/internet-explorer/default.aspx)) ，請洽詢您的瀏覽器廠商以取得 ActiveX 支援的詳細資訊。

 

 




