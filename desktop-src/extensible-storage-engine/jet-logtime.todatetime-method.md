---
description: 深入瞭解： JET_LOGTIME。ToDateTime 方法
title: JET_LOGTIME。ToDateTime 方法
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39512964
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LOGTIME.ToDateTime
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14d427d1c7e4a6f37c27677ed9617d92eb8ff644
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695671"
---
# <a name="jet_logtimetodatetime-method"></a><span data-ttu-id="7e90b-103">JET_LOGTIME。ToDateTime 方法</span><span class="sxs-lookup"><span data-stu-id="7e90b-103">JET_LOGTIME.ToDateTime method</span></span>

<span data-ttu-id="7e90b-104">產生此 JET_LOGTIME 的日期時程表示。</span><span class="sxs-lookup"><span data-stu-id="7e90b-104">Generate a DateTime representation of this JET_LOGTIME.</span></span>

<span data-ttu-id="7e90b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7e90b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7e90b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7e90b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7e90b-107">語法</span><span class="sxs-lookup"><span data-stu-id="7e90b-107">Syntax</span></span>

``` vb
'Declaration
Public Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As JET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
public Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a><span data-ttu-id="7e90b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e90b-108">Return value</span></span>

<span data-ttu-id="7e90b-109">類型： [可為 null](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="7e90b-109">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="7e90b-110">代表 JET_LOGTIME 的日期時間。</span><span class="sxs-lookup"><span data-stu-id="7e90b-110">A DateTime representing the JET_LOGTIME.</span></span> <span data-ttu-id="7e90b-111">如果 JET_LOGTIME 為 null，則會傳回 null。</span><span class="sxs-lookup"><span data-stu-id="7e90b-111">If the JET_LOGTIME is null then null is returned.</span></span>  

#### <a name="implements"></a><span data-ttu-id="7e90b-112">實作</span><span class="sxs-lookup"><span data-stu-id="7e90b-112">Implements</span></span>

[<span data-ttu-id="7e90b-113">IJET_LOGTIME。ToDateTime () </span><span class="sxs-lookup"><span data-stu-id="7e90b-113">IJET_LOGTIME.ToDateTime()</span></span>](./ijet-logtime.todatetime-method.md)  

## <a name="see-also"></a><span data-ttu-id="7e90b-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7e90b-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7e90b-115">參考</span><span class="sxs-lookup"><span data-stu-id="7e90b-115">Reference</span></span>

[<span data-ttu-id="7e90b-116">JET_LOGTIME 結構</span><span class="sxs-lookup"><span data-stu-id="7e90b-116">JET_LOGTIME structure</span></span>](./jet-logtime-structure2.md)

[<span data-ttu-id="7e90b-117">JET_LOGTIME 成員</span><span class="sxs-lookup"><span data-stu-id="7e90b-117">JET_LOGTIME members</span></span>](./jet-logtime-members.md)

[<span data-ttu-id="7e90b-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7e90b-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
