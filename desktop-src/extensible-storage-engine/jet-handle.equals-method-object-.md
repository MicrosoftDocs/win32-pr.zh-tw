---
description: 深入瞭解： JET_HANDLE。物件)  (Equals 方法
title: JET_HANDLE。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_handle.equals(v=EXCHG.10)
ms:contentKeyID: 39515621
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_HANDLE.Equals
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 31627cfc1e96f6a64779731d6bcaa2ab458f441d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695036"
---
# <a name="jet_handleequals-method-object"></a><span data-ttu-id="30558-103">JET_HANDLE。物件)  (Equals 方法</span><span class="sxs-lookup"><span data-stu-id="30558-103">JET_HANDLE.Equals method (Object)</span></span>

<span data-ttu-id="30558-104">傳回值，這個值表示這個實例是否等於另一個實例。</span><span class="sxs-lookup"><span data-stu-id="30558-104">Returns a value indicating whether this instance is equal to another instance.</span></span>

<span data-ttu-id="30558-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="30558-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="30558-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="30558-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="30558-107">語法</span><span class="sxs-lookup"><span data-stu-id="30558-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_HANDLE
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="30558-108">參數</span><span class="sxs-lookup"><span data-stu-id="30558-108">Parameters</span></span>

  - <span data-ttu-id="30558-109">obj</span><span class="sxs-lookup"><span data-stu-id="30558-109">obj</span></span>  
    <span data-ttu-id="30558-110">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="30558-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="30558-111">與這個執行個體相互比較的物件。</span><span class="sxs-lookup"><span data-stu-id="30558-111">An object to compare with this instance.</span></span>

#### <a name="return-value"></a><span data-ttu-id="30558-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="30558-112">Return value</span></span>

<span data-ttu-id="30558-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="30558-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="30558-114">如果兩個實例相等，則為 True。</span><span class="sxs-lookup"><span data-stu-id="30558-114">True if the two instances are equal.</span></span>  

## <a name="see-also"></a><span data-ttu-id="30558-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30558-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="30558-116">參考</span><span class="sxs-lookup"><span data-stu-id="30558-116">Reference</span></span>

[<span data-ttu-id="30558-117">JET_HANDLE 結構</span><span class="sxs-lookup"><span data-stu-id="30558-117">JET_HANDLE structure</span></span>](./jet-handle-structure.md)

[<span data-ttu-id="30558-118">JET_HANDLE 成員</span><span class="sxs-lookup"><span data-stu-id="30558-118">JET_HANDLE members</span></span>](./jet-handle-members.md)

[<span data-ttu-id="30558-119">等於多載</span><span class="sxs-lookup"><span data-stu-id="30558-119">Equals overload</span></span>](./jet-handle.equals-method.md)

[<span data-ttu-id="30558-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="30558-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
