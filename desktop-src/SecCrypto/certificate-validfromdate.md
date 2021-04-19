---
description: 捕獲憑證有效性的開始日期。
ms.assetid: d1caa7d3-ed5c-4637-bcb6-5a3fda8b978e
title: Certificate. ValidFromDate 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ValidFromDate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8637114ad471b2d938a94ba2d974703bdfb1f5d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992926"
---
# <a name="certificatevalidfromdate-property"></a><span data-ttu-id="6ebeb-103">Certificate. ValidFromDate 屬性</span><span class="sxs-lookup"><span data-stu-id="6ebeb-103">Certificate.ValidFromDate property</span></span>

<span data-ttu-id="6ebeb-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="6ebeb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="6ebeb-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="6ebeb-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="6ebeb-106">**ValidFromDate** 屬性會捕獲憑證有效性的開始日期。</span><span class="sxs-lookup"><span data-stu-id="6ebeb-106">The **ValidFromDate** property retrieves the beginning date for the validity of the certificate.</span></span>

<span data-ttu-id="6ebeb-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="6ebeb-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebeb-108">語法</span><span class="sxs-lookup"><span data-stu-id="6ebeb-108">Syntax</span></span>


```VB
Certificate.ValidFromDate As Date
```



## <a name="property-value"></a><span data-ttu-id="6ebeb-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="6ebeb-109">Property value</span></span>

<span data-ttu-id="6ebeb-110">表示憑證有效性之開始日期的日期。</span><span class="sxs-lookup"><span data-stu-id="6ebeb-110">A date that indicates the beginning date for the validity of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ebeb-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ebeb-111">Requirements</span></span>



| <span data-ttu-id="6ebeb-112">需求</span><span class="sxs-lookup"><span data-stu-id="6ebeb-112">Requirement</span></span> | <span data-ttu-id="6ebeb-113">值</span><span class="sxs-lookup"><span data-stu-id="6ebeb-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebeb-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="6ebeb-114">End of client support</span></span><br/> | <span data-ttu-id="6ebeb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6ebeb-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6ebeb-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="6ebeb-116">End of server support</span></span><br/> | <span data-ttu-id="6ebeb-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6ebeb-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6ebeb-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6ebeb-118">Redistributable</span></span><br/>       | <span data-ttu-id="6ebeb-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6ebeb-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6ebeb-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6ebeb-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="6ebeb-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ebeb-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ebeb-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6ebeb-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebeb-123">**憑證**</span><span class="sxs-lookup"><span data-stu-id="6ebeb-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
