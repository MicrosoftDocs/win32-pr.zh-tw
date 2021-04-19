---
description: 深入瞭解： JET_OPENTEMPORARYTABLE cbKeyMost 屬性
title: 'JET_OPENTEMPORARYTABLE. cbKeyMost 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbKeyMost property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbkeymost(v=EXCHG.10)
ms:contentKeyID: 55104228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbKeyMost
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbKeyMost
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8e608d1419cd381c507874bf1f1c334d192ae2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975916"
---
# <a name="jet_opentemporarytablecbkeymost-property"></a><span data-ttu-id="72954-103">JET_OPENTEMPORARYTABLE cbKeyMost 屬性</span><span class="sxs-lookup"><span data-stu-id="72954-103">JET_OPENTEMPORARYTABLE.cbKeyMost property</span></span>

<span data-ttu-id="72954-104">取得或設定表示指定資料列之索引鍵的大小上限。</span><span class="sxs-lookup"><span data-stu-id="72954-104">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="72954-105">您可以設定最大索引鍵大小來控制如何截斷金鑰。</span><span class="sxs-lookup"><span data-stu-id="72954-105">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="72954-106">金鑰截斷很重要，因為它可能會影響資料列視為相異的時間。</span><span class="sxs-lookup"><span data-stu-id="72954-106">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="72954-107">如果此參數設定為0或255，則最大的索引鍵大小及其語義將會與 Windows Server 2003 所支援的最大金鑰大小保持一致。</span><span class="sxs-lookup"><span data-stu-id="72954-107">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="72954-108">此參數也可以設定為較大的值，做為實例 [DatabasePageSize](./jet-param-enumeration.md)之資料庫頁面大小的功能。</span><span class="sxs-lookup"><span data-stu-id="72954-108">This parameter may also be set to a larger value as a function of the database page size for the instance [DatabasePageSize](./jet-param-enumeration.md).</span></span> <span data-ttu-id="72954-109">如需詳細資訊，請參閱 [KeyMost](./vistaparam.keymost-field.md) 。</span><span class="sxs-lookup"><span data-stu-id="72954-109">See [KeyMost](./vistaparam.keymost-field.md) for more information.</span></span>

<span data-ttu-id="72954-110">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="72954-110">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="72954-111">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="72954-111">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="72954-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="72954-112">Syntax</span></span>

``` vb
'Declaration
Public Property cbKeyMost As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbKeyMost

instance.cbKeyMost = value
```

``` csharp
public int cbKeyMost { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="72954-113">屬性值</span><span class="sxs-lookup"><span data-stu-id="72954-113">Property value</span></span>

<span data-ttu-id="72954-114">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="72954-114">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="72954-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72954-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="72954-116">參考</span><span class="sxs-lookup"><span data-stu-id="72954-116">Reference</span></span>

[<span data-ttu-id="72954-117">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="72954-117">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="72954-118">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="72954-118">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="72954-119">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="72954-119">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
