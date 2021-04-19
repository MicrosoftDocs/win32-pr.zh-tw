---
description: 深入瞭解： JET_OPENTEMPORARYTABLE pidxunicode 屬性
title: 'JET_OPENTEMPORARYTABLE. pidxunicode 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'pidxunicode property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.pidxunicode(v=EXCHG.10)
ms:contentKeyID: 55104227
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_pidxunicode
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.pidxunicode
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 98e5beb4f4523f5e6a6da37a999b6c0a2ab7b4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978377"
---
# <a name="jet_opentemporarytablepidxunicode-property"></a><span data-ttu-id="a8cda-103">JET_OPENTEMPORARYTABLE pidxunicode 屬性</span><span class="sxs-lookup"><span data-stu-id="a8cda-103">JET_OPENTEMPORARYTABLE.pidxunicode property</span></span>

<span data-ttu-id="a8cda-104">取得或設定要用來比較臨時表中任何 Unicode 索引鍵資料行資料的地區設定識別碼和正規化旗標。</span><span class="sxs-lookup"><span data-stu-id="a8cda-104">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="a8cda-105">當此參數為 null 時，預設的 LCID 將用來比較臨時表中的任何 Unicode 索引鍵資料行。</span><span class="sxs-lookup"><span data-stu-id="a8cda-105">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="a8cda-106">預設的 LCID 是美國英文地區設定。</span><span class="sxs-lookup"><span data-stu-id="a8cda-106">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="a8cda-107">當此參數為 null 時，將會使用預設正規化旗標來比較臨時表中的任何 Unicode 索引鍵資料行資料。</span><span class="sxs-lookup"><span data-stu-id="a8cda-107">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="a8cda-108">預設正規化旗標為： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。</span><span class="sxs-lookup"><span data-stu-id="a8cda-108">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="a8cda-109">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="a8cda-109">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="a8cda-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a8cda-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a8cda-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8cda-111">Syntax</span></span>

``` vb
'Declaration
Public Property pidxunicode As JET_UNICODEINDEX
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As JET_UNICODEINDEX

value = instance.pidxunicode

instance.pidxunicode = value
```

``` csharp
public JET_UNICODEINDEX pidxunicode { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="a8cda-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="a8cda-112">Property value</span></span>

<span data-ttu-id="a8cda-113">類型： [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span><span class="sxs-lookup"><span data-stu-id="a8cda-113">Type: [Microsoft.Isam.Esent.Interop.JET_UNICODEINDEX](./jet-unicodeindex-class.md)</span></span>  

## <a name="see-also"></a><span data-ttu-id="a8cda-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8cda-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a8cda-115">參考</span><span class="sxs-lookup"><span data-stu-id="a8cda-115">Reference</span></span>

[<span data-ttu-id="a8cda-116">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="a8cda-116">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="a8cda-117">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="a8cda-117">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="a8cda-118">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="a8cda-118">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
