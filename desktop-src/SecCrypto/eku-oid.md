---
description: 設定或抓取包含 EKU OID 字串值的字串，如 Wincrypt 中所定義。
ms.assetid: 2fdaeddc-5ed6-46a6-a4f7-827a605e890a
title: IEKU：： OID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.OID
- IEKU.get_OID
- IEKU.put_OID
- EKU.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 77a519051d2bd1cb3c948bf0e2271cced7d80a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984331"
---
# <a name="iekuoid-property"></a><span data-ttu-id="ccbc4-103">IEKU：： OID 屬性</span><span class="sxs-lookup"><span data-stu-id="ccbc4-103">IEKU::OID property</span></span>

<span data-ttu-id="ccbc4-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ccbc4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ccbc4-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509EnhancedKeyUsageExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="ccbc4-105">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ccbc4-106">**OID** 屬性會設定或抓取包含 EKU OID 字串值的字串，如 Wincrypt 中所定義。</span><span class="sxs-lookup"><span data-stu-id="ccbc4-106">The **OID** property sets or retrieves a string that contains an EKU OID string value as defined in Wincrypt.h.</span></span>

<span data-ttu-id="ccbc4-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="ccbc4-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccbc4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccbc4-108">Syntax</span></span>


```VB
EKU.OID As String
```



## <a name="property-value"></a><span data-ttu-id="ccbc4-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="ccbc4-109">Property value</span></span>

<span data-ttu-id="ccbc4-110">包含 Wincrypt 中所定義之 EKU OID 字串值的字串。</span><span class="sxs-lookup"><span data-stu-id="ccbc4-110">String that contains the EKU OID string value as defined in Wincrypt.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccbc4-111">備註</span><span class="sxs-lookup"><span data-stu-id="ccbc4-111">Remarks</span></span>

<span data-ttu-id="ccbc4-112">此屬性不會使用在 CAPICOM 2.0 中引進的 [**OID**](oid.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ccbc4-112">This property does not use the [**OID**](oid.md) object introduced in CAPICOM 2.0.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbc4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ccbc4-113">Requirements</span></span>



| <span data-ttu-id="ccbc4-114">需求</span><span class="sxs-lookup"><span data-stu-id="ccbc4-114">Requirement</span></span> | <span data-ttu-id="ccbc4-115">值</span><span class="sxs-lookup"><span data-stu-id="ccbc4-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbc4-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ccbc4-116">End of client support</span></span><br/> | <span data-ttu-id="ccbc4-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ccbc4-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ccbc4-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ccbc4-118">End of server support</span></span><br/> | <span data-ttu-id="ccbc4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ccbc4-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ccbc4-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ccbc4-120">Redistributable</span></span><br/>       | <span data-ttu-id="ccbc4-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ccbc4-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ccbc4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ccbc4-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ccbc4-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ccbc4-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
