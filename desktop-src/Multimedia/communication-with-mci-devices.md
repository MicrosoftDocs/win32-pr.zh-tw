---
title: 與 MCI 裝置通訊
description: 與 MCI 裝置通訊
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- MCI 裝置，通訊
- MCIWndGetDeviceID 宏
- mciSendCommand 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314710"
---
# <a name="communication-with-mci-devices"></a>與 MCI 裝置通訊

每個 MCI 裝置都可以使用下列一或多個做為識別碼：

-   裝置識別碼
-   裝置名稱
-   別名
-   目前載入之內容的檔案名。

MCIWnd 提供可讓您用來取得此資訊的宏。 然後，您可以使用此資訊，透過 MCI 與 MCIWnd windows 相關聯的 MCI 裝置直接進行通訊。

您可以使用 [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) 宏來取得目前 MCI 裝置的識別碼。 MCI 裝置識別碼是識別應用程式所使用之 MCI 裝置實例的數值。 當您的應用程式使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式與 MCI 裝置進行通訊時，您的應用程式可以使用此識別碼。

若要取出目前 MCI 裝置的名稱，請使用 [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) 宏。 MCI 裝置名稱是以 null 終止的字串，可識別與 MCIWnd 視窗相關聯的裝置類型。 當您的應用程式使用 **mciSendCommand** 與 MCI 裝置通訊時，您的應用程式可以使用這個名稱。

您可以使用 [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) 宏來取得目前 MCI 裝置的別名。 當您的應用程式使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式與 MCI 裝置進行通訊時，您的應用程式可以使用此別名。

最後，您可以使用 [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) 宏取出 MCI 裝置所使用的檔案名。 檔案名會識別目前與 MCIWnd 視窗相關聯的內容。 當您的應用程式使用 **mciSendCommand** 或 **mciSendString** 與 MCI 裝置進行通訊時，您的應用程式可以使用此檔案名。

 

 