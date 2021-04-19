---
description: 抓取包含憑證簽發者名稱的字串。
ms.assetid: 6cf528e3-061a-44dc-b320-0e4b48a6c6ab
title: Certificate. IssuerName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.IssuerName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b34b3bf198759d08fd3d0e3e4261407389a69a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992922"
---
# <a name="certificateissuername-property"></a><span data-ttu-id="9749c-103">Certificate. IssuerName 屬性</span><span class="sxs-lookup"><span data-stu-id="9749c-103">Certificate.IssuerName property</span></span>

<span data-ttu-id="9749c-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="9749c-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9749c-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="9749c-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="9749c-106">**IssuerName** 屬性會捕獲包含憑證簽發者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9749c-106">The **IssuerName** property retrieves a string that contains the name of the certificate issuer.</span></span>

<span data-ttu-id="9749c-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9749c-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="9749c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9749c-108">Syntax</span></span>


```VB
Certificate.IssuerName As String
```



## <a name="property-value"></a><span data-ttu-id="9749c-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9749c-109">Property value</span></span>

<span data-ttu-id="9749c-110">包含憑證簽發者名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="9749c-110">String that contains the name of the certificate issuer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9749c-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="9749c-111">Requirements</span></span>



| <span data-ttu-id="9749c-112">需求</span><span class="sxs-lookup"><span data-stu-id="9749c-112">Requirement</span></span> | <span data-ttu-id="9749c-113">值</span><span class="sxs-lookup"><span data-stu-id="9749c-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9749c-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9749c-114">End of client support</span></span><br/> | <span data-ttu-id="9749c-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9749c-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9749c-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9749c-116">End of server support</span></span><br/> | <span data-ttu-id="9749c-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9749c-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9749c-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9749c-118">Redistributable</span></span><br/>       | <span data-ttu-id="9749c-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9749c-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9749c-120">DLL</span><span class="sxs-lookup"><span data-stu-id="9749c-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9749c-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9749c-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
