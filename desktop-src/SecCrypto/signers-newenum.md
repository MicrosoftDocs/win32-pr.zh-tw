---
description: 簽署者的 \_ NewEnum 屬性會抓取可用於列舉集合之物件上的 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。
ms.assetid: 99d7ddd3-a552-4125-b220-d1b28f20d1ed
title: Signers._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 91007e7ce282cb44267927f54ab26f8f930028f0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976202"
---
# <a name="signers_newenum-property"></a><span data-ttu-id="3e08e-104">簽署者。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="3e08e-104">Signers.\_NewEnum property</span></span>

<span data-ttu-id="3e08e-105">\[**\_ NewEnum** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="3e08e-105">\[The **\_NewEnum** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3e08e-106">相反地，請使用 CmsSigner 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="3e08e-106">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="3e08e-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span><span class="sxs-lookup"><span data-stu-id="3e08e-107">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="3e08e-108">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="3e08e-108">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="3e08e-109">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="3e08e-109">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e08e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e08e-110">Syntax</span></span>


```VB
Signers._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="3e08e-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="3e08e-111">Property value</span></span>

<span data-ttu-id="3e08e-112">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="3e08e-112">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e08e-113">備註</span><span class="sxs-lookup"><span data-stu-id="3e08e-113">Remarks</span></span>

<span data-ttu-id="3e08e-114">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="3e08e-114">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e08e-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e08e-115">Requirements</span></span>



| <span data-ttu-id="3e08e-116">需求</span><span class="sxs-lookup"><span data-stu-id="3e08e-116">Requirement</span></span> | <span data-ttu-id="3e08e-117">值</span><span class="sxs-lookup"><span data-stu-id="3e08e-117">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e08e-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="3e08e-118">Redistributable</span></span><br/> | <span data-ttu-id="3e08e-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="3e08e-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3e08e-120">DLL</span><span class="sxs-lookup"><span data-stu-id="3e08e-120">DLL</span></span><br/>             | <dl> <span data-ttu-id="3e08e-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e08e-121"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e08e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e08e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e08e-123">**簽名**</span><span class="sxs-lookup"><span data-stu-id="3e08e-123">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
