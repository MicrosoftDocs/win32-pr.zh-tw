---
description: 深入瞭解： VistaGrbits. IndexDisallowTruncation 欄位
title: VistaGrbits. IndexDisallowTruncation 欄位)  (的欄位
TOCTitle: IndexDisallowTruncation field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits.indexdisallowtruncation(v=EXCHG.10)
ms:contentKeyID: 55104424
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaGrbits.IndexDisallowTruncation
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d359acea8de5b72bc7137feefbc1d1281c07ed57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027581"
---
# <a name="vistagrbitsindexdisallowtruncation-field"></a><span data-ttu-id="c5313-103">VistaGrbits. IndexDisallowTruncation 欄位</span><span class="sxs-lookup"><span data-stu-id="c5313-103">VistaGrbits.IndexDisallowTruncation field</span></span>

<span data-ttu-id="c5313-104">指定此旗標將會導致索引的任何更新會導致截斷的金鑰因 [KeyTruncated](./jet-err-enumeration.md)而失敗。</span><span class="sxs-lookup"><span data-stu-id="c5313-104">Specifying this flag will cause any update to the index that would result in a truncated key to fail with [KeyTruncated](./jet-err-enumeration.md).</span></span> <span data-ttu-id="c5313-105">否則，將會以無訊息方式截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="c5313-105">Otherwise, keys will be silently truncated.</span></span>

<span data-ttu-id="c5313-106">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="c5313-106">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="c5313-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="c5313-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="c5313-108">語法</span><span class="sxs-lookup"><span data-stu-id="c5313-108">Syntax</span></span>

``` vb
'Declaration
Public Const IndexDisallowTruncation As CreateIndexGrbit
'Usage
Dim value As CreateIndexGrbit

value = VistaGrbits.IndexDisallowTruncation
```

``` csharp
public const CreateIndexGrbit IndexDisallowTruncation
```

## <a name="see-also"></a><span data-ttu-id="c5313-109">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5313-109">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5313-110">參考</span><span class="sxs-lookup"><span data-stu-id="c5313-110">Reference</span></span>

[<span data-ttu-id="c5313-111">VistaGrbits 類別</span><span class="sxs-lookup"><span data-stu-id="c5313-111">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="c5313-112">VistaGrbits 成員</span><span class="sxs-lookup"><span data-stu-id="c5313-112">VistaGrbits members</span></span>](./vistagrbits-members.md)

[<span data-ttu-id="c5313-113">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="c5313-113">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
