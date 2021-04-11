---
description: 下圖顯示專家和剖析器應用程式之間的關聯性，以及網路監視器架構的其他元件之間的關聯性。
ms.assetid: f943f0e6-5fdc-48f9-ba5d-5effdf8229f3
title: 專家和剖析器架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caa8477d97604acfb04686170ca6cb5cff8116a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112245"
---
# <a name="expert-and-parser-architecture"></a><span data-ttu-id="feb64-103">專家和剖析器架構</span><span class="sxs-lookup"><span data-stu-id="feb64-103">Expert and Parser Architecture</span></span>

<span data-ttu-id="feb64-104">下圖顯示 [專家](experts.md) 和剖析器應用程式之間的關聯 [性，以及](parsers.md) 網路監視器架構的其他元件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="feb64-104">The following figure shows the relationship between [expert](experts.md) and [parser](parsers.md) applications and other components of the Network Monitor architecture.</span></span>

![專家和剖析器應用程式之間的關聯性](images/nm-arch1.png)

<span data-ttu-id="feb64-106">從 NDIS 驅動程式收集網路流量，作為個別的畫面。</span><span class="sxs-lookup"><span data-stu-id="feb64-106">The network traffic is collected, as individual frames, from the NDIS driver.</span></span> <span data-ttu-id="feb64-107">網路監視器驅動程式 (Nmnt.sys) 接著將框架路由傳送到網路封包提供者 (NPP) ，這會捕捉資料並將其放在一或多個 capture 檔案中。</span><span class="sxs-lookup"><span data-stu-id="feb64-107">The Network Monitor driver (Nmnt.sys) then routes the frames to a network packet provider (NPP), which captures the data and places it in one or more capture files.</span></span> <span data-ttu-id="feb64-108">NPP 是用來捕捉資料的 COM 介面集合。</span><span class="sxs-lookup"><span data-stu-id="feb64-108">The NPP is a collection of COM interfaces used to capture data.</span></span> <span data-ttu-id="feb64-109">在此情況下， [**IDelaydC**](idelaydc.md) 介面會用來執行延遲的捕獲。</span><span class="sxs-lookup"><span data-stu-id="feb64-109">In this case, the [**IDelaydC**](idelaydc.md) interface is used to perform a delayed capture.</span></span>

> [!Note]  
> <span data-ttu-id="feb64-110">NPP 用於延遲和即時的捕獲。</span><span class="sxs-lookup"><span data-stu-id="feb64-110">The NPP is used for delayed and real-time captures.</span></span> <span data-ttu-id="feb64-111">若為即時捕捉，則會使用 [**IRTC**](irtc.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="feb64-111">For real-time captures, the [**IRTC**](irtc.md) interface is used.</span></span>

 

<span data-ttu-id="feb64-112">當網路框架儲存在 capture 檔中，而且檔案可供存取時，專家和剖析器可以使用網路監視器 UI 和 Nmapi.dll 中提供的網路監視器函數來分析資料。</span><span class="sxs-lookup"><span data-stu-id="feb64-112">When the network frames are stored in the capture file and the file is accessible, experts and parsers can use the Network Monitor UI and the Network Monitor functions provided in Nmapi.dll to analyze the data.</span></span> <span data-ttu-id="feb64-113">在 capture 完成之前，無法存取 capture 檔。</span><span class="sxs-lookup"><span data-stu-id="feb64-113">Capture files are not accessible until the capture is complete.</span></span>

 

 



