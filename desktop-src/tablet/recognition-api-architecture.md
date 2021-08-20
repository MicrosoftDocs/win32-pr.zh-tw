---
description: 啟用筆墨的應用程式會透過 Tablet PC 平臺 Api 與辨識系統通訊。
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: 辨識 API 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59775658bcda2ecafd142476e6ff48ccdda2e82b31af62d5f49b218513f9b326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966889"
---
# <a name="recognition-api-architecture"></a>辨識 API 架構

啟用筆墨的應用程式會透過 Tablet PC 平臺 Api 與辨識系統通訊。 應用程式會使用 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件來完成此動作。 Tablet PC 平臺會使用本節所述的 C 樣式介面，與您的辨識器互動。 在下圖中，虛線內的區域會顯示本節所述的內容。

![已反白顯示辨識器的辨識架構圖例](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

自訂辨識器必須包含預設安裝在 C： \\ Program Files \\ MICROSOFT Tablet PC Platform SDK 中的 Recapis (， \\ 包括) 。 除非另有說明，否則您的動態連結程式庫 (DLL) 必須匯出所有 API 函式，即使您選擇讓其中一部分傳回 E >notimpl 亦同 \_ 。

在任何情況下，您的辨識器會直接由啟用筆墨的應用程式呼叫。 相反地，應用程式會呼叫自動化 Api 或受控 Api，以從您的辨識器取得結果。

 

 



