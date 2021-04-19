---
description: '深入瞭解： EsentIOException (字串的函式、JET_err) '
title: EsentIOException (字串 JET_err) 的函式
TOCTitle: EsentIOException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentIOException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentioexception.esentioexception(v=EXCHG.10)
ms:contentKeyID: 55102030
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentIOException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 087f22d7836ff41ac97b65c15be1b51dfac84a8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977337"
---
# <a name="esentioexception-constructor-string-jet_err"></a><span data-ttu-id="c1c0f-103">EsentIOException (字串 JET_err) 的函式</span><span class="sxs-lookup"><span data-stu-id="c1c0f-103">EsentIOException constructor (String, JET_err)</span></span>

<span data-ttu-id="c1c0f-104">初始化 EsentIOException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="c1c0f-104">Initializes a new instance of the EsentIOException class.</span></span>

<span data-ttu-id="c1c0f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c1c0f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c1c0f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c1c0f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c1c0f-107">語法</span><span class="sxs-lookup"><span data-stu-id="c1c0f-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentIOException(description, _
    err)
```

``` csharp
protected EsentIOException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="c1c0f-108">參數</span><span class="sxs-lookup"><span data-stu-id="c1c0f-108">Parameters</span></span>

  - <span data-ttu-id="c1c0f-109">description</span><span class="sxs-lookup"><span data-stu-id="c1c0f-109">description</span></span>  
    <span data-ttu-id="c1c0f-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="c1c0f-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="c1c0f-111">錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="c1c0f-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="c1c0f-112">err</span><span class="sxs-lookup"><span data-stu-id="c1c0f-112">err</span></span>  
    <span data-ttu-id="c1c0f-113">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="c1c0f-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="c1c0f-114">例外狀況的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="c1c0f-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="c1c0f-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c1c0f-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c1c0f-116">參考</span><span class="sxs-lookup"><span data-stu-id="c1c0f-116">Reference</span></span>

[<span data-ttu-id="c1c0f-117">EsentIOException 類別</span><span class="sxs-lookup"><span data-stu-id="c1c0f-117">EsentIOException class</span></span>](./esentioexception-class.md)

[<span data-ttu-id="c1c0f-118">EsentIOException 成員</span><span class="sxs-lookup"><span data-stu-id="c1c0f-118">EsentIOException members</span></span>](./esentioexception-members.md)

[<span data-ttu-id="c1c0f-119">EsentIOException 多載</span><span class="sxs-lookup"><span data-stu-id="c1c0f-119">EsentIOException overload</span></span>](./esentioexception-constructor.md)

[<span data-ttu-id="c1c0f-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c1c0f-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
