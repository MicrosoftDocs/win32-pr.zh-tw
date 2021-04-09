---
description: '深入瞭解： EsentApiException (字串的函式、JET_err) '
title: EsentApiException (字串 JET_err) 的函式
TOCTitle: EsentApiException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentApiException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentapiexception.esentapiexception(v=EXCHG.10)
ms:contentKeyID: 55101058
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentApiException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 568cf61a1c5852b70d0e08647a39ab70140d2215
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689396"
---
# <a name="esentapiexception-constructor-string-jet_err"></a><span data-ttu-id="2cf6a-103">EsentApiException (字串 JET_err) 的函式</span><span class="sxs-lookup"><span data-stu-id="2cf6a-103">EsentApiException constructor (String, JET_err)</span></span>

<span data-ttu-id="2cf6a-104">初始化 EsentApiException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="2cf6a-104">Initializes a new instance of the EsentApiException class.</span></span>

<span data-ttu-id="2cf6a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2cf6a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2cf6a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2cf6a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf6a-107">語法</span><span class="sxs-lookup"><span data-stu-id="2cf6a-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentApiException(description, _
    err)
```

``` csharp
protected EsentApiException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="2cf6a-108">參數</span><span class="sxs-lookup"><span data-stu-id="2cf6a-108">Parameters</span></span>

  - <span data-ttu-id="2cf6a-109">description</span><span class="sxs-lookup"><span data-stu-id="2cf6a-109">description</span></span>  
    <span data-ttu-id="2cf6a-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="2cf6a-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="2cf6a-111">錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="2cf6a-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="2cf6a-112">err</span><span class="sxs-lookup"><span data-stu-id="2cf6a-112">err</span></span>  
    <span data-ttu-id="2cf6a-113">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="2cf6a-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="2cf6a-114">例外狀況的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="2cf6a-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cf6a-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2cf6a-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2cf6a-116">參考</span><span class="sxs-lookup"><span data-stu-id="2cf6a-116">Reference</span></span>

[<span data-ttu-id="2cf6a-117">EsentApiException 類別</span><span class="sxs-lookup"><span data-stu-id="2cf6a-117">EsentApiException class</span></span>](./esentapiexception-class.md)

[<span data-ttu-id="2cf6a-118">EsentApiException 成員</span><span class="sxs-lookup"><span data-stu-id="2cf6a-118">EsentApiException members</span></span>](./esentapiexception-members.md)

[<span data-ttu-id="2cf6a-119">EsentApiException 多載</span><span class="sxs-lookup"><span data-stu-id="2cf6a-119">EsentApiException overload</span></span>](./esentapiexception-constructor.md)

[<span data-ttu-id="2cf6a-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2cf6a-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
