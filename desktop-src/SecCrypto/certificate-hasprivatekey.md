---
description: 判斷憑證是否有與其相關聯的私密金鑰。 方法會藉由檢查是否 \_ 有 CERT KEY \_ >prov \_ INFO \_ \_ 屬性識別碼屬性來決定這一點。
ms.assetid: 80478956-1ed7-4c25-9ae3-d7176649e6d7
title: ICertificate2：： HasPrivateKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.HasPrivateKey
- ICertificate2.HasPrivateKey
- ICertificate.HasPrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 43110e48a1172977ad979d6ec2d94c5b8e3ffc50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986184"
---
# <a name="icertificate2hasprivatekey-method"></a><span data-ttu-id="2a46b-104">ICertificate2：： HasPrivateKey 方法</span><span class="sxs-lookup"><span data-stu-id="2a46b-104">ICertificate2::HasPrivateKey method</span></span>

<span data-ttu-id="2a46b-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2a46b-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2a46b-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="2a46b-106">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2a46b-107">**HasPrivateKey** 方法會判斷 [*憑證*](../secgloss/c-gly.md)是否有與其相關聯的 [*私密金鑰*](../secgloss/p-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="2a46b-107">The **HasPrivateKey** method determines whether the [*certificate*](../secgloss/c-gly.md) has a [*private key*](../secgloss/p-gly.md) associated with it.</span></span> <span data-ttu-id="2a46b-108">方法會藉由檢查是否 \_ 有 CERT KEY \_ >prov \_ INFO \_ \_ 屬性識別碼屬性來決定這一點。</span><span class="sxs-lookup"><span data-stu-id="2a46b-108">The method determines this by checking whether the CERT\_KEY\_PROV\_INFO\_PROP\_ID property is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a46b-109">語法</span><span class="sxs-lookup"><span data-stu-id="2a46b-109">Syntax</span></span>


```VB
Certificate.HasPrivateKey()
```



## <a name="parameters"></a><span data-ttu-id="2a46b-110">參數</span><span class="sxs-lookup"><span data-stu-id="2a46b-110">Parameters</span></span>

<span data-ttu-id="2a46b-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2a46b-111">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a46b-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a46b-112">Requirements</span></span>



| <span data-ttu-id="2a46b-113">需求</span><span class="sxs-lookup"><span data-stu-id="2a46b-113">Requirement</span></span> | <span data-ttu-id="2a46b-114">值</span><span class="sxs-lookup"><span data-stu-id="2a46b-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a46b-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2a46b-115">End of client support</span></span><br/> | <span data-ttu-id="2a46b-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a46b-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2a46b-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2a46b-117">End of server support</span></span><br/> | <span data-ttu-id="2a46b-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a46b-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2a46b-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2a46b-119">Redistributable</span></span><br/>       | <span data-ttu-id="2a46b-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2a46b-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2a46b-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2a46b-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2a46b-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a46b-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a46b-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a46b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a46b-124">**PrivateKey。開啟**</span><span class="sxs-lookup"><span data-stu-id="2a46b-124">**PrivateKey.Open**</span></span>](privatekey-open.md)
</dt> <dt>

[<span data-ttu-id="2a46b-125">加密物件</span><span class="sxs-lookup"><span data-stu-id="2a46b-125">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="2a46b-126">**憑證**</span><span class="sxs-lookup"><span data-stu-id="2a46b-126">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
