---
description: '\_CertificatePolicies 的 NewEnum 屬性會抓取可以用來列舉集合之物件上的 IEnumVARIANT 介面。'
ms.assetid: 631a11c8-4442-493e-9406-bc63f79db548
title: CertificatePolicies._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificatePolicies._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2d5e90d4b906661119936ca1e893e3b6e17c9bf5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984135"
---
# <a name="certificatepolicies_newenum-property"></a><span data-ttu-id="46072-103">CertificatePolicies。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="46072-103">CertificatePolicies.\_NewEnum property</span></span>

<span data-ttu-id="46072-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="46072-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="46072-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 oid 來取得憑證原則。\]</span><span class="sxs-lookup"><span data-stu-id="46072-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to retrieve the certificate policies.\]</span></span>

<span data-ttu-id="46072-106">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="46072-106">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="46072-107">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="46072-107">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="46072-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46072-108">Syntax</span></span>


```VB
CertificatePolicies._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="46072-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="46072-109">Property value</span></span>

<span data-ttu-id="46072-110">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="46072-110">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="46072-111">備註</span><span class="sxs-lookup"><span data-stu-id="46072-111">Remarks</span></span>

<span data-ttu-id="46072-112">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="46072-112">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="46072-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="46072-113">Requirements</span></span>



| <span data-ttu-id="46072-114">需求</span><span class="sxs-lookup"><span data-stu-id="46072-114">Requirement</span></span> | <span data-ttu-id="46072-115">值</span><span class="sxs-lookup"><span data-stu-id="46072-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46072-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="46072-116">End of client support</span></span><br/> | <span data-ttu-id="46072-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46072-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="46072-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="46072-118">End of server support</span></span><br/> | <span data-ttu-id="46072-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46072-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="46072-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="46072-120">Redistributable</span></span><br/>       | <span data-ttu-id="46072-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="46072-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="46072-122">DLL</span><span class="sxs-lookup"><span data-stu-id="46072-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="46072-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46072-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
