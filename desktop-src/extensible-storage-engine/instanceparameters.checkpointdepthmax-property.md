---
description: 深入瞭解： InstanceParameters. CheckpointDepthMax 屬性
title: InstanceParameters. CheckpointDepthMax 屬性
TOCTitle: 'CheckpointDepthMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.checkpointdepthmax(v=EXCHG.10)
ms:contentKeyID: 55103294
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CheckpointDepthMax
- Microsoft.Isam.Esent.Interop.InstanceParameters.CheckpointDepthMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3addab0356206577eda22119ddce81721e9c2bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993021"
---
# <a name="instanceparameterscheckpointdepthmax-property"></a><span data-ttu-id="59832-103">InstanceParameters. CheckpointDepthMax 屬性</span><span class="sxs-lookup"><span data-stu-id="59832-103">InstanceParameters.CheckpointDepthMax property</span></span>

<span data-ttu-id="59832-104">取得或設定在損毀之後，需要重新執行多少個交易記錄檔的閾值（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="59832-104">Gets or sets the threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span> <span data-ttu-id="59832-105">如果使用 CircularLog 來啟用迴圈記錄，此參數也會控制要保留在磁片上的大約交易記錄檔量。</span><span class="sxs-lookup"><span data-stu-id="59832-105">If circular logging is enabled using CircularLog then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="59832-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="59832-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="59832-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="59832-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="59832-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="59832-108">Syntax</span></span>

``` vb
'Declaration
Public Property CheckpointDepthMax As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CheckpointDepthMax

instance.CheckpointDepthMax = value
```

``` csharp
public int CheckpointDepthMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="59832-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="59832-109">Property value</span></span>

<span data-ttu-id="59832-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="59832-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="59832-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59832-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="59832-112">參考</span><span class="sxs-lookup"><span data-stu-id="59832-112">Reference</span></span>

[<span data-ttu-id="59832-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="59832-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="59832-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="59832-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="59832-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="59832-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
