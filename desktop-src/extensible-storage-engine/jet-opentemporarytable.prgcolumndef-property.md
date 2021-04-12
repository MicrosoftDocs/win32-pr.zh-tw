---
description: 深入瞭解： JET_OPENTEMPORARYTABLE prgcolumndef 屬性
title: 'JET_OPENTEMPORARYTABLE. prgcolumndef 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'prgcolumndef property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumndef
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.prgcolumndef(v=EXCHG.10)
ms:contentKeyID: 55104129
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumndef
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_prgcolumndef
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_prgcolumndef
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.prgcolumndef
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 871cf1ba669717b9e2917a3e9012c6c16df5f97c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193043"
---
# <a name="jet_opentemporarytableprgcolumndef-property"></a><span data-ttu-id="ecdc2-103">JET_OPENTEMPORARYTABLE prgcolumndef 屬性</span><span class="sxs-lookup"><span data-stu-id="ecdc2-103">JET_OPENTEMPORARYTABLE.prgcolumndef property</span></span>

<span data-ttu-id="ecdc2-104">取得或設定在臨時表中建立之資料行的資料行定義。</span><span class="sxs-lookup"><span data-stu-id="ecdc2-104">Gets or sets the column definitions for the columns created in the temporary table.</span></span>

<span data-ttu-id="ecdc2-105">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="ecdc2-105">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ecdc2-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ecdc2-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ecdc2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ecdc2-107">Syntax</span></span>

``` vb
'Declaration
Public Property prgcolumndef As JET_COLUMNDEF()
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_COLUMNDEF()

value = instance.prgcolumndef

instance.prgcolumndef = value
```

``` csharp
public JET_COLUMNDEF[] prgcolumndef { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ecdc2-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="ecdc2-108">Property value</span></span>

<span data-ttu-id="ecdc2-109">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="ecdc2-109">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="ecdc2-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ecdc2-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ecdc2-111">參考</span><span class="sxs-lookup"><span data-stu-id="ecdc2-111">Reference</span></span>

[<span data-ttu-id="ecdc2-112">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="ecdc2-112">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="ecdc2-113">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="ecdc2-113">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="ecdc2-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="ecdc2-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
