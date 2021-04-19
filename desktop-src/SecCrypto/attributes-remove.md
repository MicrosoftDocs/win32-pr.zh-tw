---
description: 從集合中移除已編制索引的屬性物件。
ms.assetid: 6d9423e3-ab24-4973-b0aa-32e38abd607a
title: Attributes. Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e5981176afb332254d98171d40027e43383cb557
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990295"
---
# <a name="attributesremove-method"></a><span data-ttu-id="62023-103">Attributes. Remove 方法</span><span class="sxs-lookup"><span data-stu-id="62023-103">Attributes.Remove method</span></span>

<span data-ttu-id="62023-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="62023-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="62023-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="62023-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="62023-106">**Remove** 方法會從集合中移除已編制索引的 [**屬性**](attribute.md)物件。</span><span class="sxs-lookup"><span data-stu-id="62023-106">The **Remove** method removes an indexed [**Attribute**](attribute.md) object from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="62023-107">語法</span><span class="sxs-lookup"><span data-stu-id="62023-107">Syntax</span></span>


```VB
Attributes.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="62023-108">參數</span><span class="sxs-lookup"><span data-stu-id="62023-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62023-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62023-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62023-110">要移除之 [**屬性**](attribute.md) 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="62023-110">Index of the [**Attribute**](attribute.md) object to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62023-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62023-111">Return value</span></span>

<span data-ttu-id="62023-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="62023-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62023-113">備註</span><span class="sxs-lookup"><span data-stu-id="62023-113">Remarks</span></span>

<span data-ttu-id="62023-114">使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="62023-114">Applications that use this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="62023-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="62023-115">Requirements</span></span>



| <span data-ttu-id="62023-116">需求</span><span class="sxs-lookup"><span data-stu-id="62023-116">Requirement</span></span> | <span data-ttu-id="62023-117">值</span><span class="sxs-lookup"><span data-stu-id="62023-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62023-118">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="62023-118">End of client support</span></span><br/> | <span data-ttu-id="62023-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62023-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="62023-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="62023-120">End of server support</span></span><br/> | <span data-ttu-id="62023-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62023-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="62023-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="62023-122">Redistributable</span></span><br/>       | <span data-ttu-id="62023-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="62023-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="62023-124">DLL</span><span class="sxs-lookup"><span data-stu-id="62023-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="62023-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62023-125"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62023-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62023-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62023-127">加密物件</span><span class="sxs-lookup"><span data-stu-id="62023-127">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="62023-128">**屬性**</span><span class="sxs-lookup"><span data-stu-id="62023-128">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
