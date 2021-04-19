---
description: 列印多工緩衝處理器會監視目前的列印工作和目標印表機，以判斷列印工作的適當時間。
ms.assetid: c3ce7c63-b72d-4e91-9509-5189f2ccac8a
title: 列印處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bcb7ed062b4e03069201d3ec1faa0ee427f0973
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983620"
---
# <a name="print-processor"></a><span data-ttu-id="52cd6-103">列印處理器</span><span class="sxs-lookup"><span data-stu-id="52cd6-103">Print Processor</span></span>

<span data-ttu-id="52cd6-104">列印多工緩衝處理器會監視目前的列印工作和目標印表機，以判斷列印工作的適當時間。</span><span class="sxs-lookup"><span data-stu-id="52cd6-104">The print spooler monitors the current print jobs and the target printer to determine an appropriate time to print a job.</span></span> <span data-ttu-id="52cd6-105">當多工緩衝處理器判斷出應該列印工作之後，就會呼叫列印處理器。</span><span class="sxs-lookup"><span data-stu-id="52cd6-105">Once the spooler determines that a job should be printed, it calls the print processor.</span></span> <span data-ttu-id="52cd6-106">列印處理器是處理列印工作資料的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="52cd6-106">The print processor is a plug-in that processes print job data.</span></span>

<span data-ttu-id="52cd6-107">使用下列功能來處理列印處理器。</span><span class="sxs-lookup"><span data-stu-id="52cd6-107">Use the following functions to work with print processors.</span></span>



| <span data-ttu-id="52cd6-108">函式</span><span class="sxs-lookup"><span data-stu-id="52cd6-108">Function</span></span>                                                           | <span data-ttu-id="52cd6-109">描述</span><span class="sxs-lookup"><span data-stu-id="52cd6-109">Description</span></span>                                                          |
|--------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="52cd6-110">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="52cd6-110">**AddPrintProcessor**</span></span>](addprintprocessor.md)                     | <span data-ttu-id="52cd6-111">在指定的伺服器上安裝列印處理器。</span><span class="sxs-lookup"><span data-stu-id="52cd6-111">Installs a print processor on a specified server.</span></span>                    |
| [<span data-ttu-id="52cd6-112">**DeletePrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="52cd6-112">**DeletePrintProcessor**</span></span>](deleteprintprocessor.md)               | <span data-ttu-id="52cd6-113">從指定的伺服器移除印表機處理器。</span><span class="sxs-lookup"><span data-stu-id="52cd6-113">Removes a printer processor from a specified server.</span></span>                 |
| [<span data-ttu-id="52cd6-114">**EnumPrintProcessorDatatypes**</span><span class="sxs-lookup"><span data-stu-id="52cd6-114">**EnumPrintProcessorDatatypes**</span></span>](enumprintprocessordatatypes.md) | <span data-ttu-id="52cd6-115">列舉指定的列印處理器支援的資料類型。</span><span class="sxs-lookup"><span data-stu-id="52cd6-115">Enumerates the data types that a specified print processor supports.</span></span> |
| [<span data-ttu-id="52cd6-116">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="52cd6-116">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)                 | <span data-ttu-id="52cd6-117">列舉安裝在指定伺服器上的列印處理器。</span><span class="sxs-lookup"><span data-stu-id="52cd6-117">Enumerates the print processors installed on a specified server.</span></span>     |
| [<span data-ttu-id="52cd6-118">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="52cd6-118">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)   | <span data-ttu-id="52cd6-119">取得指定伺服器上列印處理器的路徑。</span><span class="sxs-lookup"><span data-stu-id="52cd6-119">Retrieves the path for the print processor on the specified server.</span></span>  |



 

 

 



