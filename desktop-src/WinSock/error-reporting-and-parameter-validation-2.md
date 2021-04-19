---
description: 錯誤報表的配置與 SPI 和 API 介面不同。
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: 錯誤報表和參數驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970604"
---
# <a name="error-reporting-and-parameter-validation"></a>錯誤報表和參數驗證

錯誤報表的配置與 SPI 和 API 介面不同。 Windows 通訊端服務提供者會報告錯誤以及傳回的函式，而不是在 API 中使用的每個執行緒方法。 Ws2 \_32.dll 會使用服務提供者的個別函式錯誤碼，來更新透過 [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API 函式取得的每個執行緒錯誤值。 不過，仍需要服務提供者，才能維持以每一通訊端為基礎的錯誤，此錯誤可透過「 \_ 錯誤通訊端」選項來抓取。

Ws2 \_32.dll 只會在完全實作為其本身的函式呼叫上執行參數驗證。 服務提供者負責執行所有自己的參數驗證。

 

 



