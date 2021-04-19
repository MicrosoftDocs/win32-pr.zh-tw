---
description: 將屬性物件加入至集合。
ms.assetid: dc2fe542-7168-4ffa-a10d-b2c051c4d42c
title: 屬性。新增方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 824bff2fcca190e25f9b9c63ba0964674aff9fb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979472"
---
# <a name="attributesadd-method"></a><span data-ttu-id="a0016-103">屬性。新增方法</span><span class="sxs-lookup"><span data-stu-id="a0016-103">Attributes.Add method</span></span>

<span data-ttu-id="a0016-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a0016-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="a0016-105">請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="a0016-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="a0016-106">**Add** 方法會將 [**屬性**](attribute.md)物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="a0016-106">The **Add** method adds an [**Attribute**](attribute.md) object to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0016-107">語法</span><span class="sxs-lookup"><span data-stu-id="a0016-107">Syntax</span></span>


```VB
Attributes.Add( _
  ByVal Attribute _
)
```



## <a name="parameters"></a><span data-ttu-id="a0016-108">參數</span><span class="sxs-lookup"><span data-stu-id="a0016-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0016-109">*屬性* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a0016-109">*Attribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0016-110">要加入至集合結尾的 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a0016-110">The [**Attribute**](attribute.md) object to be added at the end of the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0016-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0016-111">Return value</span></span>

<span data-ttu-id="a0016-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a0016-112">This method does not return a value.</span></span> <span data-ttu-id="a0016-113">使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="a0016-113">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0016-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0016-114">Requirements</span></span>



| <span data-ttu-id="a0016-115">需求</span><span class="sxs-lookup"><span data-stu-id="a0016-115">Requirement</span></span> | <span data-ttu-id="a0016-116">值</span><span class="sxs-lookup"><span data-stu-id="a0016-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0016-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a0016-117">End of client support</span></span><br/> | <span data-ttu-id="a0016-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0016-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a0016-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a0016-119">End of server support</span></span><br/> | <span data-ttu-id="a0016-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0016-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a0016-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a0016-121">Redistributable</span></span><br/>       | <span data-ttu-id="a0016-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a0016-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a0016-123">DLL</span><span class="sxs-lookup"><span data-stu-id="a0016-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a0016-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0016-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0016-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0016-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0016-126">加密物件</span><span class="sxs-lookup"><span data-stu-id="a0016-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a0016-127">**屬性**</span><span class="sxs-lookup"><span data-stu-id="a0016-127">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
