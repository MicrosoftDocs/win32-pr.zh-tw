---
description: 收件者的 \_ NewEnum 屬性會抓取可用於列舉集合之物件上的 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。
ms.assetid: affdc695-b78c-48b5-b66d-5f94e1a86ff2
title: Recipients._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a4a1e7db31ceead23509604edddee05ec64380ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989541"
---
# <a name="recipients_newenum-property"></a><span data-ttu-id="bc88c-104">收件者。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="bc88c-104">Recipients.\_NewEnum property</span></span>

<span data-ttu-id="bc88c-105">\[**\_ NewEnum** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bc88c-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bc88c-106">相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="bc88c-106">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="bc88c-107">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="bc88c-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="bc88c-108">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="bc88c-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc88c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc88c-109">Syntax</span></span>


```VB
Recipients._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="bc88c-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bc88c-110">Property value</span></span>

<span data-ttu-id="bc88c-111">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="bc88c-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc88c-112">備註</span><span class="sxs-lookup"><span data-stu-id="bc88c-112">Remarks</span></span>

<span data-ttu-id="bc88c-113">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="bc88c-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc88c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc88c-114">Requirements</span></span>



| <span data-ttu-id="bc88c-115">需求</span><span class="sxs-lookup"><span data-stu-id="bc88c-115">Requirement</span></span> | <span data-ttu-id="bc88c-116">值</span><span class="sxs-lookup"><span data-stu-id="bc88c-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc88c-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bc88c-117">Redistributable</span></span><br/> | <span data-ttu-id="bc88c-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="bc88c-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="bc88c-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bc88c-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="bc88c-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc88c-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc88c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc88c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc88c-122">**收件者**</span><span class="sxs-lookup"><span data-stu-id="bc88c-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
