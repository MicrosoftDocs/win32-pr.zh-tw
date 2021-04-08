---
title: 允許使用者指定裝置和檔案
description: 允許使用者指定裝置和檔案
ms.assetid: cc542b56-c66e-4622-b2d1-505d31aab25b
keywords:
- MCIWndOpenDialog 宏
- MCIWndOpen 宏
- MCIWndOpenInterface 宏
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac4191f18409a1fb1f23ba3a2128b4aaed1b30e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673523"
---
# <a name="allowing-the-user-to-specify-devices-and-files"></a>允許使用者指定裝置和檔案

您可以使用 [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog)、 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)、 [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) 宏和 [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) 函式，將裝置或檔案與現有的 MCIWnd 視窗建立關聯。

若要讓應用程式的使用者選取要播放的檔案，請使用 **MCIWndOpenDialog**。 這個宏會顯示 [ **開啟** ] 對話方塊， (顯示在下列螢幕擷取畫面中) 選擇檔案，並將選取的檔案與目前的 MCIWnd 視窗產生關聯。

![mciwnd 視窗影像](images/mciwnd3.gif)

您可以讓應用程式的使用者選取要與 MCIWnd 視窗相關聯的檔案，並使用 [**GetOpenFileNamePreview**](/windows/desktop/api/Vfw/nf-vfw-getopenfilenamepreviewa) 和 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)來預覽該檔案。 **GetOpenFileNamePreview** 函式會顯示 [**開啟**] 對話方塊來選擇檔案，並讓使用者預覽 (播放) 其內容。 當您在對話方塊中指定現有檔案的名稱時， **GetOpenFileNamePreview** 會提供小型控制項讓使用者預覽檔案的內容。 您可以使用 **MCIWndOpen**，將指定的檔案（以 **GetOpenFileNamePreview** 或以另一種方式指定）與 MCIWnd 視窗建立關聯。

您也可以使用 **MCIWndOpen** 來指定要與 MCIWnd 視窗相關聯的裝置。 例如，您可以使用裝置名稱，例如 "CDAudio"。

若要將 MCIWnd 視窗與檔案介面或資料串流介面關聯到多媒體資料，請使用 [**MCIWndOpenInterface**](/windows/desktop/api/Vfw/nf-vfw-mciwndopeninterface) 宏。 如需檔案和資料流程介面的詳細資訊，請參閱 [AVIFile 函式和宏](avifile-functions-and-macros.md)。

> [!Note]  
> 在建立新檔案或裝置與 MCIWnd 視窗的關聯之前， [**MCIWndOpenDialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndopendialog) 和 [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) 會關閉目前與該視窗相關聯的任何裝置。 在使用這些宏之前，您的應用程式不需要關閉任何開啟的裝置。

 

 

 




