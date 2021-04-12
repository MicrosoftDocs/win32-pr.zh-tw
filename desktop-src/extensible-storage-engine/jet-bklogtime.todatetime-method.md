---
description: 深入瞭解： JET_BKLOGTIME。ToDateTime 方法
title: JET_BKLOGTIME。ToDateTime 方法
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39515201
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b6470e8486f5ff8c8ec8d1b7eb6678741fccc04f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318660"
---
# <a name="jet_bklogtimetodatetime-method"></a><span data-ttu-id="bbb4f-103">JET_BKLOGTIME。ToDateTime 方法</span><span class="sxs-lookup"><span data-stu-id="bbb4f-103">JET_BKLOGTIME.ToDateTime method</span></span>

<span data-ttu-id="bbb4f-104">產生此 JET_BKLOGTIME 的日期時程表示。</span><span class="sxs-lookup"><span data-stu-id="bbb4f-104">Generate a DateTime representation of this JET_BKLOGTIME.</span></span>

<span data-ttu-id="bbb4f-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bbb4f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bbb4f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="bbb4f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bbb4f-107">語法</span><span class="sxs-lookup"><span data-stu-id="bbb4f-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_BKLOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a><span data-ttu-id="bbb4f-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bbb4f-108">Return value</span></span>

<span data-ttu-id="bbb4f-109">類型： [可為 null](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="bbb4f-109">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="bbb4f-110">代表 JET_BKLOGTIME 的日期時間。</span><span class="sxs-lookup"><span data-stu-id="bbb4f-110">A DateTime representing the JET_BKLOGTIME.</span></span> <span data-ttu-id="bbb4f-111">如果 JET_BKLOGTIME 為 null，則會傳回 null。</span><span class="sxs-lookup"><span data-stu-id="bbb4f-111">If the JET_BKLOGTIME is null then null is returned.</span></span>  

#### <a name="implements"></a><span data-ttu-id="bbb4f-112">實作</span><span class="sxs-lookup"><span data-stu-id="bbb4f-112">Implements</span></span>

[<span data-ttu-id="bbb4f-113">IJET_LOGTIME。ToDateTime () </span><span class="sxs-lookup"><span data-stu-id="bbb4f-113">IJET_LOGTIME.ToDateTime()</span></span>](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a><span data-ttu-id="bbb4f-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbb4f-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bbb4f-115">參考</span><span class="sxs-lookup"><span data-stu-id="bbb4f-115">Reference</span></span>

[<span data-ttu-id="bbb4f-116">JET_BKLOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="bbb4f-116">JET_BKLOGTIME structure</span></span>](./jet-bklogtime-structure2.md)

[<span data-ttu-id="bbb4f-117">JET_BKLOGTIME 成員</span><span class="sxs-lookup"><span data-stu-id="bbb4f-117">JET_BKLOGTIME members</span></span>](./jet-bklogtime-members.md)

[<span data-ttu-id="bbb4f-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="bbb4f-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
