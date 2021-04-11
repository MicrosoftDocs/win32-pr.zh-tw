---
title: 可安裝的驅動程式格式
description: 可安裝的驅動程式格式
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- 可安裝的驅動程式、格式
- 可安裝的驅動程式，DriverProc 函式
- 可安裝的驅動程式，訊息
- 驅動程式訊息
- 驅動程式格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314956"
---
# <a name="installable-driver-format"></a><span data-ttu-id="4d56a-108">可安裝的驅動程式格式</span><span class="sxs-lookup"><span data-stu-id="4d56a-108">Installable Driver Format</span></span>

<span data-ttu-id="4d56a-109">每個可安裝的驅動程式都會匯出 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 函式。</span><span class="sxs-lookup"><span data-stu-id="4d56a-109">Every installable driver exports a [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function.</span></span> <span data-ttu-id="4d56a-110">這個常見的進入點函式會接收系統的 *驅動程式訊息* ，引導驅動程式執行動作或提供資訊。</span><span class="sxs-lookup"><span data-stu-id="4d56a-110">This common entry-point function receives *driver messages* from the system that direct the driver to carry out actions or provide information.</span></span> <span data-ttu-id="4d56a-111">當應用程式或 DLL 開啟或關閉驅動程式，或要求將訊息傳送至驅動程式時，系統會將驅動程式訊息傳送至 **DriverProc** 函式。</span><span class="sxs-lookup"><span data-stu-id="4d56a-111">The system sends driver messages to the **DriverProc** function when an application or DLL opens or closes the driver or requests that a message be sent to the driver.</span></span> <span data-ttu-id="4d56a-112">**DriverProc** 函式會處理訊息，或將訊息傳遞至預設的訊息處理常式，也就是 [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)函數。</span><span class="sxs-lookup"><span data-stu-id="4d56a-112">The **DriverProc** function either processes the message or passes the message to the default message handler, the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function.</span></span> <span data-ttu-id="4d56a-113">無論是哪一種情況， **DriverProc** 都必須傳回值，指出要求的動作是否成功。</span><span class="sxs-lookup"><span data-stu-id="4d56a-113">In either case, **DriverProc** must return a value indicating whether the requested action was successful.</span></span>

 

 