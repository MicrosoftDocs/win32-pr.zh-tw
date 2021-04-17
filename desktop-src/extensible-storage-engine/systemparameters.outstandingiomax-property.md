---
description: 深入瞭解： SystemParameters. OutstandingIOMax 屬性
title: SystemParameters. OutstandingIOMax 屬性
TOCTitle: 'OutstandingIOMax property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.systemparameters.outstandingiomax(v=EXCHG.10)
ms:contentKeyID: 55104045
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.SystemParameters.get_OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.OutstandingIOMax
- Microsoft.Isam.Esent.Interop.SystemParameters.set_OutstandingIOMax
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7faf7af3aec16bc81fada5c8742b4c60595bedad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513517"
---
# <a name="systemparametersoutstandingiomax-property"></a><span data-ttu-id="1f78b-103">SystemParameters. OutstandingIOMax 屬性</span><span class="sxs-lookup"><span data-stu-id="1f78b-103">SystemParameters.OutstandingIOMax property</span></span>

<span data-ttu-id="1f78b-104">此參數控制一次可在主機作業系統中的每個磁片佇列的資料庫檔案 i/o 數目。</span><span class="sxs-lookup"><span data-stu-id="1f78b-104">This parameter controls how many database file I/Os can be queued per-disk in the host operating system at one time.</span></span> <span data-ttu-id="1f78b-105">較大的參數值可大幅協助大型資料庫應用程式的效能。</span><span class="sxs-lookup"><span data-stu-id="1f78b-105">A larger value for this parameter can significantly help the performance of a large database application.</span></span>

<span data-ttu-id="1f78b-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1f78b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1f78b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1f78b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1f78b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f78b-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Property OutstandingIOMax As Integer
    Get
    Set
'Usage
Dim value As Integer

value = SystemParameters.OutstandingIOMax

SystemParameters.OutstandingIOMax = value
```

``` csharp
public static int OutstandingIOMax { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="1f78b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1f78b-109">Property value</span></span>

<span data-ttu-id="1f78b-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="1f78b-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="1f78b-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1f78b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1f78b-112">參考</span><span class="sxs-lookup"><span data-stu-id="1f78b-112">Reference</span></span>

[<span data-ttu-id="1f78b-113">SystemParameters 類別</span><span class="sxs-lookup"><span data-stu-id="1f78b-113">SystemParameters class</span></span>](./systemparameters-class.md)

[<span data-ttu-id="1f78b-114">SystemParameters 成員</span><span class="sxs-lookup"><span data-stu-id="1f78b-114">SystemParameters members</span></span>](./systemparameters-members.md)

[<span data-ttu-id="1f78b-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1f78b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
