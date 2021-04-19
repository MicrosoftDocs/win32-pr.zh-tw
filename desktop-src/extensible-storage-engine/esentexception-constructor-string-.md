---
description: 深入瞭解： EsentException (字串) 的函數
title: 'EsentException 函式 (字串)  (的函式) '
TOCTitle: EsentException constructor (String)
ms:assetid: M:Microsoft.Isam.Esent.EsentException.#ctor(System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.esentexception.esentexception(v=EXCHG.10)
ms:contentKeyID: 55100720
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.EsentException..ctor
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 22a93625b7becbe083a42fbd6fcc71ad801173ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980046"
---
# <a name="esentexception-constructor-string"></a><span data-ttu-id="8519e-103">EsentException (字串) 的函式</span><span class="sxs-lookup"><span data-stu-id="8519e-103">EsentException constructor (String)</span></span>

<span data-ttu-id="8519e-104">使用指定的錯誤訊息，初始化 EsentException 類別的新實例。</span><span class="sxs-lookup"><span data-stu-id="8519e-104">Initializes a new instance of the EsentException class with a specified error message.</span></span>

<span data-ttu-id="8519e-105">**命名空間：**  [Microsoft. Isam. Esent](./microsoft.isam.esent-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8519e-105">**Namespace:**  [Microsoft.Isam.Esent](./microsoft.isam.esent-namespace.md)</span></span>  
<span data-ttu-id="8519e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8519e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8519e-107">語法</span><span class="sxs-lookup"><span data-stu-id="8519e-107">Syntax</span></span>

``` vb
'Declaration
Protected Sub New ( _
    message As String _
)
'Usage
Dim message As String

Dim instance As New EsentException(message)
```

``` csharp
protected EsentException(
    string message
)
```

#### <a name="parameters"></a><span data-ttu-id="8519e-108">參數</span><span class="sxs-lookup"><span data-stu-id="8519e-108">Parameters</span></span>

  - <span data-ttu-id="8519e-109">message</span><span class="sxs-lookup"><span data-stu-id="8519e-109">message</span></span>  
    <span data-ttu-id="8519e-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8519e-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8519e-111">描述錯誤的訊息。</span><span class="sxs-lookup"><span data-stu-id="8519e-111">The message that describes the error.</span></span>

## <a name="see-also"></a><span data-ttu-id="8519e-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8519e-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8519e-113">參考</span><span class="sxs-lookup"><span data-stu-id="8519e-113">Reference</span></span>

[<span data-ttu-id="8519e-114">EsentException 類別</span><span class="sxs-lookup"><span data-stu-id="8519e-114">EsentException class</span></span>](./esentexception-class.md)

[<span data-ttu-id="8519e-115">EsentException 成員</span><span class="sxs-lookup"><span data-stu-id="8519e-115">EsentException members</span></span>](./esentexception-members.md)

[<span data-ttu-id="8519e-116">EsentException 多載</span><span class="sxs-lookup"><span data-stu-id="8519e-116">EsentException overload</span></span>](./esentexception-constructor.md)

[<span data-ttu-id="8519e-117">Microsoft Isam 命名空間</span><span class="sxs-lookup"><span data-stu-id="8519e-117">Microsoft.Isam.Esent namespace</span></span>](./microsoft.isam.esent-namespace.md)
