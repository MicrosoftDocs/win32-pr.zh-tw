---
description: 代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。
ms.assetid: 08eb7c77-0224-4ab5-99e7-edf18eb23c60
title: EKU 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ff397ae747ecd09dd1292e5c15eb4291692d9651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001926"
---
# <a name="eku-object"></a><span data-ttu-id="18f00-103">EKU 物件</span><span class="sxs-lookup"><span data-stu-id="18f00-103">EKU object</span></span>

<span data-ttu-id="18f00-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="18f00-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="18f00-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="18f00-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="18f00-106">**Eku** 物件代表憑證 (EKU) 屬性的單一擴充金鑰使用方式。</span><span class="sxs-lookup"><span data-stu-id="18f00-106">The **EKU** object represents a single extended key usage (EKU) property of a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="18f00-107">成員</span><span class="sxs-lookup"><span data-stu-id="18f00-107">Members</span></span>

<span data-ttu-id="18f00-108">**EKU** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="18f00-108">The **EKU** object has these types of members:</span></span>

-   [<span data-ttu-id="18f00-109">屬性</span><span class="sxs-lookup"><span data-stu-id="18f00-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="18f00-110">屬性</span><span class="sxs-lookup"><span data-stu-id="18f00-110">Properties</span></span>

<span data-ttu-id="18f00-111">**EKU** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="18f00-111">The **EKU** object has these properties.</span></span>



| <span data-ttu-id="18f00-112">屬性</span><span class="sxs-lookup"><span data-stu-id="18f00-112">Property</span></span>                            | <span data-ttu-id="18f00-113">存取類型</span><span class="sxs-lookup"><span data-stu-id="18f00-113">Access type</span></span>           | <span data-ttu-id="18f00-114">Description</span><span class="sxs-lookup"><span data-stu-id="18f00-114">Description</span></span>                                                                                                                                                                                                   |
|:------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="18f00-115">**Name**</span><span class="sxs-lookup"><span data-stu-id="18f00-115">**Name**</span></span>](eku-name.md)<br/> | <span data-ttu-id="18f00-116">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18f00-116">Read/write</span></span><br/> | <span data-ttu-id="18f00-117">設定或抓取指定 EKU 之 CAPICOM 名稱的列舉值。</span><span class="sxs-lookup"><span data-stu-id="18f00-117">Sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="18f00-118">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="18f00-118">This is the default property.</span></span><br/>                                                                                   |
| [<span data-ttu-id="18f00-119">**老**</span><span class="sxs-lookup"><span data-stu-id="18f00-119">**OID**</span></span>](eku-oid.md)<br/>   | <span data-ttu-id="18f00-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="18f00-120">Read/write</span></span><br/> | <span data-ttu-id="18f00-121">設定或抓取包含 EKU [*物件識別碼*](../secgloss/o-gly.md) 的字串， (OID) 字串值，如 Wincrypt 中所定義。</span><span class="sxs-lookup"><span data-stu-id="18f00-121">Sets or retrieves a string that contains an EKU [*object identifier*](../secgloss/o-gly.md) (OID) string value as defined in Wincrypt.h.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="18f00-122">備註</span><span class="sxs-lookup"><span data-stu-id="18f00-122">Remarks</span></span>

<span data-ttu-id="18f00-123">下列集合和屬性會使用 **EKU** 物件：</span><span class="sxs-lookup"><span data-stu-id="18f00-123">The **EKU** object is used by the following collection and property:</span></span>

-   <span data-ttu-id="18f00-124">[**Eku**](ekus.md) 集合</span><span class="sxs-lookup"><span data-stu-id="18f00-124">[**EKUs**](ekus.md) collection</span></span>
-   <span data-ttu-id="18f00-125">[**CERTIFICATESTATUS EKU**](certificatestatus-eku.md) 屬性</span><span class="sxs-lookup"><span data-stu-id="18f00-125">[**CertificateStatus.EKU**](certificatestatus-eku.md) property</span></span>

<span data-ttu-id="18f00-126">無法建立 **EKU** 物件。</span><span class="sxs-lookup"><span data-stu-id="18f00-126">The **EKU** object cannot be created.</span></span>

## <a name="requirements"></a><span data-ttu-id="18f00-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="18f00-127">Requirements</span></span>



| <span data-ttu-id="18f00-128">需求</span><span class="sxs-lookup"><span data-stu-id="18f00-128">Requirement</span></span> | <span data-ttu-id="18f00-129">值</span><span class="sxs-lookup"><span data-stu-id="18f00-129">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="18f00-130">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="18f00-130">End of client support</span></span><br/> | <span data-ttu-id="18f00-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18f00-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="18f00-132">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="18f00-132">End of server support</span></span><br/> | <span data-ttu-id="18f00-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18f00-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="18f00-134">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="18f00-134">Redistributable</span></span><br/>       | <span data-ttu-id="18f00-135">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="18f00-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="18f00-136">DLL</span><span class="sxs-lookup"><span data-stu-id="18f00-136">DLL</span></span><br/>                   | <dl> <span data-ttu-id="18f00-137"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18f00-137"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
