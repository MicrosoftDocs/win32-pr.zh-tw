---
description: Item 屬性會從集合中抓取 ExtendedProperty 物件。 這是預設屬性。
ms.assetid: add819e1-6330-483a-8a76-3b7fb8d3f110
title: ExtendedProperties 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 200e36f232c97c1b5a86c8a8a975783469d64a71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999246"
---
# <a name="extendedpropertiesitem-property"></a><span data-ttu-id="2494f-104">ExtendedProperties 專案屬性</span><span class="sxs-lookup"><span data-stu-id="2494f-104">ExtendedProperties.Item property</span></span>

<span data-ttu-id="2494f-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="2494f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="2494f-106">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="2494f-106">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="2494f-107">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="2494f-107">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="2494f-108">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="2494f-108">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="2494f-109">**Item** 屬性會從集合中抓取 [**ExtendedProperty**](extendedproperty.md)物件。</span><span class="sxs-lookup"><span data-stu-id="2494f-109">The **Item** property retrieves an [**ExtendedProperty**](extendedproperty.md) object from the collection.</span></span> <span data-ttu-id="2494f-110">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="2494f-110">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="2494f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2494f-111">Syntax</span></span>


```VB
ExtendedProperties.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="2494f-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="2494f-112">Property value</span></span>

<span data-ttu-id="2494f-113">[**ExtendedProperty**](extendedproperty.md)物件，表示集合的索引延伸屬性。</span><span class="sxs-lookup"><span data-stu-id="2494f-113">An [**ExtendedProperty**](extendedproperty.md) object that represents the indexed extended property of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="2494f-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="2494f-114">Requirements</span></span>



| <span data-ttu-id="2494f-115">需求</span><span class="sxs-lookup"><span data-stu-id="2494f-115">Requirement</span></span> | <span data-ttu-id="2494f-116">值</span><span class="sxs-lookup"><span data-stu-id="2494f-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2494f-117">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="2494f-117">End of client support</span></span><br/> | <span data-ttu-id="2494f-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2494f-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2494f-119">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="2494f-119">End of server support</span></span><br/> | <span data-ttu-id="2494f-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2494f-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2494f-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2494f-121">Redistributable</span></span><br/>       | <span data-ttu-id="2494f-122">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2494f-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2494f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="2494f-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="2494f-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2494f-124"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
