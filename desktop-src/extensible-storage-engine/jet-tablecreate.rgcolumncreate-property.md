---
description: 深入瞭解： JET_TABLECREATE rgcolumncreate 屬性
title: JET_TABLECREATE rgcolumncreate 屬性
TOCTitle: 'rgcolumncreate property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgcolumncreate
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate.rgcolumncreate(v=EXCHG.10)
ms:contentKeyID: 55103965
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgcolumncreate
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.get_rgcolumncreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.rgcolumncreate
- Microsoft.Isam.Esent.Interop.JET_TABLECREATE.set_rgcolumncreate
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97392c9dd89502dc713f4fa7dd2c79de90360930
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847700"
---
# <a name="jet_tablecreatergcolumncreate-property"></a><span data-ttu-id="b476a-103">JET_TABLECREATE rgcolumncreate 屬性</span><span class="sxs-lookup"><span data-stu-id="b476a-103">JET_TABLECREATE.rgcolumncreate property</span></span>

<span data-ttu-id="b476a-104">取得或設定資料行建立資訊的陣列，其類型為 [JET_COLUMNCREATE](./jet-columncreate-class.md)。</span><span class="sxs-lookup"><span data-stu-id="b476a-104">Gets or sets an array of column creation info, of type [JET_COLUMNCREATE](./jet-columncreate-class.md).</span></span>

<span data-ttu-id="b476a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b476a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b476a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b476a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b476a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b476a-107">Syntax</span></span>

``` vb
'Declaration
Public Property rgcolumncreate As JET_COLUMNCREATE()
    Get
    Set
'Usage
Dim instance As JET_TABLECREATE
Dim value As JET_COLUMNCREATE()

value = instance.rgcolumncreate

instance.rgcolumncreate = value
```

``` csharp
public JET_COLUMNCREATE[] rgcolumncreate { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="b476a-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="b476a-108">Property value</span></span>

<span data-ttu-id="b476a-109">類型： \[\]</span><span class="sxs-lookup"><span data-stu-id="b476a-109">Type: \[\]</span></span>  

## <a name="see-also"></a><span data-ttu-id="b476a-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b476a-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b476a-111">參考</span><span class="sxs-lookup"><span data-stu-id="b476a-111">Reference</span></span>

[<span data-ttu-id="b476a-112">JET_TABLECREATE 類別</span><span class="sxs-lookup"><span data-stu-id="b476a-112">JET_TABLECREATE class</span></span>](./jet-tablecreate-class.md)

[<span data-ttu-id="b476a-113">JET_TABLECREATE 成員</span><span class="sxs-lookup"><span data-stu-id="b476a-113">JET_TABLECREATE members</span></span>](./jet-tablecreate-members.md)

[<span data-ttu-id="b476a-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b476a-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
