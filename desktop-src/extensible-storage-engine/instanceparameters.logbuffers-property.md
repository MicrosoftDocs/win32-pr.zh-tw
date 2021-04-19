---
description: 深入瞭解： InstanceParameters. LogBuffers 屬性
title: InstanceParameters. LogBuffers 屬性
TOCTitle: 'LogBuffers property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logbuffers(v=EXCHG.10)
ms:contentKeyID: 55107472
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogBuffers
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogBuffers
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f58e43ea38792549d384328dc0fd6c5d31616e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106994456"
---
# <a name="instanceparameterslogbuffers-property"></a><span data-ttu-id="fdbe1-103">InstanceParameters. LogBuffers 屬性</span><span class="sxs-lookup"><span data-stu-id="fdbe1-103">InstanceParameters.LogBuffers property</span></span>

<span data-ttu-id="fdbe1-104">取得或設定在將記錄寫入交易記錄檔之前，用來快取記錄檔記錄的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-104">Gets or sets the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="fdbe1-105">此參數的單位是保存交易記錄檔之磁片區的磁區大小。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-105">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="fdbe1-106">磁區大小幾乎一律為512個位元組，因此可以安全地假設該單位的大小。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-106">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span> <span data-ttu-id="fdbe1-107">此參數會對效能造成影響。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-107">This parameter has an impact on performance.</span></span> <span data-ttu-id="fdbe1-108">當資料庫引擎處於大量更新負載時，此緩衝區可能會非常快速地完成。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-108">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="fdbe1-109">交易記錄檔較大的快取大小，對於在這種高負載狀況下的良好更新效能來說非常重要。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-109">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="fdbe1-110">在此情況下，已知的預設值太小。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-110">The default is known to be too small for this case.</span></span> <span data-ttu-id="fdbe1-111">請勿將此參數設定為大於交易記錄檔大小一半的緩衝區數 (以位元組為單位) 。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-111">Do not set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<span data-ttu-id="fdbe1-112">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fdbe1-112">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fdbe1-113">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fdbe1-113">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbe1-114">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdbe1-114">Syntax</span></span>

``` vb
'Declaration
Public Property LogBuffers As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogBuffers

instance.LogBuffers = value
```

``` csharp
public int LogBuffers { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="fdbe1-115">屬性值</span><span class="sxs-lookup"><span data-stu-id="fdbe1-115">Property value</span></span>

<span data-ttu-id="fdbe1-116">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="fdbe1-116">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="fdbe1-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fdbe1-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fdbe1-118">參考</span><span class="sxs-lookup"><span data-stu-id="fdbe1-118">Reference</span></span>

[<span data-ttu-id="fdbe1-119">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="fdbe1-119">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="fdbe1-120">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="fdbe1-120">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="fdbe1-121">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fdbe1-121">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
