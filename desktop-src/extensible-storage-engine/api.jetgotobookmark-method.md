---
description: 深入瞭解： JetGotoBookmark 方法
title: JetGotoBookmark 方法
TOCTitle: 'JetGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55100753
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGotoBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 362a174e3da4dad864fd504e1678b4a3a1477e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104514129"
---
# <a name="apijetgotobookmark-method"></a><span data-ttu-id="df684-103">JetGotoBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="df684-103">Api.JetGotoBookmark method</span></span>

<span data-ttu-id="df684-104">將游標放置在與指定書簽相關聯之記錄的索引項目目。</span><span class="sxs-lookup"><span data-stu-id="df684-104">Positions a cursor to an index entry for the record that is associated with the specified bookmark.</span></span> <span data-ttu-id="df684-105">書簽可以搭配資料表上定義的任何索引使用。</span><span class="sxs-lookup"><span data-stu-id="df684-105">The bookmark can be used with any index defined over a table.</span></span> <span data-ttu-id="df684-106">您可以使用[JetGetBookmark (JET_SESID、JET_TABLEID、 \[ \] 、int32、int32) ](./api.jetgetbookmark-method.md)來取出記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="df684-106">The bookmark for a record can be retrieved using [JetGetBookmark(JET_SESID, JET_TABLEID, \[\], Int32, Int32)](./api.jetgetbookmark-method.md).</span></span>

<span data-ttu-id="df684-107">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="df684-107">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="df684-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="df684-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="df684-109">語法</span><span class="sxs-lookup"><span data-stu-id="df684-109">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGotoBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As IntegerApi.JetGotoBookmark(sesid, tableid, _
    bookmark, bookmarkSize)
```

``` csharp
public static void JetGotoBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="df684-110">參數</span><span class="sxs-lookup"><span data-stu-id="df684-110">Parameters</span></span>

  - <span data-ttu-id="df684-111">sesid</span><span class="sxs-lookup"><span data-stu-id="df684-111">sesid</span></span>  
    <span data-ttu-id="df684-112">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="df684-112">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="df684-113">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="df684-113">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="df684-114">tableid</span><span class="sxs-lookup"><span data-stu-id="df684-114">tableid</span></span>  
    <span data-ttu-id="df684-115">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="df684-115">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="df684-116">要放置的游標。</span><span class="sxs-lookup"><span data-stu-id="df684-116">The cursor to position.</span></span>

<!-- end list -->

  - <span data-ttu-id="df684-117">書籤 (bookmark)</span><span class="sxs-lookup"><span data-stu-id="df684-117">bookmark</span></span>  
    <span data-ttu-id="df684-118">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="df684-118">Type: \[\]</span></span>  
    
    <span data-ttu-id="df684-119">用來定位游標的書簽。</span><span class="sxs-lookup"><span data-stu-id="df684-119">The bookmark used to position the cursor.</span></span>

<!-- end list -->

  - <span data-ttu-id="df684-120">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="df684-120">bookmarkSize</span></span>  
    <span data-ttu-id="df684-121">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="df684-121">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="df684-122">書簽的大小。</span><span class="sxs-lookup"><span data-stu-id="df684-122">The size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="df684-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="df684-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="df684-124">參考</span><span class="sxs-lookup"><span data-stu-id="df684-124">Reference</span></span>

[<span data-ttu-id="df684-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="df684-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="df684-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="df684-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="df684-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="df684-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
