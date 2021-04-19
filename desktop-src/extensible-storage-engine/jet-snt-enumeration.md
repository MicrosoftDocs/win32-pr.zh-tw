---
description: 深入瞭解： JET_SNT 列舉
title: JET_SNT 列舉
TOCTitle: JET_SNT enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SNT
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_snt(v=EXCHG.10)
ms:contentKeyID: 39511261
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SNT
- Microsoft.Isam.Esent.Interop.JET_SNT.Complete
- Microsoft.Isam.Esent.Interop.JET_SNT.Begin
- Microsoft.Isam.Esent.Interop.JET_SNT.Progress
- Microsoft.Isam.Esent.Interop.JET_SNT.RecoveryStep
- Microsoft.Isam.Esent.Interop.JET_SNT.Fail
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f6cad661d8265c32d605bbef94d75714ccb1783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973606"
---
# <a name="jet_snt-enumeration"></a><span data-ttu-id="75070-103">JET_SNT 列舉</span><span class="sxs-lookup"><span data-stu-id="75070-103">JET_SNT enumeration</span></span>

<span data-ttu-id="75070-104">要報告的進度類型。</span><span class="sxs-lookup"><span data-stu-id="75070-104">Type of progress being reported.</span></span>

<span data-ttu-id="75070-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="75070-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="75070-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="75070-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="75070-107">語法</span><span class="sxs-lookup"><span data-stu-id="75070-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_SNT
'Usage
Dim instance As JET_SNT
```

``` csharp
public enum JET_SNT
```

## <a name="members"></a><span data-ttu-id="75070-108">成員</span><span class="sxs-lookup"><span data-stu-id="75070-108">Members</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="75070-109">成員名稱</span><span class="sxs-lookup"><span data-stu-id="75070-109">Member name</span></span></th>
<th><span data-ttu-id="75070-110">說明</span><span class="sxs-lookup"><span data-stu-id="75070-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75070-111">開始</span><span class="sxs-lookup"><span data-stu-id="75070-111">Begin</span></span></td>
<td><span data-ttu-id="75070-112">作業開始的回呼。</span><span class="sxs-lookup"><span data-stu-id="75070-112">Callback for the beginning of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75070-113">進度</span><span class="sxs-lookup"><span data-stu-id="75070-113">Progress</span></span></td>
<td><span data-ttu-id="75070-114">作業進度的回呼。</span><span class="sxs-lookup"><span data-stu-id="75070-114">Callback for operation progress.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75070-115">完成</span><span class="sxs-lookup"><span data-stu-id="75070-115">Complete</span></span></td>
<td><span data-ttu-id="75070-116">完成作業的回呼。</span><span class="sxs-lookup"><span data-stu-id="75070-116">Callback for the completion of an operation.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="75070-117">失敗</span><span class="sxs-lookup"><span data-stu-id="75070-117">Fail</span></span></td>
<td><span data-ttu-id="75070-118">作業期間發生失敗的回呼。</span><span class="sxs-lookup"><span data-stu-id="75070-118">Callback for failure during the operation.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="75070-119">RecoveryStep</span><span class="sxs-lookup"><span data-stu-id="75070-119">RecoveryStep</span></span></td>
<td><span data-ttu-id="75070-120">恢復控制的回呼。</span><span class="sxs-lookup"><span data-stu-id="75070-120">Callback for recovery control.</span></span>
<p><span data-ttu-id="75070-121">用於在早于 Windows 8 的 Windows 作業系統版本中進行內部處理。</span><span class="sxs-lookup"><span data-stu-id="75070-121">Used for internal processing in versions of the Windows operating system earlier than Windows 8.</span></span> <span data-ttu-id="75070-122">此值不適用於以 Windows 8 開頭的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="75070-122">This value is not applicable to versions of Windows starting with Windows 8.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="75070-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75070-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="75070-124">參考</span><span class="sxs-lookup"><span data-stu-id="75070-124">Reference</span></span>

[<span data-ttu-id="75070-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="75070-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
