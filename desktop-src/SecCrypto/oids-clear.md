---
description: 從集合中清除所有 OID 物件。
ms.assetid: 13c9ecf4-c3fc-4dae-a395-04e5247b3b1f
title: Oid。 Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OIDs.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f89fcc813e5b02dcc9f4d3973feb8f7b41581813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982523"
---
# <a name="oidsclear-method"></a><span data-ttu-id="e147d-103">Oid。 Clear 方法</span><span class="sxs-lookup"><span data-stu-id="e147d-103">OIDs.Clear method</span></span>

<span data-ttu-id="e147d-104">\[**Clear** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e147d-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e147d-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**OidCollection 類別**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="e147d-105">Instead, use the [**OidCollection Class**](/dotnet/api/system.security.cryptography.oidcollection?view=netcore-3.1) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="e147d-106">**Clear** 方法會清除集合中的所有 [**OID**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="e147d-106">The **Clear** method clears all [**OID**](oid.md) objects from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="e147d-107">語法</span><span class="sxs-lookup"><span data-stu-id="e147d-107">Syntax</span></span>


```VB
OIDs.Clear()
```



## <a name="parameters"></a><span data-ttu-id="e147d-108">參數</span><span class="sxs-lookup"><span data-stu-id="e147d-108">Parameters</span></span>

<span data-ttu-id="e147d-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="e147d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e147d-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e147d-110">Return value</span></span>

<span data-ttu-id="e147d-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e147d-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e147d-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e147d-112">Requirements</span></span>



| <span data-ttu-id="e147d-113">需求</span><span class="sxs-lookup"><span data-stu-id="e147d-113">Requirement</span></span> | <span data-ttu-id="e147d-114">值</span><span class="sxs-lookup"><span data-stu-id="e147d-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e147d-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e147d-115">Redistributable</span></span><br/> | <span data-ttu-id="e147d-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e147d-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e147d-117">DLL</span><span class="sxs-lookup"><span data-stu-id="e147d-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="e147d-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e147d-118"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
