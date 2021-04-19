---
description: 傳回 ExtendedKeyUsage 物件，這個物件會指出憑證的有效用法。
ms.assetid: e974e9e2-1011-48b7-9ebc-e754e4990286
title: ICertificate2：： ExtendedKeyUsage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.ExtendedKeyUsage
- ICertificate2.ExtendedKeyUsage
- ICertificate.ExtendedKeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6f349b7267d58a9376b9295e3ffd5013954a0872
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990623"
---
# <a name="icertificate2extendedkeyusage-method"></a><span data-ttu-id="313fd-103">ICertificate2：： ExtendedKeyUsage 方法</span><span class="sxs-lookup"><span data-stu-id="313fd-103">ICertificate2::ExtendedKeyUsage method</span></span>

<span data-ttu-id="313fd-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="313fd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="313fd-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="313fd-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="313fd-106">**ExtendedKeyUsage** 方法會傳回 [**ExtendedKeyUsage**](extendedkeyusage.md)物件，此物件會指出憑證的有效用法。</span><span class="sxs-lookup"><span data-stu-id="313fd-106">The **ExtendedKeyUsage** method returns an [**ExtendedKeyUsage**](extendedkeyusage.md) object that indicates the valid uses of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="313fd-107">語法</span><span class="sxs-lookup"><span data-stu-id="313fd-107">Syntax</span></span>


```VB
Certificate.ExtendedKeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="313fd-108">參數</span><span class="sxs-lookup"><span data-stu-id="313fd-108">Parameters</span></span>

<span data-ttu-id="313fd-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="313fd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="313fd-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="313fd-110">Return value</span></span>

<span data-ttu-id="313fd-111">與憑證相關聯的 [**ExtendedKeyUsage**](extendedkeyusage.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="313fd-111">The [**ExtendedKeyUsage**](extendedkeyusage.md) object that is associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="313fd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="313fd-112">Requirements</span></span>



| <span data-ttu-id="313fd-113">需求</span><span class="sxs-lookup"><span data-stu-id="313fd-113">Requirement</span></span> | <span data-ttu-id="313fd-114">值</span><span class="sxs-lookup"><span data-stu-id="313fd-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="313fd-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="313fd-115">End of client support</span></span><br/> | <span data-ttu-id="313fd-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="313fd-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="313fd-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="313fd-117">End of server support</span></span><br/> | <span data-ttu-id="313fd-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="313fd-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="313fd-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="313fd-119">Redistributable</span></span><br/>       | <span data-ttu-id="313fd-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="313fd-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="313fd-121">DLL</span><span class="sxs-lookup"><span data-stu-id="313fd-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="313fd-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="313fd-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="313fd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="313fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="313fd-124">加密物件</span><span class="sxs-lookup"><span data-stu-id="313fd-124">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="313fd-125">**憑證**</span><span class="sxs-lookup"><span data-stu-id="313fd-125">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
