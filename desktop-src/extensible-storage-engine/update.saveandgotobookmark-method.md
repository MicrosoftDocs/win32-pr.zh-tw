---
description: 深入瞭解： SaveAndGotoBookmark 方法
title: SaveAndGotoBookmark 方法
TOCTitle: 'SaveAndGotoBookmark method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update.saveandgotobookmark(v=EXCHG.10)
ms:contentKeyID: 55104204
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Update.SaveAndGotoBookmark
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d682657b9821f782af339a3d0c3253b6fa771d37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991830"
---
# <a name="updatesaveandgotobookmark-method"></a><span data-ttu-id="ca475-103">SaveAndGotoBookmark 方法</span><span class="sxs-lookup"><span data-stu-id="ca475-103">Update.SaveAndGotoBookmark method</span></span>

<span data-ttu-id="ca475-104">更新 tableid，並將 tableid 放在修改過的記錄上。</span><span class="sxs-lookup"><span data-stu-id="ca475-104">Update the tableid and position the tableid on the record that was modified.</span></span> <span data-ttu-id="ca475-105">這在插入記錄時很有用，因為 tableid 預設會保留在舊的位置。</span><span class="sxs-lookup"><span data-stu-id="ca475-105">This can be useful when inserting a record because by default the tableid remains in its old location.</span></span>

<span data-ttu-id="ca475-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="ca475-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="ca475-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ca475-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca475-108">語法</span><span class="sxs-lookup"><span data-stu-id="ca475-108">Syntax</span></span>

``` vb
'Declaration
Public Sub SaveAndGotoBookmark
'Usage
Dim instance As Update

instance.SaveAndGotoBookmark()
```

``` csharp
public void SaveAndGotoBookmark()
```

## <a name="remarks"></a><span data-ttu-id="ca475-109">備註</span><span class="sxs-lookup"><span data-stu-id="ca475-109">Remarks</span></span>

<span data-ttu-id="ca475-110">[儲存] 是執行插入或更新的最後一個步驟。</span><span class="sxs-lookup"><span data-stu-id="ca475-110">Save is the final step in performing an insert or an update.</span></span> <span data-ttu-id="ca475-111">更新的開始方式是呼叫建立更新物件，然後呼叫 JetSetColumn 或 JetSetColumns 一或多次來設定記錄狀態。</span><span class="sxs-lookup"><span data-stu-id="ca475-111">The update is begun by calling creating an Update object and then by calling JetSetColumn or JetSetColumns one or more times to set the record state.</span></span> <span data-ttu-id="ca475-112">最後，會呼叫 Update 來完成更新作業。</span><span class="sxs-lookup"><span data-stu-id="ca475-112">Finally, Update is called to complete the update operation.</span></span> <span data-ttu-id="ca475-113">索引只有在 Update 或 JetSetColumn 或 JetSetColumns 期間才會更新。</span><span class="sxs-lookup"><span data-stu-id="ca475-113">Indexes are updated only by Update or and not during JetSetColumn or JetSetColumns.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca475-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca475-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ca475-115">參考</span><span class="sxs-lookup"><span data-stu-id="ca475-115">Reference</span></span>

[<span data-ttu-id="ca475-116">Update 類別</span><span class="sxs-lookup"><span data-stu-id="ca475-116">Update class</span></span>](./update-class.md)

[<span data-ttu-id="ca475-117">更新成員</span><span class="sxs-lookup"><span data-stu-id="ca475-117">Update members</span></span>](./update-members.md)

[<span data-ttu-id="ca475-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="ca475-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
