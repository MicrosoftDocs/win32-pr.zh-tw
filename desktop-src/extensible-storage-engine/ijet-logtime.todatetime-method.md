---
description: 深入瞭解： IJET_LOGTIME。ToDateTime 方法
title: IJET_LOGTIME。ToDateTime 方法
TOCTitle: 'ToDateTime method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.ijet_logtime.todatetime(v=EXCHG.10)
ms:contentKeyID: 39510507
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.IJET_LOGTIME.ToDateTime
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 78226731ef945025aef0609cfeb905fe9b42101d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981463"
---
# <a name="ijet_logtimetodatetime-method"></a><span data-ttu-id="fe65b-103">IJET_LOGTIME。ToDateTime 方法</span><span class="sxs-lookup"><span data-stu-id="fe65b-103">IJET_LOGTIME.ToDateTime method</span></span>

<span data-ttu-id="fe65b-104">產生此 IJET_LOGTIME 的日期時程表示。</span><span class="sxs-lookup"><span data-stu-id="fe65b-104">Generate a DateTime representation of this IJET_LOGTIME.</span></span>

<span data-ttu-id="fe65b-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fe65b-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fe65b-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fe65b-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fe65b-107">語法</span><span class="sxs-lookup"><span data-stu-id="fe65b-107">Syntax</span></span>

``` vb
'Declaration
Function ToDateTime As Nullable(Of DateTime)
'Usage
Dim instance As IJET_LOGTIME
Dim returnValue As Nullable(Of DateTime)

returnValue = instance.ToDateTime()
```

``` csharp
Nullable<DateTime> ToDateTime()
```

#### <a name="return-value"></a><span data-ttu-id="fe65b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="fe65b-108">Return value</span></span>

<span data-ttu-id="fe65b-109">類型： [可為 null](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span><span class="sxs-lookup"><span data-stu-id="fe65b-109">Type: [System.Nullable](/dotnet/api/system.nullable-1)\<[DateTime](/dotnet/api/system.datetime)\></span></span>  
<span data-ttu-id="fe65b-110">代表 IJET_LOGTIME 的日期時間。</span><span class="sxs-lookup"><span data-stu-id="fe65b-110">A DateTime representing the IJET_LOGTIME.</span></span> <span data-ttu-id="fe65b-111">如果 IJET_LOGTIME 為 null，則會傳回 null。</span><span class="sxs-lookup"><span data-stu-id="fe65b-111">If the IJET_LOGTIME is null then null is returned.</span></span>  

## <a name="see-also"></a><span data-ttu-id="fe65b-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe65b-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fe65b-113">參考</span><span class="sxs-lookup"><span data-stu-id="fe65b-113">Reference</span></span>

[<span data-ttu-id="fe65b-114">IJET_LOGTIME 介面</span><span class="sxs-lookup"><span data-stu-id="fe65b-114">IJET_LOGTIME interface</span></span>](./ijet-logtime-interface.md)

[<span data-ttu-id="fe65b-115">IJET_LOGTIME 成員</span><span class="sxs-lookup"><span data-stu-id="fe65b-115">IJET_LOGTIME members</span></span>](./ijet-logtime-members.md)

[<span data-ttu-id="fe65b-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fe65b-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
