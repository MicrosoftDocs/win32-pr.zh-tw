---
description: 抓取包含憑證序號的字串。
ms.assetid: d08be744-4ae8-49f9-8b00-48e76c296f2b
title: Certificate. SerialNumber 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.SerialNumber
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6dbd9485891cc89e686cef118e12dd43ec400f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994041"
---
# <a name="certificateserialnumber-property"></a><span data-ttu-id="ec455-103">Certificate. SerialNumber 屬性</span><span class="sxs-lookup"><span data-stu-id="ec455-103">Certificate.SerialNumber property</span></span>

<span data-ttu-id="ec455-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="ec455-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="ec455-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="ec455-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="ec455-106">**SerialNumber** 屬性會捕獲包含憑證序號的字串。</span><span class="sxs-lookup"><span data-stu-id="ec455-106">The **SerialNumber** property retrieves a string that contains the certificate serial number.</span></span>

<span data-ttu-id="ec455-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ec455-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec455-108">語法</span><span class="sxs-lookup"><span data-stu-id="ec455-108">Syntax</span></span>


```VB
Certificate.SerialNumber As String
```



## <a name="property-value"></a><span data-ttu-id="ec455-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="ec455-109">Property value</span></span>

<span data-ttu-id="ec455-110">包含憑證序號的字串。</span><span class="sxs-lookup"><span data-stu-id="ec455-110">A string that contains the certificate serial number.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec455-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec455-111">Requirements</span></span>



| <span data-ttu-id="ec455-112">需求</span><span class="sxs-lookup"><span data-stu-id="ec455-112">Requirement</span></span> | <span data-ttu-id="ec455-113">值</span><span class="sxs-lookup"><span data-stu-id="ec455-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec455-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ec455-114">End of client support</span></span><br/> | <span data-ttu-id="ec455-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec455-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ec455-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="ec455-116">End of server support</span></span><br/> | <span data-ttu-id="ec455-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec455-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ec455-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ec455-118">Redistributable</span></span><br/>       | <span data-ttu-id="ec455-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ec455-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ec455-120">DLL</span><span class="sxs-lookup"><span data-stu-id="ec455-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="ec455-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec455-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
