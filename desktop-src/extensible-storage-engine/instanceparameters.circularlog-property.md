---
description: 深入瞭解： InstanceParameters. CircularLog 屬性
title: InstanceParameters. CircularLog 屬性
TOCTitle: 'CircularLog property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.circularlog(v=EXCHG.10)
ms:contentKeyID: 55103320
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.CircularLog
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CircularLog
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9f9a77aa0d0f60b49269dc939787b165a3f2f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975559"
---
# <a name="instanceparameterscircularlog-property"></a><span data-ttu-id="96827-103">InstanceParameters. CircularLog 屬性</span><span class="sxs-lookup"><span data-stu-id="96827-103">InstanceParameters.CircularLog property</span></span>

<span data-ttu-id="96827-104">取得或設定值，指出是否開啟迴圈記錄。</span><span class="sxs-lookup"><span data-stu-id="96827-104">Gets or sets a value indicating whether circular logging is on.</span></span> <span data-ttu-id="96827-105">當迴圈記錄關閉時，所產生的所有交易記錄檔都會保留在磁片上，直到不再需要該檔案，因為已執行資料庫的完整備份。</span><span class="sxs-lookup"><span data-stu-id="96827-105">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="96827-106">當迴圈記錄開啟時，只有小於目前檢查點的交易記錄檔會保留在磁片上。</span><span class="sxs-lookup"><span data-stu-id="96827-106">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="96827-107">這種模式的好處是，備份不需要淘汰舊的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="96827-107">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span>

<span data-ttu-id="96827-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="96827-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="96827-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="96827-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="96827-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="96827-110">Syntax</span></span>

``` vb
'Declaration
Public Property CircularLog As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CircularLog

instance.CircularLog = value
```

``` csharp
public bool CircularLog { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="96827-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="96827-111">Property value</span></span>

<span data-ttu-id="96827-112">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="96827-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="96827-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="96827-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="96827-114">參考</span><span class="sxs-lookup"><span data-stu-id="96827-114">Reference</span></span>

[<span data-ttu-id="96827-115">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="96827-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="96827-116">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="96827-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="96827-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="96827-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
