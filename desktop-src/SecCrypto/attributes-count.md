---
description: 抓取集合中的屬性物件數目。
ms.assetid: d5f9db7d-52a2-4feb-8d35-902caf536510
title: Attributes 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34a750b34f483342966ed1fcb3831d08b8df8f39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992583"
---
# <a name="attributescount-property"></a><span data-ttu-id="f395d-103">Attributes 屬性</span><span class="sxs-lookup"><span data-stu-id="f395d-103">Attributes.Count property</span></span>

<span data-ttu-id="f395d-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f395d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="f395d-105">請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="f395d-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="f395d-106">**Count** 屬性會抓取集合中的 [**屬性**](attribute.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="f395d-106">The **Count** property retrieves the number of [**Attribute**](attribute.md) objects in the collection.</span></span>

<span data-ttu-id="f395d-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="f395d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f395d-108">語法</span><span class="sxs-lookup"><span data-stu-id="f395d-108">Syntax</span></span>


```VB
Attributes.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="f395d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f395d-109">Property value</span></span>

<span data-ttu-id="f395d-110">集合中的 [**屬性**](attribute.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="f395d-110">The number of [**Attribute**](attribute.md) objects in the collection.</span></span> <span data-ttu-id="f395d-111">每個 **屬性** 物件都代表集合中的單一屬性。</span><span class="sxs-lookup"><span data-stu-id="f395d-111">Each **Attribute** object represents a single attribute in the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="f395d-112">備註</span><span class="sxs-lookup"><span data-stu-id="f395d-112">Remarks</span></span>

<span data-ttu-id="f395d-113">當使用 [**Attributes**](attributes-item.md)屬性來抓取特定 **屬性** 物件時，可以使用 **Count** 屬性來指定集合中的最後一個 [**屬性**](attribute.md)物件。</span><span class="sxs-lookup"><span data-stu-id="f395d-113">The **Count** property can be used to specify the last [**Attribute**](attribute.md) object in the collection when retrieving a specific **Attribute** object by using the [**Attributes.Item**](attributes-item.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="f395d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f395d-114">Requirements</span></span>



| <span data-ttu-id="f395d-115">需求</span><span class="sxs-lookup"><span data-stu-id="f395d-115">Requirement</span></span> | <span data-ttu-id="f395d-116">值</span><span class="sxs-lookup"><span data-stu-id="f395d-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f395d-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f395d-117">End of client support</span></span><br/> | <span data-ttu-id="f395d-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f395d-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f395d-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f395d-119">End of server support</span></span><br/> | <span data-ttu-id="f395d-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f395d-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f395d-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f395d-121">Redistributable</span></span><br/>       | <span data-ttu-id="f395d-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f395d-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f395d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f395d-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f395d-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f395d-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f395d-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f395d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f395d-126">**屬性**</span><span class="sxs-lookup"><span data-stu-id="f395d-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
