---
title: 判斷填充碼狀態
description: 判斷填充碼狀態
ms.assetid: 8D0B633F-9117-4F90-BF8C-AC5F57FCD30B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40b830cbb4579aa2e523dfe2ec1129ed9cd10f37
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301743"
---
# <a name="determining-shim-status"></a><span data-ttu-id="4c8e4-103">判斷填充碼狀態</span><span class="sxs-lookup"><span data-stu-id="4c8e4-103">Determining shim status</span></span>

## <a name="platforms"></a><span data-ttu-id="4c8e4-104">平台</span><span class="sxs-lookup"><span data-stu-id="4c8e4-104">Platforms</span></span>

<dl> <span data-ttu-id="4c8e4-105">用戶端-Windows 8</span><span class="sxs-lookup"><span data-stu-id="4c8e4-105">Clients - Windows 8</span></span>  
<span data-ttu-id="4c8e4-106">伺服器-Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4c8e4-106">Servers - Windows Server 2012</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="4c8e4-107">Description</span><span class="sxs-lookup"><span data-stu-id="4c8e4-107">Description</span></span>

<span data-ttu-id="4c8e4-108">Windows 8 會在基於各種原因而填充應用程式時記錄事件。</span><span class="sxs-lookup"><span data-stu-id="4c8e4-108">Windows 8 logs events when apps are being shimmed for various reasons.</span></span> <span data-ttu-id="4c8e4-109">若要判斷您的應用程式是否正在填充，最簡單的方式就是檢查事件檢視器。</span><span class="sxs-lookup"><span data-stu-id="4c8e4-109">The easiest way to determine if your app is being shimmed is to check the event viewer.</span></span> <span data-ttu-id="4c8e4-110">移至 [應用程式及服務] 記錄 \\ Microsoft Windows Application-Experience 程式 \\ 遙測。</span><span class="sxs-lookup"><span data-stu-id="4c8e4-110">Go to Applications and Services Logs\\Microsoft Windows Application-Experience Program\\Telemetry.</span></span>

## <a name="mitigation"></a><span data-ttu-id="4c8e4-111">降低</span><span class="sxs-lookup"><span data-stu-id="4c8e4-111">Mitigation</span></span>

<span data-ttu-id="4c8e4-112">取得填充碼銜接的最佳方式是將可執行檔重新命名，或增加主要版本 1 (重新編譯可執行檔) 。</span><span class="sxs-lookup"><span data-stu-id="4c8e4-112">The best way to get yourself out of shimming is to rename the executable or to increase the major version by 1 (recompile the executable).</span></span>

 

 




