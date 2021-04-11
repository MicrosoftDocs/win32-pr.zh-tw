---
description: Windows 通訊端2併入了分層式通訊協定的概念：其中一個只會執行較高層級的通訊函式，同時依賴基礎傳輸堆疊來實際交換資料與遠端端點。
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: 多層通訊協定和通訊協定鏈
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113048"
---
# <a name="layered-protocols-and-protocol-chains"></a>多層通訊協定和通訊協定鏈

Windows 通訊端2併入了分層式通訊協定的概念：其中一個只會執行較高層級的通訊函式，同時依賴基礎傳輸堆疊來實際交換資料與遠端端點。 這種分層式通訊協定類型的範例之一，就是將通訊協定新增至通訊端連線程式以執行驗證並建立加密配置的安全性層級。 這種安全性通訊協定通常需要基礎和可靠傳輸通訊協定（例如 TCP 或 SPX）的服務。

「 *基底* 」一詞指的是一種通訊協定，例如 TCP 或 SPX，其完全能夠執行與遠端端點的資料通訊。 多 *層式通訊* 協定是一種無法獨立的通訊協定，而 *通訊協定鏈* 則是一或多個階層式通訊協定總共串連在一起，並由基本通訊協定錨定。

如果您設計多層式通訊協定，以在其上和下邊緣支援 Windows 通訊端 2 SPI，您可以建立通訊協定鏈。 特殊的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構指的是整個通訊協定鏈，並描述分層通訊協定的明確順序。 下圖將說明這一點。 由於應用程式只能使用基本通訊協定和通訊協定鏈，因此只有在使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 函式來列舉已安裝的通訊協定時，才會列出它們。

![分層式通訊協定架構](images/ovrvw2-3.png)

 

 
