---
title: BITS 啟動類型
description: BITS 的啟動類型是延遲的自動啟動。 在 Windows Vista 之前，BITS 的啟動類型為手動。 建立 BITS 作業時，啟動類型會變更為 [自動]。 當所有工作都已完成或取消時，啟動類型會恢復為手動。
ms.assetid: 0d9ec60f-3488-4eb2-a6a2-22932fd74caf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd1ce1dcd2f939237142a0afd44e49b4b63df419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371877"
---
# <a name="bits-startup-type"></a><span data-ttu-id="95d5c-106">BITS 啟動類型</span><span class="sxs-lookup"><span data-stu-id="95d5c-106">BITS Startup Type</span></span>

<span data-ttu-id="95d5c-107">如果有作用中的 BITS 作業) 或需求開始 (（如果沒有任何作用中的作業) ），則 BITS 的 **啟動類型** 會延遲自動啟動 (。</span><span class="sxs-lookup"><span data-stu-id="95d5c-107">The **Startup Type** for BITS is delayed auto-start (if there are active BITS jobs) or demand start (if there are no active jobs).</span></span> <span data-ttu-id="95d5c-108">11月更新之前的 Windows 版本只使用延遲的自動啟動類型，Vista 之前的版本使用手動啟動類型。</span><span class="sxs-lookup"><span data-stu-id="95d5c-108">Versions of Windows prior to the November Update used only the delayed auto-start startup type; versions prior to Vista used the manual startup type.</span></span>

<span data-ttu-id="95d5c-109">您不應該將 **啟動類型** 設定為停用。</span><span class="sxs-lookup"><span data-stu-id="95d5c-109">You should not set the **Startup Type** to Disabled.</span></span> <span data-ttu-id="95d5c-110">停用 BITS 可能會中斷依賴 BITS 來傳送檔案的應用程式。</span><span class="sxs-lookup"><span data-stu-id="95d5c-110">Disabling BITS may break applications that rely on BITS to transfer files.</span></span>

 

 




