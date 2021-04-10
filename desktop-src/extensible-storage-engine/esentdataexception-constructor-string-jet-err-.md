---
description: '深入瞭解： EsentDataException (字串的函式、JET_err) '
title: EsentDataException (字串 JET_err) 的函式
TOCTitle: EsentDataException constructor (String, JET_err)
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentDataException.#ctor(System.String,Microsoft.Isam.Esent.Interop.JET_err)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentdataexception.esentdataexception(v=EXCHG.10)
ms:contentKeyID: 55101571
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.EsentDataException..ctor
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9e39638d6e5458c0dcc555f31bec12e752d84337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114804"
---
# <a name="esentdataexception-constructor-string-jet_err"></a><span data-ttu-id="d9df8-103">EsentDataException (字串 JET_err) 的函式</span><span class="sxs-lookup"><span data-stu-id="d9df8-103">EsentDataException constructor (String, JET_err)</span></span>

<span data-ttu-id="d9df8-104">初始化 EsentDataException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="d9df8-104">Initializes a new instance of the EsentDataException class.</span></span>

<span data-ttu-id="d9df8-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="d9df8-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="d9df8-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d9df8-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d9df8-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9df8-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    description As String, _
    err As JET_err _
)
'Usage
Dim description As String
Dim err As JET_err

Dim instance As New EsentDataException(description, _
    err)
```

``` csharp
protected EsentDataException(
    string description,
    JET_err err
)
```

#### <a name="parameters"></a><span data-ttu-id="d9df8-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9df8-108">Parameters</span></span>

  - <span data-ttu-id="d9df8-109">description</span><span class="sxs-lookup"><span data-stu-id="d9df8-109">description</span></span>  
    <span data-ttu-id="d9df8-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="d9df8-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="d9df8-111">錯誤的描述。</span><span class="sxs-lookup"><span data-stu-id="d9df8-111">The description of the error.</span></span>

<!-- end list -->

  - <span data-ttu-id="d9df8-112">err</span><span class="sxs-lookup"><span data-stu-id="d9df8-112">err</span></span>  
    <span data-ttu-id="d9df8-113">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="d9df8-113">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  
    
    <span data-ttu-id="d9df8-114">例外狀況的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d9df8-114">The error code of the exception.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9df8-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9df8-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d9df8-116">參考</span><span class="sxs-lookup"><span data-stu-id="d9df8-116">Reference</span></span>

[<span data-ttu-id="d9df8-117">EsentDataException 類別</span><span class="sxs-lookup"><span data-stu-id="d9df8-117">EsentDataException class</span></span>](./esentdataexception-class.md)

[<span data-ttu-id="d9df8-118">EsentDataException 成員</span><span class="sxs-lookup"><span data-stu-id="d9df8-118">EsentDataException members</span></span>](./esentdataexception-members.md)

[<span data-ttu-id="d9df8-119">EsentDataException 多載</span><span class="sxs-lookup"><span data-stu-id="d9df8-119">EsentDataException overload</span></span>](./esentdataexception-constructor.md)

[<span data-ttu-id="d9df8-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="d9df8-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
