---
title: 遠端資料服務已移除
description: 遠端資料服務伺服器元件已在 Windows 8 中移除
ms.assetid: 53ECB92C-8868-4A1A-82BD-4ADE75F7BB59
keywords:
- RDS 伺服器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b6588b029fe37f1312c709be168fd695bdc5738
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103933681"
---
# <a name="remote-data-service-server-components-are-removed-in-windows-8"></a><span data-ttu-id="16f83-104">遠端資料服務伺服器元件已在 Windows 8 中移除</span><span class="sxs-lookup"><span data-stu-id="16f83-104">Remote data service server components are removed in Windows 8</span></span>

## <a name="platforms"></a><span data-ttu-id="16f83-105">平台</span><span class="sxs-lookup"><span data-stu-id="16f83-105">Platforms</span></span>

 <span data-ttu-id="16f83-106">**客戶** 端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="16f83-106">**Clients** - Windows 8</span></span>  
<span data-ttu-id="16f83-107">**伺服器** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="16f83-107">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="16f83-108">Description</span><span class="sxs-lookup"><span data-stu-id="16f83-108">Description</span></span>

<span data-ttu-id="16f83-109">Windows 8 中無法使用 (RDS) server 的遠端資料服務：</span><span class="sxs-lookup"><span data-stu-id="16f83-109">The remote data service (RDS) server is not available in Windows 8:</span></span>

-   <span data-ttu-id="16f83-110">會移除裝載預設「商務物件」 RDSServer 的檔案 msadcf.dll，並移除其相關聯的檔案 (msadcfr.dll、msadcfr.dll mui、處理 .reg 和 handsafe .reg) </span><span class="sxs-lookup"><span data-stu-id="16f83-110">File msadcf.dll, which hosts the default "business object" RDSServer.DataFactory, is removed, and its associated files (msadcfr.dll, msadcfr.dll.mui, handler.reg and handsafe.reg) are removed</span></span>
-   <span data-ttu-id="16f83-111">檔案 msdfmap.dll （這是預設處理常式）已移除，並移除檔案 msdfmap.ini</span><span class="sxs-lookup"><span data-stu-id="16f83-111">File msdfmap.dll, which is the default Handler, is removed, and the file msdfmap.ini is removed</span></span>
-   <span data-ttu-id="16f83-112">檔案 msadcs.dll （ISAPI）已移除</span><span class="sxs-lookup"><span data-stu-id="16f83-112">File msadcs.dll, the ISAPI, is removed</span></span>

## <a name="manifestation"></a><span data-ttu-id="16f83-113">表現</span><span class="sxs-lookup"><span data-stu-id="16f83-113">Manifestation</span></span>

<span data-ttu-id="16f83-114">客戶無法在 Windows 8 上裝載 RDS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="16f83-114">Customers cannot host an RDS server on Windows 8.</span></span>

## <a name="mitigation"></a><span data-ttu-id="16f83-115">降低</span><span class="sxs-lookup"><span data-stu-id="16f83-115">Mitigation</span></span>

<span data-ttu-id="16f83-116">客戶可以將 RDS 伺服器保留在 Windows 7 或其他舊版作業系統的電腦上。</span><span class="sxs-lookup"><span data-stu-id="16f83-116">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="solution"></a><span data-ttu-id="16f83-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="16f83-117">Solution</span></span>

<span data-ttu-id="16f83-118">客戶可以將 RDS 伺服器保留在 Windows 7 或其他舊版作業系統的電腦上。</span><span class="sxs-lookup"><span data-stu-id="16f83-118">Customers can keep their RDS server on a machine with Windows 7 or other down-level operating systems.</span></span>

## <a name="resources"></a><span data-ttu-id="16f83-119">資源</span><span class="sxs-lookup"><span data-stu-id="16f83-119">Resources</span></span>

[<span data-ttu-id="16f83-120">資料存取技術藍圖</span><span class="sxs-lookup"><span data-stu-id="16f83-120">Data Access Technologies Roadmap</span></span>](/sql/connect/connect-history?view=sqlallproducts-allversions)

 

 