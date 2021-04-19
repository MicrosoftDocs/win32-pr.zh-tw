---
description: 深入瞭解： EsentException 類別
title: 'EsentException 類別 (Microsoft 的 Isam) '
TOCTitle: EsentException class
ms:assetid: T:Microsoft.Isam.Esent.EsentException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100645
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.EsentException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.EsentException
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 775d63c6b1d234696790b1187538a6d1ee734a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988437"
---
# <a name="esentexception-class"></a><span data-ttu-id="fa34f-103">EsentException 類別</span><span class="sxs-lookup"><span data-stu-id="fa34f-103">EsentException class</span></span>

<span data-ttu-id="fa34f-104">ESENT 例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="fa34f-104">Base class for ESENT exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="fa34f-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="fa34f-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="fa34f-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="fa34f-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="fa34f-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="fa34f-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    <span data-ttu-id="fa34f-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="fa34f-108">Microsoft.Isam.Esent.EsentException</span></span>  
      [<span data-ttu-id="fa34f-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="fa34f-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
      [<span data-ttu-id="fa34f-110">EsentInvalidColumnException （.）</span><span class="sxs-lookup"><span data-stu-id="fa34f-110">Microsoft.Isam.Esent.Interop.EsentInvalidColumnException</span></span>](./esentinvalidcolumnexception-class.md)  

<span data-ttu-id="fa34f-111">**命名空間：**  [Microsoft. Isam. Esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fa34f-111">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="fa34f-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fa34f-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fa34f-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa34f-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentException _
    Inherits Exception
'Usage
Dim instance As EsentException
```

``` csharp
[SerializableAttribute]
public abstract class EsentException : Exception
```

## <a name="thread-safety"></a><span data-ttu-id="fa34f-114">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="fa34f-114">Thread safety</span></span>

<span data-ttu-id="fa34f-115">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa34f-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="fa34f-116">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="fa34f-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa34f-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fa34f-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fa34f-118">參考</span><span class="sxs-lookup"><span data-stu-id="fa34f-118">Reference</span></span>

[<span data-ttu-id="fa34f-119">EsentException 成員</span><span class="sxs-lookup"><span data-stu-id="fa34f-119">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="fa34f-120">Microsoft Isam 命名空間</span><span class="sxs-lookup"><span data-stu-id="fa34f-120">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
