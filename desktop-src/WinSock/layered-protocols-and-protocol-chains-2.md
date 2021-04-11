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
# <a name="layered-protocols-and-protocol-chains"></a><span data-ttu-id="7df0f-103">多層通訊協定和通訊協定鏈</span><span class="sxs-lookup"><span data-stu-id="7df0f-103">Layered Protocols and Protocol Chains</span></span>

<span data-ttu-id="7df0f-104">Windows 通訊端2併入了分層式通訊協定的概念：其中一個只會執行較高層級的通訊函式，同時依賴基礎傳輸堆疊來實際交換資料與遠端端點。</span><span class="sxs-lookup"><span data-stu-id="7df0f-104">Windows Sockets 2 incorporates the concept of a layered protocol: one that implements only higher-level communications functions while relying on an underlying transport stack for the actual exchange of data with a remote endpoint.</span></span> <span data-ttu-id="7df0f-105">這種分層式通訊協定類型的範例之一，就是將通訊協定新增至通訊端連線程式以執行驗證並建立加密配置的安全性層級。</span><span class="sxs-lookup"><span data-stu-id="7df0f-105">An example of this type of layered protocol is a security layer that adds a protocol to the socket connection process in order to perform authentication and establish an encryption scheme.</span></span> <span data-ttu-id="7df0f-106">這種安全性通訊協定通常需要基礎和可靠傳輸通訊協定（例如 TCP 或 SPX）的服務。</span><span class="sxs-lookup"><span data-stu-id="7df0f-106">Such a security protocol generally requires the services of an underlying and reliable transport protocol such as TCP or SPX.</span></span>

<span data-ttu-id="7df0f-107">「 *基底* 」一詞指的是一種通訊協定，例如 TCP 或 SPX，其完全能夠執行與遠端端點的資料通訊。</span><span class="sxs-lookup"><span data-stu-id="7df0f-107">The term *base protocol* refers to a protocol, such as TCP or SPX, that is fully capable of performing data communications with a remote endpoint.</span></span> <span data-ttu-id="7df0f-108">多 *層式通訊* 協定是一種無法獨立的通訊協定，而 *通訊協定鏈* 則是一或多個階層式通訊協定總共串連在一起，並由基本通訊協定錨定。</span><span class="sxs-lookup"><span data-stu-id="7df0f-108">A *layered protocol* is a protocol that cannot stand alone, while a *protocol chain* is one or more layered protocols strung together and anchored by a base protocol.</span></span>

<span data-ttu-id="7df0f-109">如果您設計多層式通訊協定，以在其上和下邊緣支援 Windows 通訊端 2 SPI，您可以建立通訊協定鏈。</span><span class="sxs-lookup"><span data-stu-id="7df0f-109">You can create a protocol chain if you design the layered protocols to support the Windows Sockets 2 SPI at both their upper and lower edges.</span></span> <span data-ttu-id="7df0f-110">特殊的 [**WSAPROTOCOL \_ 資訊**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) 結構指的是整個通訊協定鏈，並描述分層通訊協定的明確順序。</span><span class="sxs-lookup"><span data-stu-id="7df0f-110">A special [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure refers to the protocol chain as a whole and describes the explicit order in which the layered protocols are joined.</span></span> <span data-ttu-id="7df0f-111">下圖將說明這一點。</span><span class="sxs-lookup"><span data-stu-id="7df0f-111">This is illustrated in the figure below.</span></span> <span data-ttu-id="7df0f-112">由於應用程式只能使用基本通訊協定和通訊協定鏈，因此只有在使用 [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) 函式來列舉已安裝的通訊協定時，才會列出它們。</span><span class="sxs-lookup"><span data-stu-id="7df0f-112">Since only base protocols and protocol chains are directly usable by applications, they are the only ones listed when the installed protocols are enumerated with the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

![分層式通訊協定架構](images/ovrvw2-3.png)

 

 
