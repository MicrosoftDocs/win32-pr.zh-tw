---
description: '深入瞭解： EsentOperationException (字串的函式、JET_err) '
title: EsentOperationException (字串 JET_err) 的函式
TOCTitle: EsentOperationException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentOperationException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102376
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bb25ea404e4581b369f9d81e772ba4b2e95f7fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981167"
---
# <a name="esentoperationexception-constructor-string-jet_err"></a><span data-ttu-id="0d733-103">EsentOperationException (字串 JET_err) 的函式</span><span class="sxs-lookup"><span data-stu-id="0d733-103">EsentOperationException constructor (String, JET_err)</span></span>

<span data-ttu-id="0d733-104">初始化 EsentOperationException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="0d733-104">Initializes a new instance of the EsentOperationException class.</span></span>

<span data-ttu-id="0d733-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="0d733-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="0d733-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="0d733-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="0d733-107">語法</span><span class="sxs-lookup"><span data-stu-id="0d733-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentOperationException(description, _
    err)
```

``` csharp
protected EsentOperationException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="0d733-108">參數</span><span class="sxs-lookup"><span data-stu-id="0d733-108">Parameters</span></span>

  - <span data-ttu-id="0d733-109">description</span><span class="sxs-lookup"><span data-stu-id="0d733-109">description</span></span>  
    <span data-ttu-id="0d733-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="0d733-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="0d733-111">錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="0d733-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="0d733-112">err</span><span class="sxs-lookup"><span data-stu-id="0d733-112">err</span></span>  
    <span data-ttu-id="0d733-113">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="0d733-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="0d733-114">例外狀況的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0d733-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d733-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d733-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0d733-116">參考</span><span class="sxs-lookup"><span data-stu-id="0d733-116">Reference</span></span>

[<span data-ttu-id="0d733-117">EsentOperationException 類別</span><span class="sxs-lookup"><span data-stu-id="0d733-117">EsentOperationException class</span></span>](./esentoperationexception-class.md)

[<span data-ttu-id="0d733-118">EsentOperationException 成員</span><span class="sxs-lookup"><span data-stu-id="0d733-118">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="0d733-119">EsentOperationException 多載</span><span class="sxs-lookup"><span data-stu-id="0d733-119">EsentOperationException overload</span></span>](./esentoperationexception-constructor.md)

[<span data-ttu-id="0d733-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="0d733-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
