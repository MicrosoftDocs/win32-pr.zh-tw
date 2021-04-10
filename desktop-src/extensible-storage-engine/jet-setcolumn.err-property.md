---
description: 深入瞭解： JET_SETCOLUMN err 屬性
title: JET_SETCOLUMN err 屬性
TOCTitle: 'err property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setcolumn.err(v=EXCHG.10)
ms:contentKeyID: 55107684
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.err
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.get_err
- Microsoft.Isam.Esent.Interop.JET_SETCOLUMN.set_err
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: afb84b4b8cbeda5f5686e953dd6e7b51e9bacbc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943293"
---
# <a name="jet_setcolumnerr-property"></a><span data-ttu-id="8ffce-103">JET_SETCOLUMN err 屬性</span><span class="sxs-lookup"><span data-stu-id="8ffce-103">JET_SETCOLUMN.err property</span></span>

<span data-ttu-id="8ffce-104">取得從集合資料行運算傳回的錯誤碼或警告。</span><span class="sxs-lookup"><span data-stu-id="8ffce-104">Gets the error code or warning returned from the set column operation.</span></span>

<span data-ttu-id="8ffce-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8ffce-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8ffce-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8ffce-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8ffce-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ffce-107">Syntax</span></span>

``` vb
'Declaration
Public Property err As JET_wrn
    Get
    Friend Set
'Usage
Dim instance As JET_SETCOLUMN
Dim value As JET_wrn

value = instance.err
```

``` csharp
public JET_wrn err { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="8ffce-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="8ffce-108">Property value</span></span>

<span data-ttu-id="8ffce-109">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="8ffce-109">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="8ffce-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ffce-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8ffce-111">參考</span><span class="sxs-lookup"><span data-stu-id="8ffce-111">Reference</span></span>

[<span data-ttu-id="8ffce-112">JET_SETCOLUMN 類別</span><span class="sxs-lookup"><span data-stu-id="8ffce-112">JET_SETCOLUMN class</span></span>](./jet-setcolumn-class.md)

[<span data-ttu-id="8ffce-113">JET_SETCOLUMN 成員</span><span class="sxs-lookup"><span data-stu-id="8ffce-113">JET_SETCOLUMN members</span></span>](./jet-setcolumn-members.md)

[<span data-ttu-id="8ffce-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8ffce-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
