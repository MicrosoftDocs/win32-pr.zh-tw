---
title: 關於結構化儲存體
description: 傳統檔案系統嘗試在一份檔中儲存多種類型的物件時，會遇到一些挑戰。
ms.assetid: a571f7c2-0490-463c-813e-de4a9fd12a2d
keywords:
- 關於結構化儲存體
- 結構化儲存體 Strctd Stg.，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d048907c196c871af943e5a15cc95b367724a31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672252"
---
# <a name="about-structured-storage"></a><span data-ttu-id="81d1e-105">關於結構化儲存體</span><span class="sxs-lookup"><span data-stu-id="81d1e-105">About Structured Storage</span></span>

<span data-ttu-id="81d1e-106">傳統檔案系統嘗試在一份檔中儲存多種類型的物件時，會遇到一些挑戰。</span><span class="sxs-lookup"><span data-stu-id="81d1e-106">Traditional file systems encounter challenges when they attempt to store efficiently multiple kinds of objects in one document.</span></span> <span data-ttu-id="81d1e-107">COM 提供一個方案：檔案內的檔案系統。</span><span class="sxs-lookup"><span data-stu-id="81d1e-107">COM provides a solution: a file system within a file.</span></span> <span data-ttu-id="81d1e-108">COM 結構化儲存體定義了如何將單一檔案實體視為兩種物件類型的結構化集合（儲存和資料流程），這些物件是以目錄和檔案的形式執行。</span><span class="sxs-lookup"><span data-stu-id="81d1e-108">COM structured storage defines how to treat a single file entity as a structured collection of two types of objects—storages and streams—that perform like directories and files.</span></span> <span data-ttu-id="81d1e-109">此配置稱為 *結構化儲存體*。</span><span class="sxs-lookup"><span data-stu-id="81d1e-109">This scheme is called *structured storage*.</span></span> <span data-ttu-id="81d1e-110">結構化儲存體的目的是要降低在一般檔案中儲存個別物件時所產生的效能處罰和負擔。</span><span class="sxs-lookup"><span data-stu-id="81d1e-110">The purpose of structured storage is to reduce the performance penalties and overhead associated with storing separate objects in a flat file.</span></span>

<span data-ttu-id="81d1e-111">本節包含結構化儲存體優點和基本概念、屬性集和非同步結構化儲存體的總覽，以及檔案系統的歷程記錄：</span><span class="sxs-lookup"><span data-stu-id="81d1e-111">This section contains an overview of structured storage benefits and fundamentals, property sets and asynchronous structured storage as well as a historical look at file systems:</span></span>

-   <span data-ttu-id="81d1e-112">複合檔案執行</span><span class="sxs-lookup"><span data-stu-id="81d1e-112">Compound file implementation</span></span>
-   <span data-ttu-id="81d1e-113">NTFS 檔案系統執行</span><span class="sxs-lookup"><span data-stu-id="81d1e-113">NTFS file system implementation</span></span>
-   <span data-ttu-id="81d1e-114">獨立執行</span><span class="sxs-lookup"><span data-stu-id="81d1e-114">Stand-alone implementation</span></span>

<span data-ttu-id="81d1e-115">本章節包含 [檔案系統](the-evolution-of-file-systems.md)、儲存 [和資料流程](storages-and-streams.md)、 [複合檔案](compound-files.md)、 [結構化儲存體基礎](structured-storage-fundamentals.md)，以及 [結構化儲存體範例](using-structured-storage.md)之演進的連結。</span><span class="sxs-lookup"><span data-stu-id="81d1e-115">This section includes links to [The Evolution of File Systems](the-evolution-of-file-systems.md), [Storages and Streams](storages-and-streams.md), [Compound Files](compound-files.md), [Structured Storage Fundamentals](structured-storage-fundamentals.md), and [Structured Storage Samples](using-structured-storage.md).</span></span>

 

 




