---
description: 藉由執行認證提供者來自訂 Winlogon 行為。
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: 自訂 Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10b2ae1e029bb741a2402a25d8e51f331fdd1cac1e9918dfef3b35b36c8e6d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008656"
---
# <a name="customizing-winlogon"></a>自訂 Winlogon

藉由執行認證提供者來自訂 [*Winlogon*](/windows/desktop/SecGloss/w-gly) 行為。 如需認證提供者的詳細資訊，請參閱 [**ICredentialProvider 介面**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider)。

**Windows Server 2003 和 Windows XP：** 不支援認證提供者。

下列各節說明在 Windows Vista 之前的 Windows 版本中自訂 Winlogon 的方式。

> [!Note]  
> Windows Vista 會忽略 GINA dll 和 Winlogon 通知套件。

 

-   [Winlogon 通知套件](#winlogon-notification-packages)
-   [GINA 存根](#gina-stubs)
-   [GINA 鉤](#gina-hooks)

## <a name="winlogon-notification-packages"></a>Winlogon 通知套件

Winlogon 通知套件是一個 DLL，可匯出處理 Winlogon 事件的函式。 例如，當使用者登入系統時，Winlogon 會呼叫每個通知套件來提供事件的相關資訊。 如需詳細資訊，請參閱 [Winlogon 通知套件](winlogon-notification-packages.md)。

## <a name="gina-stubs"></a>GINA 存根

[*GINA*](/windows/desktop/SecGloss/g-gly)存根是自訂的 GINA DLL，它使用先前安裝的 GINA DLL 的匯出函式， (通常 MsGina.dll) 。 GINA 存根會取得先前安裝的 GINA DLL 所匯出之每個函式的指標。 每個 GINA 存根函式接著會使用適當的函式指標，在先前安裝的 GINA DLL 中呼叫對應的函式。

> [!IMPORTANT]
> 每個 GINA 存根函數都必須在先前安裝的 GINA 中呼叫對應的函式。

 

GINA 存根函式可在其一或多個匯出函式中執行額外的功能。 例如，GINA stub 的 [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) 函式可能會在呼叫 MsGina.dll 的 **WlxLoggedOutSAS** 函式之前，先檢查目前的時間。 如果目前時間是在特定範圍內，存根函式可能會顯示一則訊息，指出在該期間內不允許登入，並將 **WLX \_ SAS \_ 動作 \_ 無** 傳回給 Winlogon。 MsGina.dll 的 **WlxLoggedOutSAS** 函式只會在允許的時間週期內呼叫。

GINA 存根應用程式會透過 [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize)函式的 *pWinlogonFunctions* 參數，取得 Winlogon 支援函數的分派資料表。 GINA 存根應用程式可以使用此分派資料表來呼叫 Winlogon 支援函式。 例如，GINA 存根應用程式可以呼叫 [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify)函式，以在 [*智慧卡*](/windows/desktop/SecGloss/s-gly)插入 [*讀取器*](/windows/desktop/SecGloss/r-gly)時， (SAS) 事件時產生 [*安全的注意順序*](/windows/desktop/SecGloss/s-gly)。

如需有關建立 GINA 存根的詳細資訊，請參閱 \\ \\ 平臺軟體發展工具組的範例安全性 GINA GinaStub 目錄中的 GINA 存根範例 \\ \\) 安裝 (SDK。

> [!Note]  
> GINA 和 Winlogon 之間的所有呼叫都必須在單一線程內。

 

## <a name="gina-hooks"></a>GINA 鉤

GINA 攔截是 GINA 存根，在其 WlxInitialize 函式的 [](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize)中，會以其本身的 **WlxDialogBoxParam** 函數實作為指標，取代分派資料表中 [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support 函數的指標。 如此一來，每次先前安裝的 GINA (通常 MsGina.dll) 呼叫 **WlxDialogBoxParam** 函式時，就會呼叫 GINA 勾點所執行的函式。

GINA 攔截所執行的 [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) 函數可以取代回應特定對話方塊事件的 [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) 回呼程式。

這可讓 GINA 攔截程式完全控制 MsGina.dll 所建立之所有對話方塊的外觀和行為。

如需有關建立 GINA 攔截的詳細資訊，請參閱 \\ \\ Platform SDK 安裝的範例 Security \\ GINA \\ GinaHook 目錄中的 GINA 攔截範例。

> [!Note]  
> GINA 和 Winlogon 之間的所有呼叫都必須在單一線程內。

 

 

 
