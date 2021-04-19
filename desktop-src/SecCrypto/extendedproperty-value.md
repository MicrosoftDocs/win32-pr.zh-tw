---
description: 設定或抓取擴充的屬性資料。
ms.assetid: 115bb52a-e64d-4d84-a491-35f6dba25a58
title: ExtendedProperty。 Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperty.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ebbd977a107d92661110ceff02f3a5bb0bea191e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999321"
---
# <a name="extendedpropertyvalue-property"></a><span data-ttu-id="f0f00-103">ExtendedProperty。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="f0f00-103">ExtendedProperty.Value property</span></span>

<span data-ttu-id="f0f00-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f0f00-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f0f00-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="f0f00-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="f0f00-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="f0f00-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f0f00-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="f0f00-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f0f00-108">**Value** 屬性會設定或抓取擴充的屬性資料。</span><span class="sxs-lookup"><span data-stu-id="f0f00-108">The **Value** property sets or retrieves the extended property data.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0f00-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0f00-109">Syntax</span></span>


```VB
ExtendedProperty.Value( _
  [ ByVal EncodingType ] _
) As String
```



## <a name="property-value"></a><span data-ttu-id="f0f00-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="f0f00-110">Property value</span></span>

<span data-ttu-id="f0f00-111">擴充屬性資料，格式為 *edi.encodingtype* 所指定的格式。</span><span class="sxs-lookup"><span data-stu-id="f0f00-111">The extended property data, in the format specified by *EncodingType*.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f00-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0f00-112">Requirements</span></span>



| <span data-ttu-id="f0f00-113">需求</span><span class="sxs-lookup"><span data-stu-id="f0f00-113">Requirement</span></span> | <span data-ttu-id="f0f00-114">值</span><span class="sxs-lookup"><span data-stu-id="f0f00-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0f00-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f0f00-115">End of client support</span></span><br/> | <span data-ttu-id="f0f00-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0f00-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f0f00-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f0f00-117">End of server support</span></span><br/> | <span data-ttu-id="f0f00-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0f00-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f0f00-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f0f00-119">Redistributable</span></span><br/>       | <span data-ttu-id="f0f00-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f0f00-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f0f00-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f0f00-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f0f00-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0f00-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
