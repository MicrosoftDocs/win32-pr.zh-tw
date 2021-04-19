---
description: 深入瞭解： JET_OPENTEMPORARYTABLE cbVarSegMac 屬性
title: 'JET_OPENTEMPORARYTABLE. cbVarSegMac 屬性 (Microsoft. < a0/&gt; < a1/&gt;) '
TOCTitle: 'cbVarSegMac property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable.cbvarsegmac(v=EXCHG.10)
ms:contentKeyID: 55104115
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.get_cbVarSegMac
- Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE.set_cbVarSegMac
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37fe218a9741235410d2452f04f082dc6673eaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979189"
---
# <a name="jet_opentemporarytablecbvarsegmac-property"></a><span data-ttu-id="ca2c4-103">JET_OPENTEMPORARYTABLE cbVarSegMac 屬性</span><span class="sxs-lookup"><span data-stu-id="ca2c4-103">JET_OPENTEMPORARYTABLE.cbVarSegMac property</span></span>

<span data-ttu-id="ca2c4-104">取得或設定將從任何變數 lengthcolumn 使用的最大資料量，以針對指定的資料列來建立索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ca2c4-104">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="ca2c4-105">此參數可用來控制任何指定的索引鍵資料行所耗用的金鑰空間量。</span><span class="sxs-lookup"><span data-stu-id="ca2c4-105">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="ca2c4-106">這項限制是以位元組為單位。</span><span class="sxs-lookup"><span data-stu-id="ca2c4-106">This limit is in bytes.</span></span> <span data-ttu-id="ca2c4-107">如果此參數為零或與 [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) 屬性相同，則沒有作用中的限制。</span><span class="sxs-lookup"><span data-stu-id="ca2c4-107">If this parameter is zero or is the same as the [cbKeyMost](./jet-opentemporarytable.cbkeymost-property.md) property then no limit is in effect.</span></span>

<span data-ttu-id="ca2c4-108">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="ca2c4-108">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="ca2c4-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="ca2c4-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="ca2c4-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca2c4-110">Syntax</span></span>

``` vb
'Declaration
Public Property cbVarSegMac As Integer
    Get
    Set
'Usage
Dim instance As JET_OPENTEMPORARYTABLE
Dim value As Integer

value = instance.cbVarSegMac

instance.cbVarSegMac = value
```

``` csharp
public int cbVarSegMac { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="ca2c4-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="ca2c4-111">Property value</span></span>

<span data-ttu-id="ca2c4-112">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="ca2c4-112">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="ca2c4-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca2c4-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ca2c4-114">參考</span><span class="sxs-lookup"><span data-stu-id="ca2c4-114">Reference</span></span>

[<span data-ttu-id="ca2c4-115">JET_OPENTEMPORARYTABLE 類別</span><span class="sxs-lookup"><span data-stu-id="ca2c4-115">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="ca2c4-116">JET_OPENTEMPORARYTABLE 成員</span><span class="sxs-lookup"><span data-stu-id="ca2c4-116">JET_OPENTEMPORARYTABLE members</span></span>](./jet-opentemporarytable-members.md)

[<span data-ttu-id="ca2c4-117">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="ca2c4-117">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
