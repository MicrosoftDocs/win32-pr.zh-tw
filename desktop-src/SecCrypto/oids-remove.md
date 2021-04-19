---
description: 從集合中移除指定的 OID 物件。
ms.assetid: c5eb6831-b195-4dc1-a6bd-d4245f9b0213
title: Oid. Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 000310e0034d413dea16a45f79647c3e0f7cf52d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001503"
---
# <a name="oidsremove-method"></a><span data-ttu-id="6af9e-103">Oid. Remove 方法</span><span class="sxs-lookup"><span data-stu-id="6af9e-103">OIDs.Remove method</span></span>

<span data-ttu-id="6af9e-104">\[**Remove** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="6af9e-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6af9e-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="6af9e-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6af9e-106">**Remove** 方法會從集合中移除指定的 [**OID**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="6af9e-106">The **Remove** method removes the specified [**OID**](oid.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af9e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6af9e-107">Syntax</span></span>


```VB
OIDs.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="6af9e-108">參數</span><span class="sxs-lookup"><span data-stu-id="6af9e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6af9e-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6af9e-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6af9e-110">要移除之 [**OID**](oid.md) 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="6af9e-110">Index of the [**OID**](oid.md) object to be removed.</span></span> <span data-ttu-id="6af9e-111">這可以是集合中的索引或 OID 的點值。</span><span class="sxs-lookup"><span data-stu-id="6af9e-111">This can be either an index into the collection or the dotted value of the OID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6af9e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6af9e-112">Return value</span></span>

<span data-ttu-id="6af9e-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6af9e-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6af9e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6af9e-114">Requirements</span></span>



| <span data-ttu-id="6af9e-115">需求</span><span class="sxs-lookup"><span data-stu-id="6af9e-115">Requirement</span></span> | <span data-ttu-id="6af9e-116">值</span><span class="sxs-lookup"><span data-stu-id="6af9e-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6af9e-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6af9e-117">Redistributable</span></span><br/> | <span data-ttu-id="6af9e-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6af9e-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6af9e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6af9e-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="6af9e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6af9e-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
