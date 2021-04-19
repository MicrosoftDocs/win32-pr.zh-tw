---
description: Item 屬性會依據索引，從集合中抓取延伸。 這是預設屬性。
ms.assetid: 0242dc14-abf2-49df-b75a-9005b2376cfc
title: Extension. Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extensions.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b2cefe9ac1dd278c17161cc8e2349c051dccabff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989753"
---
# <a name="extensionsitem-property"></a><span data-ttu-id="0cf56-104">Extension. Item 屬性</span><span class="sxs-lookup"><span data-stu-id="0cf56-104">Extensions.Item property</span></span>

<span data-ttu-id="0cf56-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="0cf56-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="0cf56-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="0cf56-106">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="0cf56-107">**Item** 屬性會依據索引，從集合中抓取延伸。</span><span class="sxs-lookup"><span data-stu-id="0cf56-107">The **Item** property retrieves an extension, by index, from the collection.</span></span> <span data-ttu-id="0cf56-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="0cf56-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cf56-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cf56-109">Syntax</span></span>


```VB
Extensions.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="0cf56-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="0cf56-110">Property value</span></span>

<span data-ttu-id="0cf56-111">代表集合之索引憑證延伸的 [**擴充**](extension.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0cf56-111">An [**Extension**](extension.md) object that represents the indexed certificate extension of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cf56-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0cf56-112">Requirements</span></span>



| <span data-ttu-id="0cf56-113">需求</span><span class="sxs-lookup"><span data-stu-id="0cf56-113">Requirement</span></span> | <span data-ttu-id="0cf56-114">值</span><span class="sxs-lookup"><span data-stu-id="0cf56-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0cf56-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="0cf56-115">End of client support</span></span><br/> | <span data-ttu-id="0cf56-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0cf56-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="0cf56-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="0cf56-117">End of server support</span></span><br/> | <span data-ttu-id="0cf56-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0cf56-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="0cf56-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0cf56-119">Redistributable</span></span><br/>       | <span data-ttu-id="0cf56-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0cf56-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="0cf56-121">DLL</span><span class="sxs-lookup"><span data-stu-id="0cf56-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="0cf56-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cf56-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cf56-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0cf56-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cf56-124">**延伸模組**</span><span class="sxs-lookup"><span data-stu-id="0cf56-124">**Extensions**</span></span>](extensions.md)
</dt> </dl>

 

 
