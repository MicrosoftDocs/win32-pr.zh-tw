---
description: 深入瞭解： JetGetBookmark 方法
title: JetGetBookmark 方法
TOCTitle: 'JetGetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetbookmark(v=EXCHG.10)
ms:contentKeyID: 55100702
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0eaac3c0c92fa9d6cfa1a5bca660791b81efe5ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973236"
---
# <a name="apijetgetbookmark-method"></a><span data-ttu-id="59067-103">JetGetBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="59067-103">Api.JetGetBookmark method</span></span>

<span data-ttu-id="59067-104">抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="59067-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="59067-105">然後，您可以使用[JetGotoBookmark (JET_SESID、JET_TABLEID、 \[ \] Int32) ](./api.jetgotobookmark-method.md)，利用這個書簽將該資料指標重新置放回相同記錄。</span><span class="sxs-lookup"><span data-stu-id="59067-105">This bookmark can then be used to reposition that cursor back to the same record using [JetGotoBookmark(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetgotobookmark-method.md).</span></span> <span data-ttu-id="59067-106">書簽將不再超過 [BookmarkMost](./systemparameters.bookmarkmost-property.md) 個位元組。</span><span class="sxs-lookup"><span data-stu-id="59067-106">The bookmark will be no longer than [BookmarkMost](./systemparameters.bookmarkmost-property.md) bytes.</span></span> <span data-ttu-id="59067-107">另請參閱 [GetBookmark (JET_SESID JET_TABLEID) ](./api.getbookmark-method.md)。</span><span class="sxs-lookup"><span data-stu-id="59067-107">Also see [GetBookmark(JET_SESID, JET_TABLEID)](./api.getbookmark-method.md).</span></span>

<span data-ttu-id="59067-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="59067-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="59067-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="59067-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="59067-110">語法</span><span class="sxs-lookup"><span data-stu-id="59067-110">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As IntegerApi.JetGetBookmark(sesid, tableid, _
    bookmark, bookmarkSize, actualBookmarkSize)
```

``` csharp
public static void JetGetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid,
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="59067-111">參數</span><span class="sxs-lookup"><span data-stu-id="59067-111">Parameters</span></span>

  - <span data-ttu-id="59067-112">sesid</span><span class="sxs-lookup"><span data-stu-id="59067-112">sesid</span></span>  
    <span data-ttu-id="59067-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="59067-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="59067-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="59067-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="59067-115">tableid</span><span class="sxs-lookup"><span data-stu-id="59067-115">tableid</span></span>  
    <span data-ttu-id="59067-116">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="59067-116">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="59067-117">要從中取出書簽的資料指標。</span><span class="sxs-lookup"><span data-stu-id="59067-117">The cursor to retrieve the bookmark from.</span></span>

<!-- end list -->

  - <span data-ttu-id="59067-118">書籤 (bookmark)</span><span class="sxs-lookup"><span data-stu-id="59067-118">bookmark</span></span>  
    <span data-ttu-id="59067-119">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="59067-119">Type: \[\]</span></span>  
    
    <span data-ttu-id="59067-120">包含書簽的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="59067-120">Buffer to contain the bookmark.</span></span>

<!-- end list -->

  - <span data-ttu-id="59067-121">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="59067-121">bookmarkSize</span></span>  
    <span data-ttu-id="59067-122">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="59067-122">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="59067-123">書簽緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="59067-123">Size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="59067-124">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="59067-124">actualBookmarkSize</span></span>  
    <span data-ttu-id="59067-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="59067-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="59067-126">傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="59067-126">Returns the actual size of the bookmark.</span></span>

## <a name="see-also"></a><span data-ttu-id="59067-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59067-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="59067-128">參考</span><span class="sxs-lookup"><span data-stu-id="59067-128">Reference</span></span>

[<span data-ttu-id="59067-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="59067-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="59067-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="59067-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="59067-131">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="59067-131">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
