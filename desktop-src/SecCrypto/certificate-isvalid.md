---
description: 建立憑證的憑證驗證鏈，並傳回包含憑證有效狀態的 CertificateStatus 物件。
ms.assetid: 4463e4ac-60a5-4845-93b3-35d2f83bd86e
title: ICertificate2：： IsValid 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IsValid
- ICertificate2.IsValid
- ICertificate.IsValid
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39fec7c1bd2b369ee512834ed1b58b59871d8ae5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982928"
---
# <a name="icertificate2isvalid-method"></a><span data-ttu-id="91966-103">ICertificate2：： IsValid 方法</span><span class="sxs-lookup"><span data-stu-id="91966-103">ICertificate2::IsValid method</span></span>

<span data-ttu-id="91966-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="91966-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="91966-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="91966-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="91966-106">**IsValid** 方法會建立憑證的憑證驗證鏈，並傳回包含憑證有效狀態的 [**CertificateStatus**](certificatestatus.md)物件。</span><span class="sxs-lookup"><span data-stu-id="91966-106">The **IsValid** method builds a certificate verification chain for a certificate and returns a [**CertificateStatus**](certificatestatus.md) object that contains the validity status of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="91966-107">語法</span><span class="sxs-lookup"><span data-stu-id="91966-107">Syntax</span></span>


```VB
Certificate.IsValid()
```



## <a name="parameters"></a><span data-ttu-id="91966-108">參數</span><span class="sxs-lookup"><span data-stu-id="91966-108">Parameters</span></span>

<span data-ttu-id="91966-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="91966-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="91966-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="91966-110">Requirements</span></span>



| <span data-ttu-id="91966-111">需求</span><span class="sxs-lookup"><span data-stu-id="91966-111">Requirement</span></span> | <span data-ttu-id="91966-112">值</span><span class="sxs-lookup"><span data-stu-id="91966-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="91966-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="91966-113">End of client support</span></span><br/> | <span data-ttu-id="91966-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91966-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="91966-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="91966-115">End of server support</span></span><br/> | <span data-ttu-id="91966-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91966-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="91966-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="91966-117">Redistributable</span></span><br/>       | <span data-ttu-id="91966-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="91966-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="91966-119">DLL</span><span class="sxs-lookup"><span data-stu-id="91966-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="91966-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91966-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91966-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="91966-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91966-122">加密物件</span><span class="sxs-lookup"><span data-stu-id="91966-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="91966-123">**憑證**</span><span class="sxs-lookup"><span data-stu-id="91966-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
