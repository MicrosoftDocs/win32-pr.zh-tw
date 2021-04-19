---
description: 傳回 BasicConstraints 物件，這個物件表示憑證的基本條件約束延伸。
ms.assetid: cc4e566a-5f68-4e28-9397-39f22a71e45b
title: ICertificate2：： BasicConstraints 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.BasicConstraints
- ICertificate2.BasicConstraints
- ICertificate.BasicConstraints
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b511781c29d313715e7714f185dbff7e4b38f86c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001025"
---
# <a name="icertificate2basicconstraints-method"></a><span data-ttu-id="d725e-103">ICertificate2：： BasicConstraints 方法</span><span class="sxs-lookup"><span data-stu-id="d725e-103">ICertificate2::BasicConstraints method</span></span>

<span data-ttu-id="d725e-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d725e-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="d725e-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="d725e-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="d725e-106">**BasicConstraints** 方法會傳回 [**BasicConstraints**](basicconstraints.md)物件，此物件代表憑證的基本條件約束延伸。</span><span class="sxs-lookup"><span data-stu-id="d725e-106">The **BasicConstraints** method returns a [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d725e-107">語法</span><span class="sxs-lookup"><span data-stu-id="d725e-107">Syntax</span></span>


```VB
Certificate.BasicConstraints()
```



## <a name="parameters"></a><span data-ttu-id="d725e-108">參數</span><span class="sxs-lookup"><span data-stu-id="d725e-108">Parameters</span></span>

<span data-ttu-id="d725e-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d725e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d725e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d725e-110">Return value</span></span>

<span data-ttu-id="d725e-111">[**BasicConstraints**](basicconstraints.md)物件，表示憑證的基本條件約束延伸。</span><span class="sxs-lookup"><span data-stu-id="d725e-111">The [**BasicConstraints**](basicconstraints.md) object that represents the basic constraints extension of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="d725e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d725e-112">Requirements</span></span>



| <span data-ttu-id="d725e-113">需求</span><span class="sxs-lookup"><span data-stu-id="d725e-113">Requirement</span></span> | <span data-ttu-id="d725e-114">值</span><span class="sxs-lookup"><span data-stu-id="d725e-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d725e-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d725e-115">End of client support</span></span><br/> | <span data-ttu-id="d725e-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d725e-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d725e-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d725e-117">End of server support</span></span><br/> | <span data-ttu-id="d725e-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d725e-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d725e-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d725e-119">Redistributable</span></span><br/>       | <span data-ttu-id="d725e-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d725e-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d725e-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d725e-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d725e-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d725e-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
