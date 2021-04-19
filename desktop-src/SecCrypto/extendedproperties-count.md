---
description: 抓取集合中的 ExtendedProperty 物件數目。
ms.assetid: 50bc8485-7285-4704-80db-c2e0d68e8cb0
title: ExtendedProperties Count 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d4370f7ce5fc215d18b0940d3dbc2edc221af536
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983061"
---
# <a name="extendedpropertiescount-property"></a><span data-ttu-id="f8874-103">ExtendedProperties Count 屬性</span><span class="sxs-lookup"><span data-stu-id="f8874-103">ExtendedProperties.Count property</span></span>

<span data-ttu-id="f8874-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="f8874-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="f8874-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="f8874-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="f8874-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="f8874-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="f8874-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="f8874-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="f8874-108">**Count** 屬性會抓取集合中的 [**ExtendedProperty**](extendedproperty.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="f8874-108">The **Count** property retrieves the number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8874-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8874-109">Syntax</span></span>


```VB
ExtendedProperties.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="f8874-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="f8874-110">Property value</span></span>

<span data-ttu-id="f8874-111">集合中的 [**ExtendedProperty**](extendedproperty.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="f8874-111">The number of [**ExtendedProperty**](extendedproperty.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8874-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8874-112">Requirements</span></span>



| <span data-ttu-id="f8874-113">需求</span><span class="sxs-lookup"><span data-stu-id="f8874-113">Requirement</span></span> | <span data-ttu-id="f8874-114">值</span><span class="sxs-lookup"><span data-stu-id="f8874-114">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8874-115">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f8874-115">End of client support</span></span><br/> | <span data-ttu-id="f8874-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f8874-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f8874-117">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="f8874-117">End of server support</span></span><br/> | <span data-ttu-id="f8874-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f8874-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f8874-119">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f8874-119">Redistributable</span></span><br/>       | <span data-ttu-id="f8874-120">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f8874-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f8874-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f8874-121">DLL</span></span><br/>                   | <dl> <span data-ttu-id="f8874-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f8874-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
