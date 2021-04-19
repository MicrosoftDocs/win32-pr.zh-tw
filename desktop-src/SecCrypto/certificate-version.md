---
description: Version 屬性會捕獲憑證的版本號碼。
ms.assetid: 7f135a1a-ca77-4ff1-9437-532e468c6b41
title: Certificate. Version 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Version
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 48d67ac2154f63573cb8b75686b3846e14b0ed65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977712"
---
# <a name="certificateversion-property"></a><span data-ttu-id="80079-103">Certificate. Version 屬性</span><span class="sxs-lookup"><span data-stu-id="80079-103">Certificate.Version property</span></span>

<span data-ttu-id="80079-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="80079-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="80079-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="80079-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="80079-106">**Version** 屬性會捕獲憑證的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="80079-106">The **Version** property retrieves the version number of the certificate.</span></span>

<span data-ttu-id="80079-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="80079-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="80079-108">語法</span><span class="sxs-lookup"><span data-stu-id="80079-108">Syntax</span></span>


```VB
Certificate.Version As Long
```



## <a name="property-value"></a><span data-ttu-id="80079-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="80079-109">Property value</span></span>

<span data-ttu-id="80079-110">憑證的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="80079-110">The version number of the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="80079-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="80079-111">Requirements</span></span>



| <span data-ttu-id="80079-112">需求</span><span class="sxs-lookup"><span data-stu-id="80079-112">Requirement</span></span> | <span data-ttu-id="80079-113">值</span><span class="sxs-lookup"><span data-stu-id="80079-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80079-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="80079-114">End of client support</span></span><br/> | <span data-ttu-id="80079-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80079-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="80079-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="80079-116">End of server support</span></span><br/> | <span data-ttu-id="80079-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80079-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="80079-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="80079-118">Redistributable</span></span><br/>       | <span data-ttu-id="80079-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="80079-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="80079-120">DLL</span><span class="sxs-lookup"><span data-stu-id="80079-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="80079-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80079-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80079-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80079-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80079-123">**憑證**</span><span class="sxs-lookup"><span data-stu-id="80079-123">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
