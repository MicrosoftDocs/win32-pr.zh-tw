---
description: 抓取代表索引屬性的屬性物件。
ms.assetid: 35c54c5f-f83f-40eb-b341-129c1aac6181
title: Attributes 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 208e36fd8d4d7e3effc2c0f59b7db921fed76d79
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983072"
---
# <a name="attributesitem-property"></a><span data-ttu-id="920d6-103">Attributes 屬性</span><span class="sxs-lookup"><span data-stu-id="920d6-103">Attributes.Item property</span></span>

<span data-ttu-id="920d6-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="920d6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="920d6-105">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="920d6-105">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="920d6-106">**Item** 屬性會抓取代表索引屬性的 [**屬性**](attribute.md)物件。</span><span class="sxs-lookup"><span data-stu-id="920d6-106">The **Item** property retrieves the [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span> <span data-ttu-id="920d6-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="920d6-107">This is the default property.</span></span>

<span data-ttu-id="920d6-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="920d6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="920d6-109">語法</span><span class="sxs-lookup"><span data-stu-id="920d6-109">Syntax</span></span>


```VB
Attributes.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="920d6-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="920d6-110">Property value</span></span>

<span data-ttu-id="920d6-111">表示已編制索引之屬性的 [**屬性**](attribute.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="920d6-111">An [**Attribute**](attribute.md) object that represents the indexed attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="920d6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="920d6-112">Requirements</span></span>



| <span data-ttu-id="920d6-113">需求</span><span class="sxs-lookup"><span data-stu-id="920d6-113">Requirement</span></span> | <span data-ttu-id="920d6-114">值</span><span class="sxs-lookup"><span data-stu-id="920d6-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="920d6-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="920d6-115">End of client support</span></span><br/> | <span data-ttu-id="920d6-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="920d6-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="920d6-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="920d6-117">End of server support</span></span><br/> | <span data-ttu-id="920d6-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="920d6-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="920d6-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="920d6-119">Redistributable</span></span><br/>       | <span data-ttu-id="920d6-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="920d6-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="920d6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="920d6-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="920d6-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="920d6-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
