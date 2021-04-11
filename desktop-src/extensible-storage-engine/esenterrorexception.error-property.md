---
description: 深入瞭解： EsentErrorException。 Error 屬性
title: EsentErrorException。 Error 屬性
TOCTitle: 'Error property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.EsentErrorException.Error
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.error(v=EXCHG.10)
ms:contentKeyID: 55101646
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.get_Error
- Microsoft.Isam.Esent.Interop.EsentErrorException.Error
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e777886ed95ea72a02626f7eb91724123a495f24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195000"
---
# <a name="esenterrorexceptionerror-property"></a><span data-ttu-id="832e7-103">EsentErrorException。 Error 屬性</span><span class="sxs-lookup"><span data-stu-id="832e7-103">EsentErrorException.Error property</span></span>

<span data-ttu-id="832e7-104">取得這個例外狀況的基礎 Esent 錯誤。</span><span class="sxs-lookup"><span data-stu-id="832e7-104">Gets the underlying Esent error for this exception.</span></span>

<span data-ttu-id="832e7-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="832e7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="832e7-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="832e7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="832e7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="832e7-107">Syntax</span></span>

``` vb
'Declaration
Public ReadOnly Property Error As JET_err
    Get
'Usage
Dim instance As EsentErrorException
Dim value As JET_err

value = instance.Error
```

``` csharp
public JET_err Error { get; }
```

#### <a name="property-value"></a><span data-ttu-id="832e7-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="832e7-108">Property value</span></span>

<span data-ttu-id="832e7-109">類型： [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="832e7-109">Type: [Microsoft.Isam.Esent.Interop.JET_err](./jet-err-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="832e7-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="832e7-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="832e7-111">參考</span><span class="sxs-lookup"><span data-stu-id="832e7-111">Reference</span></span>

[<span data-ttu-id="832e7-112">EsentErrorException 類別</span><span class="sxs-lookup"><span data-stu-id="832e7-112">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="832e7-113">EsentErrorException 成員</span><span class="sxs-lookup"><span data-stu-id="832e7-113">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="832e7-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="832e7-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
