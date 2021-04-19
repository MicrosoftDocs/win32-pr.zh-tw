---
description: Result 屬性會抓取指出憑證是否有效的值。 這是預設屬性。
ms.assetid: b1edfbde-9d54-4e9c-ba9b-33e4c354c23f
title: CertificateStatus 結果屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.Result
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: df13e9a9fb0454d30ce855b3d272fa521e96e0f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000370"
---
# <a name="certificatestatusresult-property"></a><span data-ttu-id="a4e38-104">CertificateStatus 結果屬性</span><span class="sxs-lookup"><span data-stu-id="a4e38-104">CertificateStatus.Result property</span></span>

<span data-ttu-id="a4e38-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="a4e38-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a4e38-106">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509ChainStatus 結構**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="a4e38-106">Instead, use the [**X509ChainStatus Structure**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a4e38-107">**Result** 屬性會抓取指出憑證是否有效的值。</span><span class="sxs-lookup"><span data-stu-id="a4e38-107">The **Result** property retrieves a value that indicates whether the certificate is valid.</span></span> <span data-ttu-id="a4e38-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="a4e38-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e38-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4e38-109">Syntax</span></span>


```VB
CertificateStatus.Result As Boolean
```



## <a name="property-value"></a><span data-ttu-id="a4e38-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="a4e38-110">Property value</span></span>

<span data-ttu-id="a4e38-111">若 **為 true**，則表示憑證有效。</span><span class="sxs-lookup"><span data-stu-id="a4e38-111">If **true**, the certificate is valid.</span></span> <span data-ttu-id="a4e38-112">使用 [**CheckFlag**](certificatestatus-checkflag.md) 屬性的目前設定和各種原則設定，檢查憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="a4e38-112">The certificate's validity is checked using the current setting of the [**CheckFlag**](certificatestatus-checkflag.md) property and the various policy settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e38-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4e38-113">Requirements</span></span>



| <span data-ttu-id="a4e38-114">需求</span><span class="sxs-lookup"><span data-stu-id="a4e38-114">Requirement</span></span> | <span data-ttu-id="a4e38-115">值</span><span class="sxs-lookup"><span data-stu-id="a4e38-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e38-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a4e38-116">End of client support</span></span><br/> | <span data-ttu-id="a4e38-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a4e38-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a4e38-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="a4e38-118">End of server support</span></span><br/> | <span data-ttu-id="a4e38-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a4e38-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a4e38-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a4e38-120">Redistributable</span></span><br/>       | <span data-ttu-id="a4e38-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="a4e38-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a4e38-122">DLL</span><span class="sxs-lookup"><span data-stu-id="a4e38-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a4e38-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e38-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
