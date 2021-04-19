---
description: 從集合中移除單一憑證物件。
ms.assetid: dff82825-1a7d-4c1a-94e2-7f9d1281ecf2
title: ICertificates2：： Remove 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Remove
- ICertificates2.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6a2f9336a420f1d014e178f67cae02cf85f0fd44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976216"
---
# <a name="icertificates2remove-method"></a><span data-ttu-id="682a7-103">ICertificates2：： Remove 方法</span><span class="sxs-lookup"><span data-stu-id="682a7-103">ICertificates2::Remove method</span></span>

<span data-ttu-id="682a7-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="682a7-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="682a7-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/previous-versions/windows/embedded/hh424013(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="682a7-105">Instead, use the [**X509Certificate2Collection Class**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="682a7-106">**Remove** 方法會從集合中移除單一 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="682a7-106">The **Remove** method removes a single [**Certificate**](certificate.md) object from the collection.</span></span> <span data-ttu-id="682a7-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="682a7-107">This method was introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="682a7-108">語法</span><span class="sxs-lookup"><span data-stu-id="682a7-108">Syntax</span></span>


```VB
Certificates.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="682a7-109">參數</span><span class="sxs-lookup"><span data-stu-id="682a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="682a7-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="682a7-110">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="682a7-111">要移除之 [**憑證**](certificate.md) 物件的索引值。</span><span class="sxs-lookup"><span data-stu-id="682a7-111">Index value for the [**Certificate**](certificate.md) object to be removed.</span></span> <span data-ttu-id="682a7-112">這個參數可以是下列其中一種可能的類型。</span><span class="sxs-lookup"><span data-stu-id="682a7-112">This parameter can be one of the following possible types.</span></span>



| <span data-ttu-id="682a7-113">類型</span><span class="sxs-lookup"><span data-stu-id="682a7-113">Type</span></span>                                                                                                                                                                                                                                                              | <span data-ttu-id="682a7-114">意義</span><span class="sxs-lookup"><span data-stu-id="682a7-114">Meaning</span></span>                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Long"></span><span id="long"></span><span id="LONG"></span><dl> <span data-ttu-id="682a7-115"><dt>\* \* \* \* 長 \*</dt> \* \* <dt></dt></span><span class="sxs-lookup"><span data-stu-id="682a7-115"><dt>\*\*\*\*Long\*\*\*\*</dt> <dt></dt></span></span> </dl>                                                | <span data-ttu-id="682a7-116">已移除集合中指定索引處的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="682a7-116">The [**Certificate**](certificate.md) object at the specified index into the collection is removed.</span></span><br/>                                                                                                          |
| <span id="String"></span><span id="string"></span><span id="STRING"></span><dl> <span data-ttu-id="682a7-117"><dt>\* \* \* \* 字串 \* \*</dt> \* \* <dt></dt></span><span class="sxs-lookup"><span data-stu-id="682a7-117"><dt>\*\*\*\*String\*\*\*\*</dt> <dt></dt></span></span> </dl>                                        | <span data-ttu-id="682a7-118">集合中的第一個符合指定字串之 [*sha-1*](../secgloss/s-gly.md)指紋的 [**憑證**](certificate.md)物件會被移除。</span><span class="sxs-lookup"><span data-stu-id="682a7-118">The first [**Certificate**](certificate.md) object in the collection that matches the [*SHA-1*](../secgloss/s-gly.md) thumbprint contained in the specified string is removed.</span></span><br/> |
| <span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span><dl> <span data-ttu-id="682a7-119"><dt>**[**憑證**](certificate.md)**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="682a7-119"><dt>**[**Certificate**](certificate.md)**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="682a7-120">集合中符合指定 **憑證** 物件的第一個 [**憑證**](certificate.md)物件會被移除。</span><span class="sxs-lookup"><span data-stu-id="682a7-120">The first [**Certificate**](certificate.md) object in the collection that matches the specified **Certificate** object is removed.</span></span><br/>                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="682a7-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="682a7-121">Return value</span></span>

<span data-ttu-id="682a7-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="682a7-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="682a7-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="682a7-123">Requirements</span></span>



| <span data-ttu-id="682a7-124">需求</span><span class="sxs-lookup"><span data-stu-id="682a7-124">Requirement</span></span> | <span data-ttu-id="682a7-125">值</span><span class="sxs-lookup"><span data-stu-id="682a7-125">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="682a7-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="682a7-126">End of client support</span></span><br/> | <span data-ttu-id="682a7-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="682a7-127">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="682a7-128">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="682a7-128">End of server support</span></span><br/> | <span data-ttu-id="682a7-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="682a7-129">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="682a7-130">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="682a7-130">Redistributable</span></span><br/>       | <span data-ttu-id="682a7-131">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="682a7-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="682a7-132">DLL</span><span class="sxs-lookup"><span data-stu-id="682a7-132">DLL</span></span><br/>                   | <dl> <span data-ttu-id="682a7-133"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="682a7-133"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
