---
description: Winsock 提供服務提供者介面，用來建立 Winsock 服務，通常稱為 Winsock SPI。
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: 關於 Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f321aabfd6345e3209414f96dedfaca4b9ab0acfa1629d49883a72ab8199cfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996938"
---
# <a name="about-the-winsock-spi"></a>關於 Winsock SPI

Winsock 提供服務提供者介面，用來建立 Winsock 服務，通常稱為 Winsock SPI。 有兩種類型的服務提供者存在：傳輸提供者和命名空間提供者。 傳輸提供者的範例包括通訊協定堆疊（例如 TCP/IP 或 IPX/SPX），而命名空間提供者的範例是網際網路網域命名系統 (DNS) 的介面。 服務提供者介面規格的個別區段適用于每種類型的服務提供者。

[傳輸](transport-service-providers-2.md) 和 [命名空間](name-space-service-providers-2.md) 服務提供者必須在 \_ 安裝時向 Ws232.dll 註冊。 此註冊只需要針對每個提供者執行一次，因為必要的資訊會保留在持續性儲存體中。

 

 



