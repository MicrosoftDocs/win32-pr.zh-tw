---
description: '\_ExtendedProperties 的 NewEnum 屬性會抓取可以用來列舉集合之物件上的 IEnumVARIANT 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。'
ms.assetid: 2692f607-3bec-4674-9d8d-3c872d523ace
title: ExtendedProperties._NewEnum 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties._NewEnum
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 62f07fe7a1a193f93fc0d3bf4c04fbfc5d76ecf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994730"
---
# <a name="extendedproperties_newenum-property"></a><span data-ttu-id="89bda-104">ExtendedProperties。 \_NewEnum 屬性</span><span class="sxs-lookup"><span data-stu-id="89bda-104">ExtendedProperties.\_NewEnum property</span></span>

<span data-ttu-id="89bda-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="89bda-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="89bda-106">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="89bda-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="89bda-107">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="89bda-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="89bda-108">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="89bda-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="89bda-109">**\_ NewEnum** 屬性會抓取可用於列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)介面。</span><span class="sxs-lookup"><span data-stu-id="89bda-109">The **\_NewEnum** property retrieves an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span> <span data-ttu-id="89bda-110">這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。</span><span class="sxs-lookup"><span data-stu-id="89bda-110">This property is hidden within Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="syntax"></a><span data-ttu-id="89bda-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="89bda-111">Syntax</span></span>


```VB
ExtendedProperties._NewEnum As IUnknown
```



## <a name="property-value"></a><span data-ttu-id="89bda-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="89bda-112">Property value</span></span>

<span data-ttu-id="89bda-113">可以用來列舉集合之物件上的 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。</span><span class="sxs-lookup"><span data-stu-id="89bda-113">An [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface on an object that can be used to enumerate the collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="89bda-114">備註</span><span class="sxs-lookup"><span data-stu-id="89bda-114">Remarks</span></span>

<span data-ttu-id="89bda-115">當您使用 Visual Basic Scripting Edition 中的結構時，會自動在內部使用此屬性 `For Each In` (VBScript) 。</span><span class="sxs-lookup"><span data-stu-id="89bda-115">This property is automatically used internally when you use the `For Each In` construct in Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="requirements"></a><span data-ttu-id="89bda-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="89bda-116">Requirements</span></span>



| <span data-ttu-id="89bda-117">需求</span><span class="sxs-lookup"><span data-stu-id="89bda-117">Requirement</span></span> | <span data-ttu-id="89bda-118">值</span><span class="sxs-lookup"><span data-stu-id="89bda-118">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89bda-119">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="89bda-119">End of client support</span></span><br/> | <span data-ttu-id="89bda-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89bda-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="89bda-121">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="89bda-121">End of server support</span></span><br/> | <span data-ttu-id="89bda-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89bda-122">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="89bda-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="89bda-123">Redistributable</span></span><br/>       | <span data-ttu-id="89bda-124">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="89bda-124">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="89bda-125">DLL</span><span class="sxs-lookup"><span data-stu-id="89bda-125">DLL</span></span><br/>                   | <dl> <span data-ttu-id="89bda-126"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89bda-126"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
