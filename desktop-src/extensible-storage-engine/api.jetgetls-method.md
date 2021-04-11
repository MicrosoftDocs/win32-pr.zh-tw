---
description: 深入瞭解： JetGetLS 方法
title: JetGetLS 方法
TOCTitle: 'JetGetLS method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetLS(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_LS@,Microsoft.Isam.Esent.Interop.LsGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetls(v=EXCHG.10)
ms:contentKeyID: 55100734
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetLS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 611f92e21dad83121b4e4a6226838ac9ebce2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191241"
---
# <a name="apijetgetls-method"></a><span data-ttu-id="c3470-103">JetGetLS 方法</span><span class="sxs-lookup"><span data-stu-id="c3470-103">Api.JetGetLS method</span></span>

<span data-ttu-id="c3470-104">讓應用程式取出與資料指標相關聯的內容控制碼，或與該資料指標相關聯的資料表。</span><span class="sxs-lookup"><span data-stu-id="c3470-104">Enables the application to retrieve the context handle known as Local Storage that is associated with a cursor or the table associated with that cursor.</span></span> <span data-ttu-id="c3470-105">先前必須使用 [JetSetLS (JET_SESID、JET_TABLEID、JET_LS、LsGrbit) ](./api.jetsetls-method.md)設定此內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="c3470-105">This context handle must have been previously set using [JetSetLS(JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).</span></span> <span data-ttu-id="c3470-106">JetGetLS 也可以用來同時提取資料指標或資料表的目前內容控制碼，並重設該內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="c3470-106">JetGetLS can also be used to simultaneously fetch the current context handle for a cursor or table and reset that context handle.</span></span>

<span data-ttu-id="c3470-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="c3470-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="c3470-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c3470-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c3470-109">語法</span><span class="sxs-lookup"><span data-stu-id="c3470-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetLS ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef ls As JET_LS, _
    grbit As LsGrbit _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim ls As JET_LS
Dim grbit As LsGrbitApi.JetGetLS(sesid, tableid, ls, _
    grbit)
```

``` csharp
public static void JetGetLS(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out JET_LS ls,
    LsGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="c3470-110">參數</span><span class="sxs-lookup"><span data-stu-id="c3470-110">Parameters</span></span>

  - <span data-ttu-id="c3470-111">sesid</span><span class="sxs-lookup"><span data-stu-id="c3470-111">sesid</span></span>  
    <span data-ttu-id="c3470-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3470-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="c3470-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="c3470-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3470-114">tableid</span><span class="sxs-lookup"><span data-stu-id="c3470-114">tableid</span></span>  
    <span data-ttu-id="c3470-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3470-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="c3470-116">要使用的資料指標。</span><span class="sxs-lookup"><span data-stu-id="c3470-116">The cursor to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3470-117">ls</span><span class="sxs-lookup"><span data-stu-id="c3470-117">ls</span></span>  
    <span data-ttu-id="c3470-118">類型： [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span><span class="sxs-lookup"><span data-stu-id="c3470-118">Type: [Microsoft.Isam.Esent.Interop.JET_LS](./jet-ls-structure.md)</span></span>  
    
    <span data-ttu-id="c3470-119">傳回取出的內容控制碼。</span><span class="sxs-lookup"><span data-stu-id="c3470-119">Returns the retrieved context handle.</span></span>

<!-- end list -->

  - <span data-ttu-id="c3470-120">grbit</span><span class="sxs-lookup"><span data-stu-id="c3470-120">grbit</span></span>  
    <span data-ttu-id="c3470-121">型別： [LsGrbit](./lsgrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="c3470-121">Type: [Microsoft.Isam.Esent.Interop.LsGrbit](./lsgrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="c3470-122">取出選項。</span><span class="sxs-lookup"><span data-stu-id="c3470-122">Retrieve options.</span></span>

## <a name="see-also"></a><span data-ttu-id="c3470-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c3470-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c3470-124">參考</span><span class="sxs-lookup"><span data-stu-id="c3470-124">Reference</span></span>

[<span data-ttu-id="c3470-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="c3470-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="c3470-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="c3470-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="c3470-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="c3470-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
