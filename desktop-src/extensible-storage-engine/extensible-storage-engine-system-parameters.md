---
description: 深入瞭解：可擴充儲存引擎系統參數
title: 可擴充儲存引擎系統參數
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512653"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="09189-103">可擴充儲存引擎系統參數</span><span class="sxs-lookup"><span data-stu-id="09189-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="09189-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="09189-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="09189-105">可擴充儲存引擎系統參數</span><span class="sxs-lookup"><span data-stu-id="09189-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="09189-106">下列常數會當做 [JetGetSystemParameter](./jetgetsystemparameter-function.md)和 [JetSetSystemParameter](./jetsetsystemparameter-function.md)函數之 *paramid* 參數的值使用。</span><span class="sxs-lookup"><span data-stu-id="09189-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="09189-107">備份和還原參數</span><span class="sxs-lookup"><span data-stu-id="09189-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="09189-108">回呼參數</span><span class="sxs-lookup"><span data-stu-id="09189-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="09189-109">資料庫參數</span><span class="sxs-lookup"><span data-stu-id="09189-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="09189-110">資料庫快取參數</span><span class="sxs-lookup"><span data-stu-id="09189-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="09189-111">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="09189-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="09189-112">事件記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="09189-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="09189-113">I/o 參數</span><span class="sxs-lookup"><span data-stu-id="09189-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="09189-114">索引參數</span><span class="sxs-lookup"><span data-stu-id="09189-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="09189-115">資訊參數</span><span class="sxs-lookup"><span data-stu-id="09189-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="09189-116">中繼參數</span><span class="sxs-lookup"><span data-stu-id="09189-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="09189-117">資源參數</span><span class="sxs-lookup"><span data-stu-id="09189-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="09189-118">暫存資料庫參數</span><span class="sxs-lookup"><span data-stu-id="09189-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="09189-119">交易記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="09189-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="09189-120">系統參數描述格式</span><span class="sxs-lookup"><span data-stu-id="09189-120">System Parameter Description Format</span></span>

<span data-ttu-id="09189-121">系統會使用下列格式來描述每個系統參數：</span><span class="sxs-lookup"><span data-stu-id="09189-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="09189-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="09189-122">JET_paramX</span></span>

<span data-ttu-id="09189-123">JET_paramX 系統參數的描述。</span><span class="sxs-lookup"><span data-stu-id="09189-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09189-124">預設值：3</span><span class="sxs-lookup"><span data-stu-id="09189-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09189-125">參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="09189-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09189-126">輸入：</span><span class="sxs-lookup"><span data-stu-id="09189-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="09189-127">參數的資料類型。</span><span class="sxs-lookup"><span data-stu-id="09189-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09189-128">有效範圍：</span><span class="sxs-lookup"><span data-stu-id="09189-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09189-129">參數的合法值。</span><span class="sxs-lookup"><span data-stu-id="09189-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09189-130">範圍：</span><span class="sxs-lookup"><span data-stu-id="09189-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09189-131">參數是全域或每個實例？</span><span class="sxs-lookup"><span data-stu-id="09189-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09189-132">在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="09189-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09189-133">如果有任何實例存在，是否可以設定參數？</span><span class="sxs-lookup"><span data-stu-id="09189-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09189-134">在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</span><span class="sxs-lookup"><span data-stu-id="09189-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09189-135">是否可以在初始化時設定參數？</span><span class="sxs-lookup"><span data-stu-id="09189-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09189-136">會影響實體版面配置：</span><span class="sxs-lookup"><span data-stu-id="09189-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09189-137">參數是否會影響磁片上的檔案？</span><span class="sxs-lookup"><span data-stu-id="09189-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09189-138">會影響可靠性：</span><span class="sxs-lookup"><span data-stu-id="09189-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09189-139">參數是否會影響引擎可靠性？</span><span class="sxs-lookup"><span data-stu-id="09189-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09189-140">影響效能：</span><span class="sxs-lookup"><span data-stu-id="09189-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09189-141">參數是否會影響引擎效能？</span><span class="sxs-lookup"><span data-stu-id="09189-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09189-142">會影響資源：</span><span class="sxs-lookup"><span data-stu-id="09189-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09189-143">參數是否會影響引擎資源？</span><span class="sxs-lookup"><span data-stu-id="09189-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09189-144">可用性：</span><span class="sxs-lookup"><span data-stu-id="09189-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09189-145">支援參數的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="09189-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
