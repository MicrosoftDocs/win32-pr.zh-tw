---
description: 設定或抓取與憑證相關聯的私密金鑰。
ms.assetid: 976d81b4-5cbe-4824-9087-9a908b0e60e5
title: Certificate. PrivateKey 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.PrivateKey
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: eed2297a4546250cfe9e360029f11b2e4e6e67d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981673"
---
# <a name="certificateprivatekey-property"></a><span data-ttu-id="2f316-103">Certificate. PrivateKey 屬性</span><span class="sxs-lookup"><span data-stu-id="2f316-103">Certificate.PrivateKey property</span></span>

<span data-ttu-id="2f316-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2f316-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2f316-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2 類別**](/previous-versions/windows/embedded/hh424017(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="2f316-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2f316-106">**PrivateKey** 屬性會設定或抓取與憑證相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f316-106">The **PrivateKey** property sets or retrieves the private key associated with the certificate.</span></span> <span data-ttu-id="2f316-107">這個屬性是在 CAPICOM 2.0 中引進。</span><span class="sxs-lookup"><span data-stu-id="2f316-107">This property was introduced in CAPICOM 2.0.</span></span>

<span data-ttu-id="2f316-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="2f316-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f316-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="2f316-109">Syntax</span></span>


```VB
Certificate.PrivateKey As PrivateKey
```



## <a name="property-value"></a><span data-ttu-id="2f316-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="2f316-110">Property value</span></span>

<span data-ttu-id="2f316-111">[**PrivateKey**](privatekey.md)物件，代表與憑證相關聯的私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f316-111">A [**PrivateKey**](privatekey.md) object that represents the private key that is associated with the certificate.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f316-112">備註</span><span class="sxs-lookup"><span data-stu-id="2f316-112">Remarks</span></span>

<span data-ttu-id="2f316-113">將 **PrivateKey** 屬性設定為 Nothing 時，不會移除私密金鑰與憑證之間的關聯，但不會刪除私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="2f316-113">Setting the **PrivateKey** property to Nothing removes the association between the private key and the certificate, but it does not delete the private key.</span></span> <span data-ttu-id="2f316-114">若要刪除私密金鑰，請呼叫 [**PrivateKey**](privatekey-delete.md) 方法，然後將此屬性設定為 Nothing。</span><span class="sxs-lookup"><span data-stu-id="2f316-114">To delete the private key, call the [**PrivateKey.Delete**](privatekey-delete.md) method, and then set this property to Nothing.</span></span>

<span data-ttu-id="2f316-115">\_ \_ \_ 從 web 應用程式設定時，此屬性會引發 CAPICOM E （不允許）。</span><span class="sxs-lookup"><span data-stu-id="2f316-115">This property raises CAPICOM\_E\_NOT\_ALLOWED when it is set from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f316-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f316-116">Requirements</span></span>



| <span data-ttu-id="2f316-117">需求</span><span class="sxs-lookup"><span data-stu-id="2f316-117">Requirement</span></span> | <span data-ttu-id="2f316-118">值</span><span class="sxs-lookup"><span data-stu-id="2f316-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f316-119">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2f316-119">End of client support</span></span><br/> | <span data-ttu-id="2f316-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f316-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2f316-121">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2f316-121">End of server support</span></span><br/> | <span data-ttu-id="2f316-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f316-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2f316-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2f316-123">Redistributable</span></span><br/>       | <span data-ttu-id="2f316-124">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2f316-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2f316-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2f316-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2f316-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f316-126"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f316-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f316-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f316-128">**憑證**</span><span class="sxs-lookup"><span data-stu-id="2f316-128">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
