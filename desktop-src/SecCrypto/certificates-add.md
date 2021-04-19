---
description: 將憑證物件加入至集合。
ms.assetid: 0973018d-1e83-41b4-a250-7dd5be2fb664
title: ICertificates2：： Add 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Add
- ICertificates2.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d56120c6f584e828c3aadca037d75263d5350f48
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987865"
---
# <a name="icertificates2add-method"></a><span data-ttu-id="b1a04-103">ICertificates2：： Add 方法</span><span class="sxs-lookup"><span data-stu-id="b1a04-103">ICertificates2::Add method</span></span>

<span data-ttu-id="b1a04-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="b1a04-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b1a04-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="b1a04-105">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b1a04-106">**Add** 方法會將 [**憑證**](certificate.md)物件加入至集合。</span><span class="sxs-lookup"><span data-stu-id="b1a04-106">The **Add** method adds a [**Certificate**](certificate.md) object to the collection.</span></span> <span data-ttu-id="b1a04-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="b1a04-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a04-108">語法</span><span class="sxs-lookup"><span data-stu-id="b1a04-108">Syntax</span></span>


```VB
Certificates.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="b1a04-109">參數</span><span class="sxs-lookup"><span data-stu-id="b1a04-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1a04-110">*憑證* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1a04-110">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1a04-111">要加入至集合的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="b1a04-111">The [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1a04-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1a04-112">Return value</span></span>

<span data-ttu-id="b1a04-113">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="b1a04-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a04-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1a04-114">Requirements</span></span>



| <span data-ttu-id="b1a04-115">需求</span><span class="sxs-lookup"><span data-stu-id="b1a04-115">Requirement</span></span> | <span data-ttu-id="b1a04-116">值</span><span class="sxs-lookup"><span data-stu-id="b1a04-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a04-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b1a04-117">End of client support</span></span><br/> | <span data-ttu-id="b1a04-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1a04-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="b1a04-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="b1a04-119">End of server support</span></span><br/> | <span data-ttu-id="b1a04-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1a04-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="b1a04-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b1a04-121">Redistributable</span></span><br/>       | <span data-ttu-id="b1a04-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="b1a04-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b1a04-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a04-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="b1a04-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1a04-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
