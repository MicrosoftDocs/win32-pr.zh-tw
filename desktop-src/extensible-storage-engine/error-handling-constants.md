---
description: 深入瞭解：錯誤處理常數
title: 錯誤處理常數
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
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
ms.openlocfilehash: 1ab59a8e0c721558e5c056d25798c5d1273bd86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997979"
---
# <a name="error-handling-constants"></a><span data-ttu-id="e72ba-103">錯誤處理常數</span><span class="sxs-lookup"><span data-stu-id="e72ba-103">Error Handling Constants</span></span>


<span data-ttu-id="e72ba-104">_**適用于：** Windows |Windows Server_</span><span class="sxs-lookup"><span data-stu-id="e72ba-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="error-handling-constants"></a><span data-ttu-id="e72ba-105">錯誤處理常數</span><span class="sxs-lookup"><span data-stu-id="e72ba-105">Error Handling Constants</span></span>

<span data-ttu-id="e72ba-106">下列常數可用來設定 [JET_paramExceptionAction](./error-handling-parameters.md) 系統參數的範圍。</span><span class="sxs-lookup"><span data-stu-id="e72ba-106">The following constants are used to set the range for the [JET_paramExceptionAction](./error-handling-parameters.md) system parameters.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e72ba-107">常數/值</span><span class="sxs-lookup"><span data-stu-id="e72ba-107">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="e72ba-108">Description</span><span class="sxs-lookup"><span data-stu-id="e72ba-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e72ba-109">JET_ExceptionMsgBox</span><span class="sxs-lookup"><span data-stu-id="e72ba-109">JET_ExceptionMsgBox</span></span><br />
<span data-ttu-id="e72ba-110">0x0001</span><span class="sxs-lookup"><span data-stu-id="e72ba-110">0x0001</span></span></p></td>
<td><p><span data-ttu-id="e72ba-111">發生例外狀況時顯示訊息方塊。</span><span class="sxs-lookup"><span data-stu-id="e72ba-111">Displays a message box when an exception occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e72ba-112">JET_ExceptionNone</span><span class="sxs-lookup"><span data-stu-id="e72ba-112">JET_ExceptionNone</span></span><br />
<span data-ttu-id="e72ba-113">0x0002</span><span class="sxs-lookup"><span data-stu-id="e72ba-113">0x0002</span></span></p></td>
<td><p><span data-ttu-id="e72ba-114">發生例外狀況時，不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="e72ba-114">Does nothing when an exception occurs.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="e72ba-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e72ba-115">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e72ba-116"><strong>用戶端</strong></span><span class="sxs-lookup"><span data-stu-id="e72ba-116"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="e72ba-117">需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</span><span class="sxs-lookup"><span data-stu-id="e72ba-117">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e72ba-118"><strong>伺服器</strong></span><span class="sxs-lookup"><span data-stu-id="e72ba-118"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="e72ba-119">需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</span><span class="sxs-lookup"><span data-stu-id="e72ba-119">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e72ba-120"><strong>標頭</strong></span><span class="sxs-lookup"><span data-stu-id="e72ba-120"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="e72ba-121">宣告于 Esent. h 中。</span><span class="sxs-lookup"><span data-stu-id="e72ba-121">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="e72ba-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e72ba-122">See Also</span></span>

[<span data-ttu-id="e72ba-123">錯誤處理參數</span><span class="sxs-lookup"><span data-stu-id="e72ba-123">Error Handling Parameters</span></span>](./error-handling-parameters.md)
