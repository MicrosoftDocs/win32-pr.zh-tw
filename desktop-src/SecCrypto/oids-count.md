---
description: 抓取集合中的 Oid 數目。
ms.assetid: 074ab4a2-b48e-4f43-8ea2-9d28477b2b33
title: Oid 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 602ef914dbeb5fe0664f517b85fbb6935a0b4e1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990106"
---
# <a name="oidscount-property"></a><span data-ttu-id="fd09d-103">Oid 屬性</span><span class="sxs-lookup"><span data-stu-id="fd09d-103">OIDs.Count property</span></span>

<span data-ttu-id="fd09d-104">\[[ **計數** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="fd09d-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fd09d-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="fd09d-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="fd09d-106">**Count** 屬性會抓取集合中的 oid 數目。</span><span class="sxs-lookup"><span data-stu-id="fd09d-106">The **Count** property retrieves the number of OIDs in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd09d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd09d-107">Syntax</span></span>


```VB
OIDs.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="fd09d-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="fd09d-108">Property value</span></span>

<span data-ttu-id="fd09d-109">集合中的 [**OID**](oid.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="fd09d-109">Number of [**OID**](oid.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd09d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="fd09d-110">Requirements</span></span>



| <span data-ttu-id="fd09d-111">需求</span><span class="sxs-lookup"><span data-stu-id="fd09d-111">Requirement</span></span> | <span data-ttu-id="fd09d-112">值</span><span class="sxs-lookup"><span data-stu-id="fd09d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fd09d-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="fd09d-113">Redistributable</span></span><br/> | <span data-ttu-id="fd09d-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="fd09d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fd09d-115">DLL</span><span class="sxs-lookup"><span data-stu-id="fd09d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="fd09d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fd09d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd09d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd09d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd09d-118">**Oid**</span><span class="sxs-lookup"><span data-stu-id="fd09d-118">**OIDs**</span></span>](oids.md)
</dt> </dl>

 

 
