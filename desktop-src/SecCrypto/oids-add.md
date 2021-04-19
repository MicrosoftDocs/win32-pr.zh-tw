---
description: 將指定的 OID 物件加入至集合。
ms.assetid: 0ae087d6-768a-4538-b834-0f936680de05
title: Oid. Add 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d2fa007798a0657991ec8e37a7dddc9fb4c95b2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981371"
---
# <a name="oidsadd-method"></a><span data-ttu-id="8a007-103">Oid. Add 方法</span><span class="sxs-lookup"><span data-stu-id="8a007-103">OIDs.Add method</span></span>

<span data-ttu-id="8a007-104">\[**Add** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="8a007-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="8a007-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="8a007-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="8a007-106">**Add** 方法會將指定的 [**OID**](oid.md)物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="8a007-106">The **Add** method adds the specified [**OID**](oid.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a007-107">語法</span><span class="sxs-lookup"><span data-stu-id="8a007-107">Syntax</span></span>


```VB
OIDs.Add( _
  ByVal OID _
)
```



## <a name="parameters"></a><span data-ttu-id="8a007-108">參數</span><span class="sxs-lookup"><span data-stu-id="8a007-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a007-109">*OID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a007-109">*OID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a007-110">要加入至集合的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="8a007-110">The [**OID**](oid.md) object to be added to the collection.</span></span> <span data-ttu-id="8a007-111">**OID** 物件會根據其點值以排序的順序加入。</span><span class="sxs-lookup"><span data-stu-id="8a007-111">The **OID** object is added in sorted order based on its dotted value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a007-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a007-112">Return value</span></span>

<span data-ttu-id="8a007-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8a007-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a007-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a007-114">Requirements</span></span>



| <span data-ttu-id="8a007-115">需求</span><span class="sxs-lookup"><span data-stu-id="8a007-115">Requirement</span></span> | <span data-ttu-id="8a007-116">值</span><span class="sxs-lookup"><span data-stu-id="8a007-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a007-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8a007-117">Redistributable</span></span><br/> | <span data-ttu-id="8a007-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8a007-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8a007-119">DLL</span><span class="sxs-lookup"><span data-stu-id="8a007-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="8a007-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a007-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
