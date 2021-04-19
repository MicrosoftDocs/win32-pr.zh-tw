---
description: 傳回與憑證相關聯的範本。
ms.assetid: 84fbf984-b932-4794-a939-de01e529d891
title: ICertificate2：： Template 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Template
- ICertificate2.Template
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f4b2666f4006cd2a583809725749d16daf8e6e6a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991537"
---
# <a name="icertificate2template-method"></a><span data-ttu-id="f7f9b-103">ICertificate2：： Template 方法</span><span class="sxs-lookup"><span data-stu-id="f7f9b-103">ICertificate2::Template method</span></span>

<span data-ttu-id="f7f9b-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f7f9b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f7f9b-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="f7f9b-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f7f9b-106">**範本** 方法會傳回與憑證相關聯的範本。</span><span class="sxs-lookup"><span data-stu-id="f7f9b-106">The **Template** method returns the template that is associated with the certificate.</span></span> <span data-ttu-id="f7f9b-107">此方法是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="f7f9b-107">This method is introduced in CAPICOM 2.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7f9b-108">語法</span><span class="sxs-lookup"><span data-stu-id="f7f9b-108">Syntax</span></span>


```VB
Certificate.Template()
```



## <a name="parameters"></a><span data-ttu-id="f7f9b-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7f9b-109">Parameters</span></span>

<span data-ttu-id="f7f9b-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="f7f9b-110">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7f9b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7f9b-111">Requirements</span></span>



| <span data-ttu-id="f7f9b-112">需求</span><span class="sxs-lookup"><span data-stu-id="f7f9b-112">Requirement</span></span> | <span data-ttu-id="f7f9b-113">值</span><span class="sxs-lookup"><span data-stu-id="f7f9b-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7f9b-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f7f9b-114">End of client support</span></span><br/> | <span data-ttu-id="f7f9b-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f7f9b-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f7f9b-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f7f9b-116">End of server support</span></span><br/> | <span data-ttu-id="f7f9b-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f7f9b-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f7f9b-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f7f9b-118">Redistributable</span></span><br/>       | <span data-ttu-id="f7f9b-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f7f9b-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f7f9b-120">DLL</span><span class="sxs-lookup"><span data-stu-id="f7f9b-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f7f9b-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7f9b-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
