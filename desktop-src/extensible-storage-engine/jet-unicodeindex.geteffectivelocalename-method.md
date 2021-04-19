---
description: 深入瞭解： JET_UNICODEINDEX。GetEffectiveLocaleName 方法
title: JET_UNICODEINDEX。GetEffectiveLocaleName 方法
TOCTitle: 'GetEffectiveLocaleName method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_unicodeindex.geteffectivelocalename(v=EXCHG.10)
ms:contentKeyID: 55103988
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX.GetEffectiveLocaleName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 012ed93015705454efdf5e329d4b385924f1a343
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972371"
---
# <a name="jet_unicodeindexgeteffectivelocalename-method"></a><span data-ttu-id="4b7b9-103">JET_UNICODEINDEX。GetEffectiveLocaleName 方法</span><span class="sxs-lookup"><span data-stu-id="4b7b9-103">JET_UNICODEINDEX.GetEffectiveLocaleName method</span></span>

<span data-ttu-id="4b7b9-104">為了因應沒有 LCID 支援之系統的因應措施，我們會將非常有限數目的 Lcid 轉換成地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b9-104">As a workaround for systems that do not have LCID support, we will convert a VERY limited number of LCIDs to locale names.</span></span>

<span data-ttu-id="4b7b9-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="4b7b9-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="4b7b9-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="4b7b9-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7b9-107">語法</span><span class="sxs-lookup"><span data-stu-id="4b7b9-107">Syntax</span></span>

``` vb
'Declaration
Public Function GetEffectiveLocaleName As String
'Usage
Dim instance As JET_UNICODEINDEX
Dim returnValue As String

returnValue = instance.GetEffectiveLocaleName()
```

``` csharp
public string GetEffectiveLocaleName()
```

#### <a name="return-value"></a><span data-ttu-id="4b7b9-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b7b9-108">Return value</span></span>

<span data-ttu-id="4b7b9-109">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="4b7b9-109">Type: [System.String](/dotnet/api/system.string)</span></span>  
<span data-ttu-id="4b7b9-110">BCP-47 樣式的地區設定名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b9-110">A BCP-47 style locale name.</span></span>  

## <a name="see-also"></a><span data-ttu-id="4b7b9-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b7b9-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="4b7b9-112">參考</span><span class="sxs-lookup"><span data-stu-id="4b7b9-112">Reference</span></span>

[<span data-ttu-id="4b7b9-113">JET_UNICODEINDEX 類別</span><span class="sxs-lookup"><span data-stu-id="4b7b9-113">JET_UNICODEINDEX class</span></span>](./jet-unicodeindex-class.md)

[<span data-ttu-id="4b7b9-114">JET_UNICODEINDEX 成員</span><span class="sxs-lookup"><span data-stu-id="4b7b9-114">JET_UNICODEINDEX members</span></span>](./jet-unicodeindex-members.md)

[<span data-ttu-id="4b7b9-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="4b7b9-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
