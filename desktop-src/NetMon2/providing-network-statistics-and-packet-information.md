---
description: 網路封包提供者 (NPP) 是與網路監視器驅動程式進行通訊的 DLL，並提供網路統計資料和封包資料。
ms.assetid: ee258bf7-7894-458d-b418-57a19ac985f2
title: 提供網路統計資料和封包資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c68be6b5b0db1fae2c19f5bc44e6e94a54c63b21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978268"
---
# <a name="providing-network-statistics-and-packet-information"></a><span data-ttu-id="41582-103">提供網路統計資料和封包資訊</span><span class="sxs-lookup"><span data-stu-id="41582-103">Providing Network Statistics and Packet Information</span></span>

<span data-ttu-id="41582-104">網路封包提供者 (NPP) 是與網路監視器驅動程式進行通訊的 DLL，並提供網路統計資料和封包資料。</span><span class="sxs-lookup"><span data-stu-id="41582-104">The Network Packet Provider (NPP) is a DLL that communicates with the Network Monitor driver and provides network statistics and packet data.</span></span>

<span data-ttu-id="41582-105">使用 NPP 的最常見方式包括：</span><span class="sxs-lookup"><span data-stu-id="41582-105">The most common ways to use the NPP include:</span></span>

-   <span data-ttu-id="41582-106">網路統計資料。</span><span class="sxs-lookup"><span data-stu-id="41582-106">Network statistics.</span></span>
-   <span data-ttu-id="41582-107">即時傳遞至應用程式的畫面格。</span><span class="sxs-lookup"><span data-stu-id="41582-107">Frames passed to the application in real time.</span></span>
-   <span data-ttu-id="41582-108">只有在停用 capture 之後才可存取的封包。</span><span class="sxs-lookup"><span data-stu-id="41582-108">Packets accessible only after the capture has been stopped.</span></span>

<span data-ttu-id="41582-109">本節包含下列主題：</span><span class="sxs-lookup"><span data-stu-id="41582-109">This section includes the following topics:</span></span>

-   [<span data-ttu-id="41582-110">選取 NIC</span><span class="sxs-lookup"><span data-stu-id="41582-110">Selecting a NIC</span></span>](selecting-a-nic-using-getnppblobfromui.md)
-   [<span data-ttu-id="41582-111">使用 GetNPPBlobTable</span><span class="sxs-lookup"><span data-stu-id="41582-111">Using GetNPPBlobTable</span></span>](using-getnppblobtable.md)

 

 



