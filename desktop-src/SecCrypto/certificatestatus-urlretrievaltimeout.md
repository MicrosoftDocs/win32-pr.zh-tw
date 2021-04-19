---
description: 設定或抓取 URL 判定為無法存取之前的時間長度。
ms.assetid: f39dafc4-6017-463c-aeee-948b6173862a
title: CertificateStatus. UrlRetrievalTimeout 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.UrlRetrievalTimeout
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fcaaafa1f2e870195b612eb225696f2c23a80ee1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999316"
---
# <a name="certificatestatusurlretrievaltimeout-property"></a><span data-ttu-id="d9498-103">CertificateStatus. UrlRetrievalTimeout 屬性</span><span class="sxs-lookup"><span data-stu-id="d9498-103">CertificateStatus.UrlRetrievalTimeout property</span></span>

<span data-ttu-id="d9498-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d9498-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d9498-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="d9498-105">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d9498-106">**UrlRetrievalTimeout** 屬性會設定或抓取 URL 判定為無法存取之前的時間長度。</span><span class="sxs-lookup"><span data-stu-id="d9498-106">The **UrlRetrievalTimeout** property sets or retrieves the length of time before a URL is determined to be unreachable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9498-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9498-107">Syntax</span></span>


```VB
CertificateStatus.UrlRetrievalTimeout As Long
```



## <a name="property-value"></a><span data-ttu-id="d9498-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="d9498-108">Property value</span></span>

<span data-ttu-id="d9498-109">將 URL 判定為無法存取之前的秒數。</span><span class="sxs-lookup"><span data-stu-id="d9498-109">The number of seconds before a URL is determined to be unreachable.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9498-110">備註</span><span class="sxs-lookup"><span data-stu-id="d9498-110">Remarks</span></span>

<span data-ttu-id="d9498-111">如果未設定此屬性，預設的超時時間為15秒。</span><span class="sxs-lookup"><span data-stu-id="d9498-111">If this property is not set, the default time-out is 15 seconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9498-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9498-112">Requirements</span></span>



| <span data-ttu-id="d9498-113">需求</span><span class="sxs-lookup"><span data-stu-id="d9498-113">Requirement</span></span> | <span data-ttu-id="d9498-114">值</span><span class="sxs-lookup"><span data-stu-id="d9498-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9498-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d9498-115">End of client support</span></span><br/> | <span data-ttu-id="d9498-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9498-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d9498-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d9498-117">End of server support</span></span><br/> | <span data-ttu-id="d9498-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9498-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d9498-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d9498-119">Redistributable</span></span><br/>       | <span data-ttu-id="d9498-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d9498-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d9498-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d9498-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d9498-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9498-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
