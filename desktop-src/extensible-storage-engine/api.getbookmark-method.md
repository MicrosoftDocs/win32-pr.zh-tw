---
description: 深入瞭解： GetBookmark 方法
title: GetBookmark 方法
TOCTitle: 'GetBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.GetBookmark(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.getbookmark(v=EXCHG.10)
ms:contentKeyID: 55100654
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.GetBookmark
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4edcdfe7ddefadd993ef9c96e6dcc1416080b413
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510860"
---
# <a name="apigetbookmark-method"></a><span data-ttu-id="ac966-103">GetBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="ac966-103">Api.GetBookmark method</span></span>

<span data-ttu-id="ac966-104">抓取與資料指標目前位置的索引項目目相關聯之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="ac966-104">Retrieves the bookmark for the record that is associated with the index entry at the current position of a cursor.</span></span> <span data-ttu-id="ac966-105">然後，您可以使用這個書簽，將該資料指標重新放置到使用 JetGotoBookmark 的相同記錄。</span><span class="sxs-lookup"><span data-stu-id="ac966-105">This bookmark can then be used to reposition that cursor back to the same record using JetGotoBookmark.</span></span>

<span data-ttu-id="ac966-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ac966-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ac966-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ac966-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ac966-108">語法</span><span class="sxs-lookup"><span data-stu-id="ac966-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Function GetBookmark ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID _
) As Byte()
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim returnValue As Byte()

returnValue = Api.GetBookmark(sesid, _
    tableid)
```

``` csharp
public static byte[] GetBookmark(
    JET_SESID sesid,
    JET_TABLEID tableid
)
```

#### <a name="parameters"></a><span data-ttu-id="ac966-109">參數</span><span class="sxs-lookup"><span data-stu-id="ac966-109">Parameters</span></span>

  - <span data-ttu-id="ac966-110">sesid</span><span class="sxs-lookup"><span data-stu-id="ac966-110">sesid</span></span>  
    <span data-ttu-id="ac966-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ac966-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="ac966-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="ac966-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="ac966-113">tableid</span><span class="sxs-lookup"><span data-stu-id="ac966-113">tableid</span></span>  
    <span data-ttu-id="ac966-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="ac966-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="ac966-115">要從中取出書簽的資料指標。</span><span class="sxs-lookup"><span data-stu-id="ac966-115">The cursor to retrieve the bookmark from.</span></span>

#### <a name="return-value"></a><span data-ttu-id="ac966-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac966-116">Return value</span></span>

<span data-ttu-id="ac966-117">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="ac966-117">Type: \[\]</span></span>  
<span data-ttu-id="ac966-118">記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="ac966-118">The bookmark of the record.</span></span>  

## <a name="see-also"></a><span data-ttu-id="ac966-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac966-119">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ac966-120">參考</span><span class="sxs-lookup"><span data-stu-id="ac966-120">Reference</span></span>

[<span data-ttu-id="ac966-121">Api 類別</span><span class="sxs-lookup"><span data-stu-id="ac966-121">Api class</span></span>](./api-class.md)

[<span data-ttu-id="ac966-122">Api 成員</span><span class="sxs-lookup"><span data-stu-id="ac966-122">Api members</span></span>](./api-members.md)

[<span data-ttu-id="ac966-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ac966-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
