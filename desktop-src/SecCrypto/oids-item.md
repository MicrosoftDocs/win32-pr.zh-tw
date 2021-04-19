---
description: 從集合中捕獲 OID 物件。 這是預設屬性。
ms.assetid: af0de567-e520-411d-850d-fbdbcb2ace69
title: Oid。 Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dfdf65f013c5e5e1a031c03c19af9d08b8fc72c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991551"
---
# <a name="oidsitem-property"></a><span data-ttu-id="db30e-104">Oid。 Item 屬性</span><span class="sxs-lookup"><span data-stu-id="db30e-104">OIDs.Item property</span></span>

<span data-ttu-id="db30e-105">\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="db30e-105">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="db30e-106">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="db30e-106">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="db30e-107">**Item** 屬性會從集合中抓取 [**OID**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="db30e-107">The **Item** property retrieves an [**OID**](oid.md) object from the collection.</span></span> <span data-ttu-id="db30e-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="db30e-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="db30e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="db30e-109">Syntax</span></span>


```VB
OIDs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="db30e-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="db30e-110">Property value</span></span>

<span data-ttu-id="db30e-111">位於指定之索引處的 [**oid**](oid.md) 物件，或具有指定點值的 **oid** 物件。</span><span class="sxs-lookup"><span data-stu-id="db30e-111">The [**OID**](oid.md) object at the specified index, or the **OID** object with the specified dotted value.</span></span>

## <a name="requirements"></a><span data-ttu-id="db30e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="db30e-112">Requirements</span></span>



| <span data-ttu-id="db30e-113">需求</span><span class="sxs-lookup"><span data-stu-id="db30e-113">Requirement</span></span> | <span data-ttu-id="db30e-114">值</span><span class="sxs-lookup"><span data-stu-id="db30e-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="db30e-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="db30e-115">Redistributable</span></span><br/> | <span data-ttu-id="db30e-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="db30e-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="db30e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="db30e-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="db30e-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db30e-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db30e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="db30e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db30e-120">**Oid**</span><span class="sxs-lookup"><span data-stu-id="db30e-120">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
