---
description: '\_憑證的 NewEnum 屬性會在可用來列舉集合的物件上，捕獲 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。'
ms.assetid: bbe6c82c-1949-4d81-bb87-3f05613efa6d
title: Certificates._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 71760f23bbb19d32c3caf8011eb87b8d03941eac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984440"
---
# <a name="certificates_newenum-property"></a><span data-ttu-id="e6910-104">憑證。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="e6910-104">Certificates.\_NewEnum property</span></span>

<span data-ttu-id="e6910-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e6910-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="e6910-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Certificate2Collection 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="e6910-106">Instead, use the [**X509Certificate2Collection Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="e6910-107">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="e6910-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="e6910-108">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="e6910-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="e6910-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6910-109">Syntax</span></span>


```VB
Certificates._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="e6910-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e6910-110">Property value</span></span>

<span data-ttu-id="e6910-111">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="e6910-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6910-112">備註</span><span class="sxs-lookup"><span data-stu-id="e6910-112">Remarks</span></span>

<span data-ttu-id="e6910-113">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="e6910-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6910-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6910-114">Requirements</span></span>



| <span data-ttu-id="e6910-115">需求</span><span class="sxs-lookup"><span data-stu-id="e6910-115">Requirement</span></span> | <span data-ttu-id="e6910-116">值</span><span class="sxs-lookup"><span data-stu-id="e6910-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6910-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e6910-117">End of client support</span></span><br/> | <span data-ttu-id="e6910-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e6910-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e6910-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e6910-119">End of server support</span></span><br/> | <span data-ttu-id="e6910-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6910-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e6910-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e6910-121">Redistributable</span></span><br/>       | <span data-ttu-id="e6910-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e6910-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e6910-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e6910-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e6910-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6910-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6910-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6910-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6910-126">**憑證**</span><span class="sxs-lookup"><span data-stu-id="e6910-126">**Certificates**</span></span>](certificates.md)
</dt> </dl>

 

 
