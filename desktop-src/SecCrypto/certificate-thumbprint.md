---
description: 抓取包含憑證之 SHA-1 雜湊的十六進位字串。
ms.assetid: 6fd6f3ba-f7a9-43a3-a8da-8fd826649a92
title: Certificate. Thumbprint 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Thumbprint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c576c46ecf669d215c5bd20a80a0e5a65e3d4706
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998706"
---
# <a name="certificatethumbprint-property"></a><span data-ttu-id="1665d-103">Certificate. Thumbprint 屬性</span><span class="sxs-lookup"><span data-stu-id="1665d-103">Certificate.Thumbprint property</span></span>

<span data-ttu-id="1665d-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1665d-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="1665d-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="1665d-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="1665d-106">[ **指紋** ] 屬性會抓取包含憑證之 [*sha-1*](../secgloss/s-gly.md) 雜湊的十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="1665d-106">The **Thumbprint** property retrieves a hexadecimal string that contains the [*SHA-1*](../secgloss/s-gly.md) hash of the certificate.</span></span>

<span data-ttu-id="1665d-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="1665d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1665d-108">語法</span><span class="sxs-lookup"><span data-stu-id="1665d-108">Syntax</span></span>


```VB
Certificate.Thumbprint As String
```



## <a name="property-value"></a><span data-ttu-id="1665d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="1665d-109">Property value</span></span>

<span data-ttu-id="1665d-110">包含憑證之 SHA-1 雜湊的十六進位字串。</span><span class="sxs-lookup"><span data-stu-id="1665d-110">A hexadecimal string that contains the SHA-1 hash of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="1665d-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="1665d-111">Requirements</span></span>



| <span data-ttu-id="1665d-112">需求</span><span class="sxs-lookup"><span data-stu-id="1665d-112">Requirement</span></span> | <span data-ttu-id="1665d-113">值</span><span class="sxs-lookup"><span data-stu-id="1665d-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1665d-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1665d-114">End of client support</span></span><br/> | <span data-ttu-id="1665d-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1665d-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1665d-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1665d-116">End of server support</span></span><br/> | <span data-ttu-id="1665d-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1665d-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1665d-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1665d-118">Redistributable</span></span><br/>       | <span data-ttu-id="1665d-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1665d-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1665d-120">DLL</span><span class="sxs-lookup"><span data-stu-id="1665d-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1665d-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1665d-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1665d-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1665d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1665d-123">**憑證**</span><span class="sxs-lookup"><span data-stu-id="1665d-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
