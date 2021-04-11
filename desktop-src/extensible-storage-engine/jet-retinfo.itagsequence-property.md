---
description: 深入瞭解： JET_RETINFO itagSequence 屬性
title: JET_RETINFO itagSequence 屬性
TOCTitle: 'itagSequence property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo.itagsequence(v=EXCHG.10)
ms:contentKeyID: 55103876
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_RETINFO.get_itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.itagSequence
- Microsoft.Isam.Esent.Interop.JET_RETINFO.set_itagSequence
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: df42b6a52b34ec265aceb5b069b06f39c0663b44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194880"
---
# <a name="jet_retinfoitagsequence-property"></a><span data-ttu-id="537bf-103">JET_RETINFO itagSequence 屬性</span><span class="sxs-lookup"><span data-stu-id="537bf-103">JET_RETINFO.itagSequence property</span></span>

<span data-ttu-id="537bf-104">取得或設定多重值資料行中值的序號。</span><span class="sxs-lookup"><span data-stu-id="537bf-104">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="537bf-105">值的陣列是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="537bf-105">The array of values is one-based.</span></span> <span data-ttu-id="537bf-106">第一個值是 sequence 1，不是0。</span><span class="sxs-lookup"><span data-stu-id="537bf-106">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="537bf-107">如果 [記錄] 資料行只有一個值，則應該以 itagSequence 的形式傳遞1。</span><span class="sxs-lookup"><span data-stu-id="537bf-107">If the record column has only one value then 1 should be passed as the itagSequence.</span></span>

<span data-ttu-id="537bf-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="537bf-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="537bf-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="537bf-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="537bf-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="537bf-110">Syntax</span></span>

``` vb
'Declaration
Public Property itagSequence As Integer
    Get
    Set
'Usage
Dim instance As JET_RETINFO
Dim value As Integer

value = instance.itagSequence

instance.itagSequence = value
```

``` csharp
public int itagSequence { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="537bf-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="537bf-111">Property value</span></span>

<span data-ttu-id="537bf-112">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="537bf-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="537bf-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="537bf-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="537bf-114">參考</span><span class="sxs-lookup"><span data-stu-id="537bf-114">Reference</span></span>

[<span data-ttu-id="537bf-115">JET_RETINFO 類別</span><span class="sxs-lookup"><span data-stu-id="537bf-115">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="537bf-116">JET_RETINFO 成員</span><span class="sxs-lookup"><span data-stu-id="537bf-116">JET_RETINFO members</span></span>](./jet-retinfo-members.md)

[<span data-ttu-id="537bf-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="537bf-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
