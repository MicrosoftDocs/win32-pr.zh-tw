---
description: 深入瞭解：事件記錄常數
title: 事件記錄常數
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
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
ms.openlocfilehash: e7ada5c71b603bf530c62d9f3af238131e305e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106986988"
---
# <a name="event-logging-constants"></a><span data-ttu-id="27cb5-103">事件記錄常數</span><span class="sxs-lookup"><span data-stu-id="27cb5-103">Event Logging Constants</span></span>


<span data-ttu-id="27cb5-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="27cb5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="event-logging-constants"></a><span data-ttu-id="27cb5-105">事件記錄常數</span><span class="sxs-lookup"><span data-stu-id="27cb5-105">Event Logging Constants</span></span>

<span data-ttu-id="27cb5-106">下列常數指出 [JET_ParamEventLoggingLevel](./event-log-parameters.md) 系統參數之事件記錄檔訊息的詳細層級。</span><span class="sxs-lookup"><span data-stu-id="27cb5-106">The following constants indicate the detail level for event log messages for the [JET_ParamEventLoggingLevel](./event-log-parameters.md) system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27cb5-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="27cb5-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="27cb5-108">Description</span><span class="sxs-lookup"><span data-stu-id="27cb5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27cb5-109">JET_EventLoggingDisable</span><span class="sxs-lookup"><span data-stu-id="27cb5-109">JET_EventLoggingDisable</span></span><br />
<span data-ttu-id="27cb5-110">0</span><span class="sxs-lookup"><span data-stu-id="27cb5-110">0</span></span></p></td>
<td><p><span data-ttu-id="27cb5-111">停用事件記錄。</span><span class="sxs-lookup"><span data-stu-id="27cb5-111">Disables event logging.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27cb5-112">JET_EventLoggingLevelMax</span><span class="sxs-lookup"><span data-stu-id="27cb5-112">JET_EventLoggingLevelMax</span></span><br />
<span data-ttu-id="27cb5-113">100</span><span class="sxs-lookup"><span data-stu-id="27cb5-113">100</span></span></p></td>
<td><p><span data-ttu-id="27cb5-114">設定要用於事件記錄檔的最大層級（目前為100個字元）。</span><span class="sxs-lookup"><span data-stu-id="27cb5-114">Sets the maximum level to use for event logs, which is currently 100 characters.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="27cb5-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="27cb5-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27cb5-116"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="27cb5-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="27cb5-117">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="27cb5-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27cb5-118"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="27cb5-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="27cb5-119">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="27cb5-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27cb5-120"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="27cb5-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="27cb5-121">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="27cb5-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="27cb5-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27cb5-122">See Also</span></span>

[<span data-ttu-id="27cb5-123">事件記錄檔參數</span><span class="sxs-lookup"><span data-stu-id="27cb5-123">Event Log Parameters</span></span>](./event-log-parameters.md)
