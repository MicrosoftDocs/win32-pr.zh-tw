---
description: 屬性（attribute）的 \_ NewEnum 屬性（attribute）會在可以用來列舉集合的物件上，抓取 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。
ms.assetid: a90ef28b-3926-4542-bcd2-27f0eda4e339
title: Attributes._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9948c55943a8374665fe5e4883013742188665c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989649"
---
# <a name="attributes_newenum-property"></a><span data-ttu-id="142af-104">屬性。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="142af-104">Attributes.\_NewEnum property</span></span>

<span data-ttu-id="142af-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="142af-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="142af-106">請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="142af-106">Instead, use the [**CryptographicAttributeObjectCollection Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="142af-107">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="142af-107">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="142af-108">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="142af-108">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="142af-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="142af-109">Syntax</span></span>


```VB
Attributes._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="142af-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="142af-110">Property value</span></span>

<span data-ttu-id="142af-111">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="142af-111">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="142af-112">備註</span><span class="sxs-lookup"><span data-stu-id="142af-112">Remarks</span></span>

<span data-ttu-id="142af-113">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="142af-113">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="142af-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="142af-114">Requirements</span></span>



| <span data-ttu-id="142af-115">需求</span><span class="sxs-lookup"><span data-stu-id="142af-115">Requirement</span></span> | <span data-ttu-id="142af-116">值</span><span class="sxs-lookup"><span data-stu-id="142af-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="142af-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="142af-117">End of client support</span></span><br/> | <span data-ttu-id="142af-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="142af-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="142af-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="142af-119">End of server support</span></span><br/> | <span data-ttu-id="142af-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="142af-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="142af-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="142af-121">Redistributable</span></span><br/>       | <span data-ttu-id="142af-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="142af-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="142af-123">DLL</span><span class="sxs-lookup"><span data-stu-id="142af-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="142af-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="142af-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="142af-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="142af-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142af-126">**屬性**</span><span class="sxs-lookup"><span data-stu-id="142af-126">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 
