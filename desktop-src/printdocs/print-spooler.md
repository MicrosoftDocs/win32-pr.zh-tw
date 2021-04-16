---
description: 列印介面的主要元件是列印多工緩衝處理器。
ms.assetid: 36ffb001-78e2-4fa0-8241-3891493ac02d
title: 列印多工緩衝處理器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfcc6ea2e46c06b5e51032a4c43f46df7f07c04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513444"
---
# <a name="print-spooler"></a><span data-ttu-id="8987a-103">列印多工緩衝處理器</span><span class="sxs-lookup"><span data-stu-id="8987a-103">Print Spooler</span></span>

<span data-ttu-id="8987a-104">列印介面的主要元件是列印多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="8987a-104">The primary component of the printing interface is the print spooler.</span></span> <span data-ttu-id="8987a-105">列印多工緩衝處理器是一個可執行檔，可管理列印程式。</span><span class="sxs-lookup"><span data-stu-id="8987a-105">The print spooler is an executable file that manages the printing process.</span></span> <span data-ttu-id="8987a-106">列印的管理包括取出正確印表機驅動程式的位置、載入該驅動程式、將高階函式呼叫緩衝處理到列印工作、排程列印工作以進行列印等等。</span><span class="sxs-lookup"><span data-stu-id="8987a-106">Management of printing involves retrieving the location of the correct printer driver, loading that driver, spooling high-level function calls into a print job, scheduling the print job for printing, and so on.</span></span> <span data-ttu-id="8987a-107">系統會在系統啟動時載入多工緩衝處理器，並繼續執行，直到作業系統關閉為止。</span><span class="sxs-lookup"><span data-stu-id="8987a-107">The spooler is loaded at system startup and continues to run until the operating system is shut down.</span></span>

<span data-ttu-id="8987a-108">列印 (DC) 的印表機建立印表機裝置內容的應用程式。</span><span class="sxs-lookup"><span data-stu-id="8987a-108">Applications that print create a printer device context (DC).</span></span> <span data-ttu-id="8987a-109">當應用程式建立印表機 DC 時，多工緩衝處理器會執行必要的工作，例如判斷所需的印表機驅動程式的位置，然後載入該驅動程式。</span><span class="sxs-lookup"><span data-stu-id="8987a-109">When an application creates a printer DC, the spooler performs necessary tasks such as determining the location of the required printer driver and then loading that driver.</span></span> <span data-ttu-id="8987a-110">列印多工緩衝處理器也會決定用來記錄列印工作的資料類型。</span><span class="sxs-lookup"><span data-stu-id="8987a-110">The print spooler also determines the data type used to record the print job.</span></span>

<span data-ttu-id="8987a-111">列印多工緩衝處理器支援下列資料類型：</span><span class="sxs-lookup"><span data-stu-id="8987a-111">The print spooler supports the following data types:</span></span>

-   <span data-ttu-id="8987a-112">增強型中繼檔 (EMF) 。</span><span class="sxs-lookup"><span data-stu-id="8987a-112">Enhanced metafile (EMF).</span></span>
-   <span data-ttu-id="8987a-113">ASCII 文字。</span><span class="sxs-lookup"><span data-stu-id="8987a-113">ASCII text.</span></span>
-   <span data-ttu-id="8987a-114">原始資料，包括印表機資料類型，例如 PostScript、PCL 和自訂資料類型。</span><span class="sxs-lookup"><span data-stu-id="8987a-114">Raw data, which includes printer data types such as PostScript, PCL, and custom data types.</span></span>

<span data-ttu-id="8987a-115">您可以藉由安裝額外的印表機驅動程式和列印處理器，將自訂資料類型新增至多工緩衝處理器。</span><span class="sxs-lookup"><span data-stu-id="8987a-115">Custom data types can be added to the spooler by installing additional printer drivers and print processors.</span></span> <span data-ttu-id="8987a-116">列印工作是在內部儲存的檔，並使用其中一種支援的資料類型進行編碼，而列印工作可包含一或多個頁面的輸出。</span><span class="sxs-lookup"><span data-stu-id="8987a-116">A print job is a document stored internally and encoded by using one of the supported data types, and a print job may contain one or more pages of output.</span></span> <span data-ttu-id="8987a-117">列印工作可能包含多個表單;例如，作業可能包含一個信封和三頁的 A4 紙張。</span><span class="sxs-lookup"><span data-stu-id="8987a-117">The print job may consist of multiple forms; for example, a job may consist of one envelope and three pages of A4 paper.</span></span> <span data-ttu-id="8987a-118">列印工作的定義 (或由 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) 和 [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) 函式) 括住。</span><span class="sxs-lookup"><span data-stu-id="8987a-118">A print job is defined (or bracketed) by the [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc) functions.</span></span>

<span data-ttu-id="8987a-119">列印工作的預設資料類型是增強的中繼檔。</span><span class="sxs-lookup"><span data-stu-id="8987a-119">The default data type for a print job is the enhanced metafile.</span></span> <span data-ttu-id="8987a-120">EMF 記錄是精簡結構，可用來儲存文字輸出命令、點陣圖形命令等等。</span><span class="sxs-lookup"><span data-stu-id="8987a-120">An EMF record is a compact structure used to store text output commands, raster graphics commands, and so on.</span></span> <span data-ttu-id="8987a-121">當應用程式呼叫 [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca)時，多工緩衝處理器會建立多工緩衝處理檔案和資料檔案，然後開始將 EMF 記錄儲存在多工緩衝處理檔案中。</span><span class="sxs-lookup"><span data-stu-id="8987a-121">When an application calls [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca), the spooler creates a spool file and a data file and begins storing EMF records in the spool file.</span></span> <span data-ttu-id="8987a-122">每次應用程式呼叫其中一個 GDI 繪圖函式時，就會建立一或多個新的 EMF 記錄，並儲存在多工緩衝處理檔案中。</span><span class="sxs-lookup"><span data-stu-id="8987a-122">Each time the application calls one of the GDI drawing functions, one or more new EMF records are created and stored in the spool file.</span></span> <span data-ttu-id="8987a-123">多工緩衝處理和資料檔案會建立在作業系統目錄中。</span><span class="sxs-lookup"><span data-stu-id="8987a-123">The spool and data files are created in an operating system directory.</span></span> <span data-ttu-id="8987a-124">多工緩衝處理器會使用多工緩衝處理檔案來儲存 EMF 記錄，並使用資料檔案來記錄表單類型、列印工作的資料類型、目標印表機等等。</span><span class="sxs-lookup"><span data-stu-id="8987a-124">The spooler uses the spool file to store EMF records and uses the data file to record the type of form, the data type for the print job, the target printer, and so on.</span></span> <span data-ttu-id="8987a-125">當工作已順利列印時，多工緩衝處理器會刪除這些檔案。</span><span class="sxs-lookup"><span data-stu-id="8987a-125">The spooler deletes these files when the job has successfully printed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8987a-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="8987a-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8987a-127">增強格式的中繼檔</span><span class="sxs-lookup"><span data-stu-id="8987a-127">Enhanced-Format Metafiles</span></span>](/windows/desktop/gdi/enhanced-format-metafiles)
</dt> </dl>

 

 
