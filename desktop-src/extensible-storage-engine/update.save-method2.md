---
description: 深入瞭解： Update. Save 方法
title: 更新. 儲存方法
TOCTitle: 'Save method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.Save
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.save(v=EXCHG.10)
ms:contentKeyID: 55104195
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Update.Save
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad933c9601dc1a20932550aef363e067458ff79e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/05/2021
ms.locfileid: "106983272"
---
# <a name="updatesave-method"></a><span data-ttu-id="5eb95-103">更新. 儲存方法</span><span class="sxs-lookup"><span data-stu-id="5eb95-103">Update.Save method</span></span>

<span data-ttu-id="5eb95-104">更新 tableid。</span><span class="sxs-lookup"><span data-stu-id="5eb95-104">Update the tableid.</span></span>

<span data-ttu-id="5eb95-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="5eb95-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="5eb95-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="5eb95-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="5eb95-107">語法</span><span class="sxs-lookup"><span data-stu-id="5eb95-107">Syntax</span></span>

``` vb
'Declaration
Public Sub Save
'Usage
Dim instance As Update

instance.Save()
```

``` csharp
public void Save()
```

## <a name="remarks"></a><span data-ttu-id="5eb95-108">備註</span><span class="sxs-lookup"><span data-stu-id="5eb95-108">Remarks</span></span>

<span data-ttu-id="5eb95-109">[儲存] 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="5eb95-109">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="5eb95-110">更新的開始方式是呼叫建立更新物件，然後呼叫 JetSetColumn 或 JetSetColumns 一或多次來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="5eb95-110">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="5eb95-111">最後，會呼叫 Update 來完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="5eb95-111">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="5eb95-112">索引只有在 Update 或 JetSetColumn 或 JetSetColumns 期間才會更新。</span><span class="sxs-lookup"><span data-stu-id="5eb95-112">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="5eb95-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5eb95-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="5eb95-114">參考</span><span class="sxs-lookup"><span data-stu-id="5eb95-114">Reference</span></span>

[<span data-ttu-id="5eb95-115">Update 類別</span><span class="sxs-lookup"><span data-stu-id="5eb95-115">Update class</span></span>](./update-class.md)

[<span data-ttu-id="5eb95-116">更新成員</span><span class="sxs-lookup"><span data-stu-id="5eb95-116">Update members</span></span>](./update-members.md)

[<span data-ttu-id="5eb95-117">儲存多載</span><span class="sxs-lookup"><span data-stu-id="5eb95-117">Save overload</span></span>](./update.save-method.md)

[<span data-ttu-id="5eb95-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="5eb95-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
