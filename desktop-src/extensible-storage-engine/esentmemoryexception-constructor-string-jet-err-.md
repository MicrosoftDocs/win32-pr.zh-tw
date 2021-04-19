---
description: '深入瞭解： EsentMemoryException (字串的函式、JET_err) '
title: EsentMemoryException (字串 JET_err) 的函式
TOCTitle: EsentMemoryException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentMemoryException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentmemoryexception.esentmemoryexception(v=EXCHG.10)
ms:contentKeyID: 55102199
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentMemoryException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 60cdb6fda03695a4afb41d82e83aaeeb9415f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983590"
---
# <a name="esentmemoryexception-constructor-string-jet_err"></a><span data-ttu-id="5b969-103">EsentMemoryException (字串 JET_err) 的函式</span><span class="sxs-lookup"><span data-stu-id="5b969-103">EsentMemoryException constructor (String, JET_err)</span></span>

<span data-ttu-id="5b969-104">初始化 EsentMemoryException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="5b969-104">Initializes a new instance of the EsentMemoryException class.</span></span>

<span data-ttu-id="5b969-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5b969-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5b969-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5b969-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5b969-107">語法</span><span class="sxs-lookup"><span data-stu-id="5b969-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentMemoryException(description, _
    err)
```

``` csharp
protected EsentMemoryException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="5b969-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b969-108">Parameters</span></span>

  - <span data-ttu-id="5b969-109">description</span><span class="sxs-lookup"><span data-stu-id="5b969-109">description</span></span>  
    <span data-ttu-id="5b969-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="5b969-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="5b969-111">錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="5b969-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="5b969-112">err</span><span class="sxs-lookup"><span data-stu-id="5b969-112">err</span></span>  
    <span data-ttu-id="5b969-113">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="5b969-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="5b969-114">例外狀況的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5b969-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="5b969-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b969-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5b969-116">參考</span><span class="sxs-lookup"><span data-stu-id="5b969-116">Reference</span></span>

[<span data-ttu-id="5b969-117">EsentMemoryException 類別</span><span class="sxs-lookup"><span data-stu-id="5b969-117">EsentMemoryException class</span></span>](./esentmemoryexception-class.md)

[<span data-ttu-id="5b969-118">EsentMemoryException 成員</span><span class="sxs-lookup"><span data-stu-id="5b969-118">EsentMemoryException members</span></span>](./esentmemoryexception-members.md)

[<span data-ttu-id="5b969-119">EsentMemoryException 多載</span><span class="sxs-lookup"><span data-stu-id="5b969-119">EsentMemoryException overload</span></span>](./esentmemoryexception-constructor.md)

[<span data-ttu-id="5b969-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5b969-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
