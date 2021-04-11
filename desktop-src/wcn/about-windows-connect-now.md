---
title: 關於 Windows Connect Now
description: Windows Connect Now (的 WCN) 提供簡單且安全的機制，可用於網路存取點和裝置， (像是印表機、攝影機和電腦) 連接和交換設定。
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093144"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="49d28-103">關於 Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="49d28-103">About Windows Connect Now</span></span>

<span data-ttu-id="49d28-104">Windows Connect Now (的 WCN) 提供簡單且安全的機制，可用於網路存取點和裝置， (像是印表機、攝影機和電腦) 連接和交換設定。</span><span class="sxs-lookup"><span data-stu-id="49d28-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="49d28-105">此 API 是 Microsoft 針對 Wi-Fi 受保護的設定 (WPS) /Wi-Fi 簡單設定 (WSC) 通訊協定，這是由 Wi-Fi 聯盟所建立，作為家用網路和小型企業的解決方案。</span><span class="sxs-lookup"><span data-stu-id="49d28-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="49d28-106">這項技術並非適用于企業案例。</span><span class="sxs-lookup"><span data-stu-id="49d28-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="49d28-107">版本 1.0 h 與第2版之間的規格名稱有所變更。</span><span class="sxs-lookup"><span data-stu-id="49d28-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="49d28-108">1.0 版 h 規格的名稱 Wi-Fi 受保護的設定 (WPS) 。</span><span class="sxs-lookup"><span data-stu-id="49d28-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="49d28-109">從第2版規格開始，此規格會命名為 Wi-Fi Simple Configuration (WSC) 。</span><span class="sxs-lookup"><span data-stu-id="49d28-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="49d28-110">在我們的檔中，將會交替使用 WPS 和 WSC 條款，除非另行注明。</span><span class="sxs-lookup"><span data-stu-id="49d28-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="49d28-111">Windows Connect Now 可讓應用程式使用函式 [探索 API](/previous-versions/windows/desktop/fundisc/fd-portal)來搜尋具有 WCN 功能的裝置。</span><span class="sxs-lookup"><span data-stu-id="49d28-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="49d28-112">搜尋範圍可以縮小為特定的 SSID、狀態、類別，甚至是放寬了，以包含所有支援 WCN 的裝置。</span><span class="sxs-lookup"><span data-stu-id="49d28-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="49d28-113">一旦找到裝置之後，WCN API 就會允許與支援 WCN 的裝置進行通訊，以加速設定或連接。</span><span class="sxs-lookup"><span data-stu-id="49d28-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 