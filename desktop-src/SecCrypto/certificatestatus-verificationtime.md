---
description: 設定或抓取憑證驗證的時間。
ms.assetid: 1bd17df3-2fa1-4b99-ab00-659b4ad5fcd9
title: CertificateStatus. VerificationTime 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.VerificationTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 178402861c9830efbea78a31081ae7e8b31800b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976765"
---
# <a name="certificatestatusverificationtime-property"></a><span data-ttu-id="83bc2-103">CertificateStatus. VerificationTime 屬性</span><span class="sxs-lookup"><span data-stu-id="83bc2-103">CertificateStatus.VerificationTime property</span></span>

<span data-ttu-id="83bc2-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="83bc2-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="83bc2-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="83bc2-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="83bc2-106">**VerificationTime** 屬性會設定或抓取憑證驗證的時間。</span><span class="sxs-lookup"><span data-stu-id="83bc2-106">The **VerificationTime** property sets or retrieves the time that the certificate was verified.</span></span>

## <a name="syntax"></a><span data-ttu-id="83bc2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="83bc2-107">Syntax</span></span>


```VB
CertificateStatus.VerificationTime As Date
```



## <a name="property-value"></a><span data-ttu-id="83bc2-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="83bc2-108">Property value</span></span>

<span data-ttu-id="83bc2-109">驗證憑證的時間。</span><span class="sxs-lookup"><span data-stu-id="83bc2-109">The time that the certificate was verified.</span></span>

## <a name="remarks"></a><span data-ttu-id="83bc2-110">備註</span><span class="sxs-lookup"><span data-stu-id="83bc2-110">Remarks</span></span>

<span data-ttu-id="83bc2-111">如果未設定此屬性，則會使用目前的時間。</span><span class="sxs-lookup"><span data-stu-id="83bc2-111">If this property is not set, the current time is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="83bc2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="83bc2-112">Requirements</span></span>



| <span data-ttu-id="83bc2-113">需求</span><span class="sxs-lookup"><span data-stu-id="83bc2-113">Requirement</span></span> | <span data-ttu-id="83bc2-114">值</span><span class="sxs-lookup"><span data-stu-id="83bc2-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83bc2-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="83bc2-115">End of client support</span></span><br/> | <span data-ttu-id="83bc2-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83bc2-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="83bc2-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="83bc2-117">End of server support</span></span><br/> | <span data-ttu-id="83bc2-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83bc2-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83bc2-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="83bc2-119">Redistributable</span></span><br/>       | <span data-ttu-id="83bc2-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="83bc2-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="83bc2-121">DLL</span><span class="sxs-lookup"><span data-stu-id="83bc2-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="83bc2-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83bc2-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
