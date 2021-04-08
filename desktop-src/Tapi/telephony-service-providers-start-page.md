---
description: 電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制項。
ms.assetid: 276c27ac-b6ee-42a7-8327-33dfd87e69bd
title: 電話語音服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40c3c8887723cc74a1bf0d77bcdcfd06c8468a4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852028"
---
# <a name="telephony-service-providers"></a>電話語音服務提供者

## <a name="purpose"></a>目的

電話語音服務提供者 (TSP) 是動態連結程式庫 (DLL) ，可透過一組匯出的服務功能來支援通訊裝置控制項。 TAPI 應用程式使用標準化的命令、TAPI 會將資訊傳遞給電話語音服務提供者，而 TSP 則會處理必須與裝置交換的特定命令。

TSP 必須符合電話語音服務提供者介面 (TSPI) ，才能以 Microsoft 電話語音環境內的服務提供者形式運作。 TSPI 會定義由通訊設備提供的電話語音服務提供者所公開的外部函數。

## <a name="developer-audience"></a>開發人員對象

您可以用多種語言撰寫啟用 TAPI 的應用程式，包括 JAVA、Visual Basic 和 C/c + +。 使用電信或其他電話語音應用程式的先前開發經驗很有説明，但並非必要。

## <a name="run-time-requirements"></a>執行階段需求求

TSPI 可讓您開發所有 Windows 版本的 Tsp。

## <a name="in-this-section"></a>本節內容



| 主題                                                                | 描述                                                              |
|----------------------------------------------------------------------|--------------------------------------------------------------------------|
| [概觀](about-the-telephony-service-provider-tsp-.md)<br/> | 關於 TSPI 架構和元件的一般資訊。<br/> |
| [參考](tspi-reference.md)<br/>                           | TSPI 介面的檔。<br/>                        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Microsoft 電話語音總覽](./microsoft-telephony-overview.md)
</dt> <dt>

[媒體服務提供者](./media-service-providers-start-page.md)
</dt> <dt>

[TAPI 2。2](./tapi-2-2-start-page.md)
</dt> <dt>

[TAPI 3。1](./tapi-3-1-start-page.md)
</dt> </dl>

 

