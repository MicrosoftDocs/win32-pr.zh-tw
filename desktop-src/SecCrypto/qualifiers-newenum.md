---
description: '\_限定詞的 NewEnum 屬性會抓取可用於列舉集合之物件上的 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。'
ms.assetid: e51f8ca1-ef1f-475b-8368-e8296fae0f04
title: Qualifiers._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 01a4d62604dabacd2d78d5d2f6cbee0db7189196
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990597"
---
# <a name="qualifiers_newenum-property"></a><span data-ttu-id="7b5ca-104">限定詞。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="7b5ca-104">Qualifiers.\_NewEnum property</span></span>

<span data-ttu-id="7b5ca-105">\[**\_ NewEnum** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7b5ca-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7b5ca-106">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="7b5ca-106">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="7b5ca-107">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="7b5ca-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="7b5ca-108">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="7b5ca-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5ca-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b5ca-109">Syntax</span></span>


```VB
Qualifiers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="7b5ca-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="7b5ca-110">Property value</span></span>

<span data-ttu-id="7b5ca-111">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="7b5ca-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5ca-112">備註</span><span class="sxs-lookup"><span data-stu-id="7b5ca-112">Remarks</span></span>

<span data-ttu-id="7b5ca-113">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="7b5ca-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5ca-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7b5ca-114">Requirements</span></span>



| <span data-ttu-id="7b5ca-115">需求</span><span class="sxs-lookup"><span data-stu-id="7b5ca-115">Requirement</span></span> | <span data-ttu-id="7b5ca-116">值</span><span class="sxs-lookup"><span data-stu-id="7b5ca-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5ca-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="7b5ca-117">Redistributable</span></span><br/> | <span data-ttu-id="7b5ca-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="7b5ca-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="7b5ca-119">DLL</span><span class="sxs-lookup"><span data-stu-id="7b5ca-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="7b5ca-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b5ca-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b5ca-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7b5ca-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b5ca-122">**限定詞**</span><span class="sxs-lookup"><span data-stu-id="7b5ca-122">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
