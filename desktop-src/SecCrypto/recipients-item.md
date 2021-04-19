---
description: 從收件者集合抓取物件。
ms.assetid: 03600d4a-5fd4-45c7-ae91-efdc26c084ee
title: 收件者. 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a80b472c8257597356c626a9e88aad97c447f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000005"
---
# <a name="recipientsitem-property"></a><span data-ttu-id="5f51d-103">收件者. 專案屬性</span><span class="sxs-lookup"><span data-stu-id="5f51d-103">Recipients.Item property</span></span>

<span data-ttu-id="5f51d-104">\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5f51d-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5f51d-105">相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="5f51d-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="5f51d-106">**Item** 屬性會從收件 [**者集合抓取**](recipients.md)物件。</span><span class="sxs-lookup"><span data-stu-id="5f51d-106">The **Item** property retrieves an object from the [**Recipients**](recipients.md) collection.</span></span> <span data-ttu-id="5f51d-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="5f51d-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f51d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f51d-108">Syntax</span></span>


```VB
Recipients.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="5f51d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="5f51d-109">Property value</span></span>

<span data-ttu-id="5f51d-110">代表收件 [**者集合中**](recipients.md) 索引項目目的 variant。</span><span class="sxs-lookup"><span data-stu-id="5f51d-110">A variant that represents the indexed item in the [**Recipients**](recipients.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f51d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f51d-111">Requirements</span></span>



| <span data-ttu-id="5f51d-112">需求</span><span class="sxs-lookup"><span data-stu-id="5f51d-112">Requirement</span></span> | <span data-ttu-id="5f51d-113">值</span><span class="sxs-lookup"><span data-stu-id="5f51d-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f51d-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="5f51d-114">Redistributable</span></span><br/> | <span data-ttu-id="5f51d-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="5f51d-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5f51d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5f51d-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="5f51d-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f51d-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f51d-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f51d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f51d-119">**收件者**</span><span class="sxs-lookup"><span data-stu-id="5f51d-119">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
