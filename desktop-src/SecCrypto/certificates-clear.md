---
description: 從集合中移除所有的憑證物件。
ms.assetid: 7349a9dd-d17b-4f79-b31d-0d79ff7641d1
title: ICertificates2：： Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Clear
- ICertificates2.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 600d7b6e2b1c5996ffbd59a8a4a4ecc667cec3ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106988648"
---
# <a name="icertificates2clear-method"></a><span data-ttu-id="786c3-103">ICertificates2：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="786c3-103">ICertificates2::Clear method</span></span>

<span data-ttu-id="786c3-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="786c3-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="786c3-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="786c3-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="786c3-106">**Clear** 方法會從集合中移除所有的 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="786c3-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from the collection.</span></span> <span data-ttu-id="786c3-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="786c3-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="786c3-108">語法</span><span class="sxs-lookup"><span data-stu-id="786c3-108">Syntax</span></span>


```VB
Certificates.Clear()
```



## <a name="parameters"></a><span data-ttu-id="786c3-109">參數</span><span class="sxs-lookup"><span data-stu-id="786c3-109">Parameters</span></span>

<span data-ttu-id="786c3-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="786c3-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="786c3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="786c3-111">Return value</span></span>

<span data-ttu-id="786c3-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="786c3-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="786c3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="786c3-113">Requirements</span></span>



| <span data-ttu-id="786c3-114">需求</span><span class="sxs-lookup"><span data-stu-id="786c3-114">Requirement</span></span> | <span data-ttu-id="786c3-115">值</span><span class="sxs-lookup"><span data-stu-id="786c3-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="786c3-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="786c3-116">End of client support</span></span><br/> | <span data-ttu-id="786c3-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="786c3-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="786c3-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="786c3-118">End of server support</span></span><br/> | <span data-ttu-id="786c3-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="786c3-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="786c3-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="786c3-120">Redistributable</span></span><br/>       | <span data-ttu-id="786c3-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="786c3-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="786c3-122">DLL</span><span class="sxs-lookup"><span data-stu-id="786c3-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="786c3-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="786c3-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
