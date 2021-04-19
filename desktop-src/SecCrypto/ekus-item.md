---
description: 抓取代表索引的擴充金鑰使用方式 (EKU) 屬性的 EKU 物件。
ms.assetid: b8c12a7a-e836-48c2-958c-937b3723f85b
title: IEKUs：： Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKUs.Item
- IEKUs.get_Item
- EKUs.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e3eaf8d0b303207aae3ef78cc82771e1436b1027
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978436"
---
# <a name="iekusitem-property"></a><span data-ttu-id="1eef1-103">IEKUs：： Item 屬性</span><span class="sxs-lookup"><span data-stu-id="1eef1-103">IEKUs::Item property</span></span>

<span data-ttu-id="1eef1-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1eef1-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1eef1-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ExtensionCollection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="1eef1-105">Instead, use the [**X509ExtensionCollection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extensioncollection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1eef1-106">**Item** 屬性會抓取代表索引的擴充金鑰使用方式 (eku) 屬性的 [**eku**](eku.md)物件。</span><span class="sxs-lookup"><span data-stu-id="1eef1-106">The **Item** property retrieves the [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

<span data-ttu-id="1eef1-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1eef1-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1eef1-108">語法</span><span class="sxs-lookup"><span data-stu-id="1eef1-108">Syntax</span></span>


```VB
EKUs.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="1eef1-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1eef1-109">Property value</span></span>

<span data-ttu-id="1eef1-110">[**Eku**](eku.md)物件，代表索引的擴充金鑰使用方式 (eku) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1eef1-110">An [**EKU**](eku.md) object that represents the indexed extended key usage (EKU) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1eef1-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1eef1-111">Requirements</span></span>



| <span data-ttu-id="1eef1-112">需求</span><span class="sxs-lookup"><span data-stu-id="1eef1-112">Requirement</span></span> | <span data-ttu-id="1eef1-113">值</span><span class="sxs-lookup"><span data-stu-id="1eef1-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1eef1-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1eef1-114">End of client support</span></span><br/> | <span data-ttu-id="1eef1-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1eef1-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1eef1-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1eef1-116">End of server support</span></span><br/> | <span data-ttu-id="1eef1-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1eef1-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1eef1-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1eef1-118">Redistributable</span></span><br/>       | <span data-ttu-id="1eef1-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1eef1-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1eef1-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1eef1-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1eef1-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1eef1-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1eef1-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1eef1-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1eef1-123">**Eku**</span><span class="sxs-lookup"><span data-stu-id="1eef1-123">**EKUs**</span></span>](ekus.md)
</dt> </dl>

 

 
