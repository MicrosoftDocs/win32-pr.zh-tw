---
description: 傳回與憑證相關聯的延伸模組集合。
ms.assetid: 07793061-6f94-4467-bb01-aa65db657658
title: ICertificate2：： Extension 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Extensions
- ICertificate2.Extensions
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cc96dee9c33bb3f76e1fb17acb2000f9740d1b5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976133"
---
# <a name="icertificate2extensions-method"></a><span data-ttu-id="4b551-103">ICertificate2：： Extension 方法</span><span class="sxs-lookup"><span data-stu-id="4b551-103">ICertificate2::Extensions method</span></span>

<span data-ttu-id="4b551-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="4b551-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="4b551-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="4b551-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4b551-106">**擴充** 方法會傳回與憑證相關聯的延伸模組集合。</span><span class="sxs-lookup"><span data-stu-id="4b551-106">The **Extensions** method returns a collection of the extensions associated with the certificate.</span></span> <span data-ttu-id="4b551-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="4b551-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b551-108">語法</span><span class="sxs-lookup"><span data-stu-id="4b551-108">Syntax</span></span>


```VB
Certificate.Extensions()
```



## <a name="parameters"></a><span data-ttu-id="4b551-109">參數</span><span class="sxs-lookup"><span data-stu-id="4b551-109">Parameters</span></span>

<span data-ttu-id="4b551-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="4b551-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4b551-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4b551-111">Return value</span></span>

<span data-ttu-id="4b551-112">[**擴充**](extensions.md)物件，代表與憑證相關聯的所有延伸模組。</span><span class="sxs-lookup"><span data-stu-id="4b551-112">An [**Extensions**](extensions.md) object that represents all of the extensions associated with the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b551-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b551-113">Requirements</span></span>



| <span data-ttu-id="4b551-114">需求</span><span class="sxs-lookup"><span data-stu-id="4b551-114">Requirement</span></span> | <span data-ttu-id="4b551-115">值</span><span class="sxs-lookup"><span data-stu-id="4b551-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b551-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4b551-116">End of client support</span></span><br/> | <span data-ttu-id="4b551-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4b551-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4b551-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4b551-118">End of server support</span></span><br/> | <span data-ttu-id="4b551-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4b551-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4b551-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4b551-120">Redistributable</span></span><br/>       | <span data-ttu-id="4b551-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4b551-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4b551-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4b551-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4b551-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b551-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
