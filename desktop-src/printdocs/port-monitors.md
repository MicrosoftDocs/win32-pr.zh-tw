---
description: 設備磁碟機將整個日誌檔案轉換成原始裝置命令之後，已轉換命令的檔案會傳回至多工緩衝處理器。
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: 埠監視器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994381"
---
# <a name="port-monitors"></a><span data-ttu-id="bf44c-103">埠監視器</span><span class="sxs-lookup"><span data-stu-id="bf44c-103">Port Monitors</span></span>

<span data-ttu-id="bf44c-104">設備磁碟機將整個日誌檔案轉換成原始裝置命令之後，已轉換命令的檔案會傳回至多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="bf44c-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="bf44c-105">多工緩衝處理器會將這些低層級的命令傳送至監視器。</span><span class="sxs-lookup"><span data-stu-id="bf44c-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="bf44c-106">埠監視器是一個 .dll，可透過網路、透過平行埠，或透過序列埠傳送至印表機裝置來傳遞原始裝置命令。</span><span class="sxs-lookup"><span data-stu-id="bf44c-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="bf44c-107">您可以安裝自訂埠監視，以支援透過其他通訊埠傳遞裝置資料。</span><span class="sxs-lookup"><span data-stu-id="bf44c-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="bf44c-108">使用下列功能來處理埠監視器。</span><span class="sxs-lookup"><span data-stu-id="bf44c-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="bf44c-109">函式</span><span class="sxs-lookup"><span data-stu-id="bf44c-109">Function</span></span>                               | <span data-ttu-id="bf44c-110">描述</span><span class="sxs-lookup"><span data-stu-id="bf44c-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf44c-111">**AddMonitor**</span><span class="sxs-lookup"><span data-stu-id="bf44c-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="bf44c-112">安裝本機埠監視器，並連結設定、資料和監視檔案。</span><span class="sxs-lookup"><span data-stu-id="bf44c-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="bf44c-113">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="bf44c-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="bf44c-114">移除 [**AddMonitor**](addmonitor.md) 函式所新增的埠監視器。</span><span class="sxs-lookup"><span data-stu-id="bf44c-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="bf44c-115">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="bf44c-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="bf44c-116">列舉安裝在指定伺服器上的埠監視器。</span><span class="sxs-lookup"><span data-stu-id="bf44c-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



