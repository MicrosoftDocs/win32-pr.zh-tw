---
description: PublicKey 方法會傳回憑證物件的公開金鑰物件。
ms.assetid: 9a7ea6d5-365e-4360-ab50-2bafcfaecaa0
title: PublicKey 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PublicKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 472acee68aa653cc72787a5ac5ce2c2ace4ec70f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994664"
---
# <a name="certificatepublickey-method"></a><span data-ttu-id="086e4-103">PublicKey 方法</span><span class="sxs-lookup"><span data-stu-id="086e4-103">Certificate.PublicKey method</span></span>

<span data-ttu-id="086e4-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="086e4-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="086e4-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="086e4-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="086e4-106">**PublicKey** 方法會傳回 [**憑證**](certificate.md)物件的公開金鑰物件。</span><span class="sxs-lookup"><span data-stu-id="086e4-106">The **PublicKey** method returns the public key object for a [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="086e4-107">語法</span><span class="sxs-lookup"><span data-stu-id="086e4-107">Syntax</span></span>


```VB
Certificate.PublicKey()
```



## <a name="parameters"></a><span data-ttu-id="086e4-108">參數</span><span class="sxs-lookup"><span data-stu-id="086e4-108">Parameters</span></span>

<span data-ttu-id="086e4-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="086e4-109">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="086e4-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="086e4-110">Requirements</span></span>



| <span data-ttu-id="086e4-111">需求</span><span class="sxs-lookup"><span data-stu-id="086e4-111">Requirement</span></span> | <span data-ttu-id="086e4-112">值</span><span class="sxs-lookup"><span data-stu-id="086e4-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="086e4-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="086e4-113">End of client support</span></span><br/> | <span data-ttu-id="086e4-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="086e4-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="086e4-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="086e4-115">End of server support</span></span><br/> | <span data-ttu-id="086e4-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="086e4-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="086e4-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="086e4-117">Redistributable</span></span><br/>       | <span data-ttu-id="086e4-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="086e4-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="086e4-119">DLL</span><span class="sxs-lookup"><span data-stu-id="086e4-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="086e4-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="086e4-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="086e4-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="086e4-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086e4-122">**憑證**</span><span class="sxs-lookup"><span data-stu-id="086e4-122">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
