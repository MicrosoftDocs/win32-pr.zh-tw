---
description: '深入瞭解： Update。 Save 方法 (Byte，Int32，Int32) '
title: 'Update。 Save 方法 (Byte，Int32，Int32) '
TOCTitle: Save method (Byte , Int32, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save(System.Byte[],System.Int32,System.Int32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55107759
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e2c798f22039ced1bab30ecaa9c3f650079be0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469164"
---
# <a name="updatesave-method-byte--int32-int32"></a><span data-ttu-id="a621a-103">Update。 Save 方法 (Byte，Int32，Int32) </span><span class="sxs-lookup"><span data-stu-id="a621a-103">Update.Save method (Byte , Int32, Int32)</span></span>

<span data-ttu-id="a621a-104">更新 tableid。</span><span class="sxs-lookup"><span data-stu-id="a621a-104">Update the tableid.</span></span>

<span data-ttu-id="a621a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a621a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a621a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a621a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a621a-107">語法</span><span class="sxs-lookup"><span data-stu-id="a621a-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save ( _
    bookmark As Byte(), _
    bookmarkSize As Integer, _
    <OutAttribute> ByRef actualBookmarkSize As Integer _
)
'Usage
Dim instance As Update
Dim bookmark As Byte()
Dim bookmarkSize As Integer
Dim actualBookmarkSize As Integer

instance.Save(bookmark, bookmarkSize, _
    actualBookmarkSize)
```

``` csharp
public void Save(
    byte[] bookmark,
    int bookmarkSize,
    out int actualBookmarkSize
)
```

#### <a name="parameters"></a><span data-ttu-id="a621a-108">參數</span><span class="sxs-lookup"><span data-stu-id="a621a-108">Parameters</span></span>

  - <span data-ttu-id="a621a-109">書籤 (bookmark)</span><span class="sxs-lookup"><span data-stu-id="a621a-109">bookmark</span></span>  
    <span data-ttu-id="a621a-110">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="a621a-110">Type: \[\]</span></span>  
    
    <span data-ttu-id="a621a-111">傳回已更新之記錄的書簽。</span><span class="sxs-lookup"><span data-stu-id="a621a-111">Returns the bookmark of the updated record.</span></span> <span data-ttu-id="a621a-112">這個可以是 null。</span><span class="sxs-lookup"><span data-stu-id="a621a-112">This can be null.</span></span>

<!-- end list -->

  - <span data-ttu-id="a621a-113">bookmarkSize</span><span class="sxs-lookup"><span data-stu-id="a621a-113">bookmarkSize</span></span>  
    <span data-ttu-id="a621a-114">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a621a-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a621a-115">書簽緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="a621a-115">The size of the bookmark buffer.</span></span>

<!-- end list -->

  - <span data-ttu-id="a621a-116">actualBookmarkSize</span><span class="sxs-lookup"><span data-stu-id="a621a-116">actualBookmarkSize</span></span>  
    <span data-ttu-id="a621a-117">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="a621a-117">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="a621a-118">傳回書簽的實際大小。</span><span class="sxs-lookup"><span data-stu-id="a621a-118">Returns the actual size of the bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="a621a-119">備註</span><span class="sxs-lookup"><span data-stu-id="a621a-119">Remarks</span></span>

<span data-ttu-id="a621a-120">[儲存] 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="a621a-120">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="a621a-121">更新的開始方式是呼叫建立更新物件，然後呼叫 JetSetColumn 或 JetSetColumns 一或多次來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="a621a-121">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="a621a-122">最後，會呼叫 Update 來完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="a621a-122">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="a621a-123">索引只有在 Update 或 JetSetColumn 或 JetSetColumns 期間才會更新。</span><span class="sxs-lookup"><span data-stu-id="a621a-123">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="a621a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a621a-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a621a-125">參考</span><span class="sxs-lookup"><span data-stu-id="a621a-125">Reference</span></span>

[<span data-ttu-id="a621a-126">Update 類別</span><span class="sxs-lookup"><span data-stu-id="a621a-126">Update class</span></span>](./update-class.md)

[<span data-ttu-id="a621a-127">更新成員</span><span class="sxs-lookup"><span data-stu-id="a621a-127">Update members</span></span>](./update-members.md)

[<span data-ttu-id="a621a-128">儲存多載</span><span class="sxs-lookup"><span data-stu-id="a621a-128">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="a621a-129">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a621a-129">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
