---
description: 傳回 KeyUsage 物件，這個物件表示憑證的有效金鑰使用方式。
ms.assetid: e4590e95-ffa2-4953-bfc1-4d7c70271029
title: ICertificate2：： KeyUsage 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.KeyUsage
- ICertificate2.KeyUsage
- ICertificate.KeyUsage
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85fe008880d9613586d38dba7afaca39bb29f72f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991013"
---
# <a name="icertificate2keyusage-method"></a><span data-ttu-id="ee8d0-103">ICertificate2：： KeyUsage 方法</span><span class="sxs-lookup"><span data-stu-id="ee8d0-103">ICertificate2::KeyUsage method</span></span>

<span data-ttu-id="ee8d0-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ee8d0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ee8d0-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="ee8d0-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ee8d0-106">**KeyUsage** 方法會傳回 [**KeyUsage**](keyusage.md)物件，指出憑證的有效金鑰使用方式。</span><span class="sxs-lookup"><span data-stu-id="ee8d0-106">The **KeyUsage** method returns a [**KeyUsage**](keyusage.md) object that indicates the valid key usage of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8d0-107">語法</span><span class="sxs-lookup"><span data-stu-id="ee8d0-107">Syntax</span></span>


```VB
Certificate.KeyUsage()
```



## <a name="parameters"></a><span data-ttu-id="ee8d0-108">參數</span><span class="sxs-lookup"><span data-stu-id="ee8d0-108">Parameters</span></span>

<span data-ttu-id="ee8d0-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ee8d0-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8d0-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="ee8d0-110">Requirements</span></span>



| <span data-ttu-id="ee8d0-111">需求</span><span class="sxs-lookup"><span data-stu-id="ee8d0-111">Requirement</span></span> | <span data-ttu-id="ee8d0-112">值</span><span class="sxs-lookup"><span data-stu-id="ee8d0-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8d0-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ee8d0-113">End of client support</span></span><br/> | <span data-ttu-id="ee8d0-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee8d0-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ee8d0-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ee8d0-115">End of server support</span></span><br/> | <span data-ttu-id="ee8d0-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee8d0-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ee8d0-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ee8d0-117">Redistributable</span></span><br/>       | <span data-ttu-id="ee8d0-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ee8d0-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ee8d0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ee8d0-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ee8d0-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee8d0-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8d0-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ee8d0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8d0-122">加密物件</span><span class="sxs-lookup"><span data-stu-id="ee8d0-122">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ee8d0-123">**憑證**</span><span class="sxs-lookup"><span data-stu-id="ee8d0-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
