---
description: 深入瞭解： JET_OPENTEMPORARYTABLE tableid 屬性
title: 'JET_OPENTEMPORARYTABLE. tableid 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'tableid property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.tableid
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.tableid(v=EXCHG.10)
ms:contentKeyID: 55104232
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.tableid
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.tableid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_tableid
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_tableid
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c4ea8f029265ff6725febe7817d6b8cc61807640
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193042"
---
# <a name="jet_opentemporarytabletableid-property"></a><span data-ttu-id="2678e-103">JET_OPENTEMPORARYTABLE tableid 屬性</span><span class="sxs-lookup"><span data-stu-id="2678e-103">JET_OPENTEMPORARYTABLE.tableid property</span></span>

<span data-ttu-id="2678e-104">取得在成功呼叫 JetOpenTemporaryTable 時所建立之臨時表的資料表控制碼。</span><span class="sxs-lookup"><span data-stu-id="2678e-104">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span>

<span data-ttu-id="2678e-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="2678e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="2678e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2678e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2678e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2678e-107">Syntax</span></span>

``` vb
'Declaration
Public Property tableid As JET_TABLEID
    Get
    Friend Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_TABLEID

value = instance.tableid
```

``` csharp
public JET_TABLEID tableid { get; internal set; }
```

#### <a name="property-value"></a><span data-ttu-id="2678e-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="2678e-108">Property value</span></span>

<span data-ttu-id="2678e-109">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2678e-109">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="2678e-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2678e-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2678e-111">參考</span><span class="sxs-lookup"><span data-stu-id="2678e-111">Reference</span></span>

[<span data-ttu-id="2678e-112">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="2678e-112">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="2678e-113">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="2678e-113">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="2678e-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="2678e-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
