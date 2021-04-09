---
description: 深入瞭解： Windows8Api. JetSetSessionParameter 方法
title: 'Windows8Api. JetSetSessionParameter 方法 (Windows8 的) '
TOCTitle: 'JetSetSessionParameter method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.windows8api.jetsetsessionparameter(v=EXCHG.10)
ms:contentKeyID: 55104461
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Windows8.Windows8Api.JetSetSessionParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b73331c765e1f8026b39c28dde5268417601663c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848381"
---
# <a name="windows8apijetsetsessionparameter-method"></a><span data-ttu-id="6b90f-103">Windows8Api. JetSetSessionParameter 方法</span><span class="sxs-lookup"><span data-stu-id="6b90f-103">Windows8Api.JetSetSessionParameter method</span></span>

<span data-ttu-id="6b90f-104">在提供的會話狀態上設定參數，用於此會話的存留期，或在重設之前使用。</span><span class="sxs-lookup"><span data-stu-id="6b90f-104">Sets a parameter on the provided session state, used for the lifetime of this session or until reset.</span></span>

<span data-ttu-id="6b90f-105">**命名空間：**  [Microsoft Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6b90f-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)</span></span>  
<span data-ttu-id="6b90f-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6b90f-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6b90f-107">語法</span><span class="sxs-lookup"><span data-stu-id="6b90f-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetSetSessionParameter ( _
    sesid As JET_SESID, _
    sesparamid As JET_sesparam, _
    data As Byte(), _
    dataSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim sesparamid As JET_sesparam
Dim data As Byte()
Dim dataSize As IntegerWindows8Api.JetSetSessionParameter(sesid, _
    sesparamid, data, dataSize)
```

``` csharp
public static void JetSetSessionParameter(
    JET_SESID sesid,
    JET_sesparam sesparamid,
    byte[] data,
    int dataSize
)
```

#### <a name="parameters"></a><span data-ttu-id="6b90f-108">參數</span><span class="sxs-lookup"><span data-stu-id="6b90f-108">Parameters</span></span>

  - <span data-ttu-id="6b90f-109">sesid</span><span class="sxs-lookup"><span data-stu-id="6b90f-109">sesid</span></span>  
    <span data-ttu-id="6b90f-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="6b90f-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="6b90f-111">要在其上設定參數的會話。</span><span class="sxs-lookup"><span data-stu-id="6b90f-111">The session to set the parameter on.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b90f-112">sesparamid</span><span class="sxs-lookup"><span data-stu-id="6b90f-112">sesparamid</span></span>  
    <span data-ttu-id="6b90f-113">類型： [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6b90f-113">Type: [Microsoft.Isam.Esent.Interop.Windows8.JET_sesparam](./jet-sesparam-enumeration.md)</span></span>  
    
    <span data-ttu-id="6b90f-114">要設定之會話參數的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6b90f-114">The ID of the session parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b90f-115">data</span><span class="sxs-lookup"><span data-stu-id="6b90f-115">data</span></span>  
    <span data-ttu-id="6b90f-116">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="6b90f-116">Type: \[\]</span></span>  
    
    <span data-ttu-id="6b90f-117">要在此會話參數中設定的資料。</span><span class="sxs-lookup"><span data-stu-id="6b90f-117">Data to set in this session parameter.</span></span>

<!-- end list -->

  - <span data-ttu-id="6b90f-118">dataSize</span><span class="sxs-lookup"><span data-stu-id="6b90f-118">dataSize</span></span>  
    <span data-ttu-id="6b90f-119">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6b90f-119">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6b90f-120">所提供資料的大小。</span><span class="sxs-lookup"><span data-stu-id="6b90f-120">Size of the data provided.</span></span>

## <a name="see-also"></a><span data-ttu-id="6b90f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b90f-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6b90f-122">參考</span><span class="sxs-lookup"><span data-stu-id="6b90f-122">Reference</span></span>

[<span data-ttu-id="6b90f-123">Windows8Api 類別</span><span class="sxs-lookup"><span data-stu-id="6b90f-123">Windows8Api class</span></span>](./windows8api-class.md)

[<span data-ttu-id="6b90f-124">Windows8Api 成員</span><span class="sxs-lookup"><span data-stu-id="6b90f-124">Windows8Api members</span></span>](./windows8api-members.md)

[<span data-ttu-id="6b90f-125">Windows8 命名空間。</span><span class="sxs-lookup"><span data-stu-id="6b90f-125">Microsoft.Isam.Esent.Interop.Windows8 namespace</span></span>](./microsoft.isam.esent.interop.windows8-namespace.md)
