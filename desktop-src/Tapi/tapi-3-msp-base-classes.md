---
description: 本檔說明 MSP 基類的設計和使用。 這些類別並不是必要的，但大部分的開發人員會發現它們簡化了針對 TAPI 3 秒新 MSPI 建立以 DirectShow 為基礎之 MSP 的工作。
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: TAPI 3 MSP 基類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34d4f9f67618c3637bfaff149773ab7b0de4b93f33c8bca8e5eb892527735e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012338"
---
# <a name="tapi-3-msp-base-classes"></a>TAPI 3 MSP 基類

本檔說明 MSP 基類的設計和使用。 這些類別並不是必要的，但大部分的開發人員會發現它們簡化了針對 TAPI 3 的新 MSPI 建立以 DirectShow 為基礎之 MSP 的工作。

MSP 基礎類別的原始程式碼可在平臺軟體發展工具組 (SDK) 的範例目錄中找到。

假設您熟悉 COM、ATL、DirectShow 和 c + +。 讀者也必須知道 [媒體服務提供者 (MSP) ](about-the-media-service-provider-msp-.md) 和 [媒體服務提供者介面 (MSPI) ](media-service-provider-interface-mspi-.md)中的一般內容。

Windows 2000 需要 ATL 2.1。 從 Windows XP 開始，ATL 2.1 和3.0 都會編譯。

 (可以在 SDK) 中取得 MSP 基礎類別庫：

-   Mspbase .lib
-   Mspid .lib
-   Strmbase .lib
-   Tmuid .lib
    > [!Note]  
    > 應該使用動態而非靜態連結。

     

 (在 SDK) 提供的 MSP 基類標頭檔：

-   Mspaddr。h
-   Mspbase。h
-   Mspcall。h
-   Msplog。h
-   Mspstrm。h
-   Mspterm。h
-   Mspthrd。h
-   Msptmac。h
-   Msptmvc。h
-   Msptrmvc。h
-   Msptrmac。h
-   Msptrmar。h
-   Msputils。h

 (可在 SDK 範例中使用的 MSP 基礎類別來源檔案) ：

-   Mspaddr .cpp
-   Mspcall .cpp
-   Msplog .cpp
-   Mspstrm .cpp
-   Mspterm .cpp
-   Mspthrd .cpp
-   Msptrmac .cpp
-   Msptrmar .cpp
-   Msptrmvc .cpp
-   Msputils .cpp

 

 



