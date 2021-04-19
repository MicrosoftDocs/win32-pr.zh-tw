---
description: 深入瞭解： JET_UNICODEINDEX dwMapFlags 屬性
title: JET_UNICODEINDEX dwMapFlags 屬性
TOCTitle: 'dwMapFlags property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.dwmapflags(v=EXCHG.10)
ms:contentKeyID: 55103990
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.set_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.get_dwMapFlags
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.dwMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a625da5f80271b52f6eff74a2427e749219e46a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990341"
---
# <a name="jet_unicodeindexdwmapflags-property"></a><span data-ttu-id="3645b-103">JET_UNICODEINDEX dwMapFlags 屬性</span><span class="sxs-lookup"><span data-stu-id="3645b-103">JET_UNICODEINDEX.dwMapFlags property</span></span>

<span data-ttu-id="3645b-104">取得或設定正規化 unicode 資料時，要與 LCMapString 搭配使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="3645b-104">Gets or sets the flags to be used with LCMapString when normalizing unicode data.</span></span>

<span data-ttu-id="3645b-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="3645b-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="3645b-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3645b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3645b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="3645b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3645b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3645b-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Property dwMapFlags As UInteger
    Get
    Set
'Usage
Dim instance As JET_UNICODEINDEX
Dim value As UInteger

value = instance.dwMapFlags

instance.dwMapFlags = value
```

``` csharp
[CLSCompliantAttribute(false)]
public uint dwMapFlags { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="3645b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="3645b-109">Property value</span></span>

<span data-ttu-id="3645b-110">類型： [system.object](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="3645b-110">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="3645b-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3645b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3645b-112">參考</span><span class="sxs-lookup"><span data-stu-id="3645b-112">Reference</span></span>

[<span data-ttu-id="3645b-113">JET_UNICODEINDEX 類別</span><span class="sxs-lookup"><span data-stu-id="3645b-113">JET_UNICODEINDEX class</span></span>](./jet-unicodeindex-class.md)

[<span data-ttu-id="3645b-114">JET_UNICODEINDEX 成員</span><span class="sxs-lookup"><span data-stu-id="3645b-114">JET_UNICODEINDEX members</span></span>](./jet-unicodeindex-members.md)

[<span data-ttu-id="3645b-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="3645b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
