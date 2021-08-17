---
description: 錯誤報表的配置與 SPI 和 API 介面不同。
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: 錯誤報表和參數驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5fdec1ee6a4cd7d052ba9f94cdf62ce7de70969a521a7023a5ca41e37f6a931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132611"
---
# <a name="error-reporting-and-parameter-validation"></a>錯誤報表和參數驗證

錯誤報表的配置與 SPI 和 API 介面不同。 Windows除了 API 中使用的每個執行緒型方法，通訊端服務提供者會回報錯誤以及傳回的函式。 Ws2 \_32.dll 會使用服務提供者的個別函式錯誤碼，來更新透過 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API 函式取得的每個執行緒錯誤值。 不過，仍需要服務提供者，才能維持以每一通訊端為基礎的錯誤，此錯誤可透過「 \_ 錯誤通訊端」選項來抓取。

Ws2 \_32.dll 只會在完全實作為其本身的函式呼叫上執行參數驗證。 服務提供者負責執行所有自己的參數驗證。

 

 



