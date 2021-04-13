---
description: 從協調3.0 或更新版本的 Windows 2000 電話語音服務提供者開始，必須有相符的媒體服務提供者。
ms.assetid: 9235c631-77bc-42c6-8139-9208c9c254b4
title: 媒體服務提供者通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a50ec6a4fb96a86ceab3a302b138ee72d6c61b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321567"
---
# <a name="media-service-provider-communication"></a>媒體服務提供者通訊

從協調3.0 或更新版本的 Windows 2000 電話語音服務提供者開始，必須有相符的媒體服務提供者。 營運責任的精確劃分是實作為相依。 例如，TSP 可能會使用相符的 MSP 來執行傳入會話的媒體類型判斷。 不過，TSP 必須符合 TSPI 的規定，這表示從 MSP 取得該判斷，並將其報告至 TAPI。

TSPI 提供下列函式和訊息，以允許 TSP 和 MSP 之間的虛擬連接：

-   [**TSPI \_ lineCloseMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [**TSPI \_ lineCreateMSPInstance**](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [**TSPI \_ lineMSPIdentify**](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [**TSPI \_ lineReceiveMSPData**](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [**行 \_ QOSINFO**](line-qosinfo.md)
-   [**行 \_ SENDMSPDATA**](line-sendmspdata.md)

 

 
