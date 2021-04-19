---
description: 設定或抓取可以用來建立憑證鏈的憑證集合。
ms.assetid: cdf378f9-0d71-4dd9-93cc-85f09a51c5fc
title: CertificateStatus 憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 325b5c45fc6ae626363de286a6e131f1782cb83f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989529"
---
# <a name="certificatestatuscertificates-property"></a><span data-ttu-id="6ef0e-103">CertificateStatus 憑證屬性</span><span class="sxs-lookup"><span data-stu-id="6ef0e-103">CertificateStatus.Certificates property</span></span>

<span data-ttu-id="6ef0e-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6ef0e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6ef0e-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="6ef0e-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6ef0e-106">[ **憑證** ] 屬性會設定或抓取可用來建立憑證鏈的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="6ef0e-106">The **Certificates** property sets or retrieves the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ef0e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ef0e-107">Syntax</span></span>


```VB
CertificateStatus.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="6ef0e-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="6ef0e-108">Property value</span></span>

<span data-ttu-id="6ef0e-109">代表憑證集合的 [**憑證**](certificates.md) 物件，這些憑證可以用來建立憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="6ef0e-109">A [**Certificates**](certificates.md) object that represents the collection of certificates that can be used to build the certificate chain.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ef0e-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ef0e-110">Requirements</span></span>



| <span data-ttu-id="6ef0e-111">需求</span><span class="sxs-lookup"><span data-stu-id="6ef0e-111">Requirement</span></span> | <span data-ttu-id="6ef0e-112">值</span><span class="sxs-lookup"><span data-stu-id="6ef0e-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ef0e-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6ef0e-113">End of client support</span></span><br/> | <span data-ttu-id="6ef0e-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ef0e-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6ef0e-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6ef0e-115">End of server support</span></span><br/> | <span data-ttu-id="6ef0e-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ef0e-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6ef0e-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6ef0e-117">Redistributable</span></span><br/>       | <span data-ttu-id="6ef0e-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6ef0e-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ef0e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="6ef0e-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6ef0e-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ef0e-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
