---
description: 深入瞭解： JET_DBINFOMISC。物件)  (Equals 方法
title: JET_DBINFOMISC。物件)  (Equals 方法
TOCTitle: Equals method (Object)
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals(System.Object)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.equals(v=EXCHG.10)
ms:contentKeyID: 39513216
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.Equals
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c07e722abf0c6a291d42bc094ba7a2a7c5238cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973455"
---
# <a name="jet_dbinfomiscequals-method-object"></a><span data-ttu-id="5d8f3-103">JET_DBINFOMISC。物件)  (Equals 方法</span><span class="sxs-lookup"><span data-stu-id="5d8f3-103">JET_DBINFOMISC.Equals method (Object)</span></span>

<span data-ttu-id="5d8f3-104">判斷指定的 [物件](/dotnet/api/system.object) 是否等於目前的 [物件](/dotnet/api/system.object)。</span><span class="sxs-lookup"><span data-stu-id="5d8f3-104">Determines whether the specified [Object](/dotnet/api/system.object) is equal to the current [Object](/dotnet/api/system.object).</span></span>

<span data-ttu-id="5d8f3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5d8f3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5d8f3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5d8f3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5d8f3-107">語法</span><span class="sxs-lookup"><span data-stu-id="5d8f3-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Function Equals ( _
    obj As Object _
) As Boolean
'Usage
Dim instance As JET_DBINFOMISC
Dim obj As Object
Dim returnValue As Boolean

returnValue = instance.Equals(obj)
```

``` csharp
public override bool Equals(
    Object obj
)
```

#### <a name="parameters"></a><span data-ttu-id="5d8f3-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d8f3-108">Parameters</span></span>

  - <span data-ttu-id="5d8f3-109">obj</span><span class="sxs-lookup"><span data-stu-id="5d8f3-109">obj</span></span>  
    <span data-ttu-id="5d8f3-110">類型： [system.object](/dotnet/api/system.object)</span><span class="sxs-lookup"><span data-stu-id="5d8f3-110">Type: [System.Object](/dotnet/api/system.object)</span></span>  
    
    <span data-ttu-id="5d8f3-111">要與目前[物件](/dotnet/api/system.object)比較的[物件](/dotnet/api/system.object)。</span><span class="sxs-lookup"><span data-stu-id="5d8f3-111">The [Object](/dotnet/api/system.object) to compare with the current [Object](/dotnet/api/system.object).</span></span>

#### <a name="return-value"></a><span data-ttu-id="5d8f3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d8f3-112">Return value</span></span>

<span data-ttu-id="5d8f3-113">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="5d8f3-113">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  
<span data-ttu-id="5d8f3-114">如果指定的 [物件](/dotnet/api/system.object) 等於目前的 [物件](/dotnet/api/system.object)，則為 True;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="5d8f3-114">True if the specified [Object](/dotnet/api/system.object) is equal to the current [Object](/dotnet/api/system.object); otherwise, false.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5d8f3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d8f3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5d8f3-116">參考</span><span class="sxs-lookup"><span data-stu-id="5d8f3-116">Reference</span></span>

[<span data-ttu-id="5d8f3-117">JET_DBINFOMISC 類別</span><span class="sxs-lookup"><span data-stu-id="5d8f3-117">JET_DBINFOMISC class</span></span>](./jet-dbinfomisc-class.md)

[<span data-ttu-id="5d8f3-118">JET_DBINFOMISC 成員</span><span class="sxs-lookup"><span data-stu-id="5d8f3-118">JET_DBINFOMISC members</span></span>](./jet-dbinfomisc-members.md)

[<span data-ttu-id="5d8f3-119">等於多載</span><span class="sxs-lookup"><span data-stu-id="5d8f3-119">Equals overload</span></span>](./jet-dbinfomisc.equals-method.md)

[<span data-ttu-id="5d8f3-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5d8f3-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
