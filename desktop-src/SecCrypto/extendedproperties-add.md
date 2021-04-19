---
description: 將擴充屬性加入至集合。
ms.assetid: 1d6b3c39-17b0-4a7c-a5c2-4a3bd866be07
title: ExtendedProperties 新增方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06e4170b34dcdca97bc0bae6bb48b4a057a8e9b8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990068"
---
# <a name="extendedpropertiesadd-method"></a><span data-ttu-id="00c6a-103">ExtendedProperties 新增方法</span><span class="sxs-lookup"><span data-stu-id="00c6a-103">ExtendedProperties.Add method</span></span>

<span data-ttu-id="00c6a-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="00c6a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="00c6a-105">相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。</span><span class="sxs-lookup"><span data-stu-id="00c6a-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API function [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) and obtain the properties.</span></span> <span data-ttu-id="00c6a-106">如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。</span><span class="sxs-lookup"><span data-stu-id="00c6a-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="00c6a-107">[.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]</span><span class="sxs-lookup"><span data-stu-id="00c6a-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="00c6a-108">**Add** 方法會將擴充屬性加入至集合。</span><span class="sxs-lookup"><span data-stu-id="00c6a-108">The **Add** method adds an extended property to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="00c6a-109">語法</span><span class="sxs-lookup"><span data-stu-id="00c6a-109">Syntax</span></span>


```VB
ExtendedProperties.Add( _
  ByVal valProperty _
)
```



## <a name="parameters"></a><span data-ttu-id="00c6a-110">參數</span><span class="sxs-lookup"><span data-stu-id="00c6a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00c6a-111">*valProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00c6a-111">*valProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00c6a-112">代表擴充屬性的 [**ExtendedProperty**](extendedproperty.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="00c6a-112">An [**ExtendedProperty**](extendedproperty.md) object that represents the extended property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00c6a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="00c6a-113">Return value</span></span>

<span data-ttu-id="00c6a-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="00c6a-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="00c6a-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="00c6a-115">Requirements</span></span>



| <span data-ttu-id="00c6a-116">需求</span><span class="sxs-lookup"><span data-stu-id="00c6a-116">Requirement</span></span> | <span data-ttu-id="00c6a-117">值</span><span class="sxs-lookup"><span data-stu-id="00c6a-117">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="00c6a-118">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="00c6a-118">End of client support</span></span><br/> | <span data-ttu-id="00c6a-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00c6a-119">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="00c6a-120">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="00c6a-120">End of server support</span></span><br/> | <span data-ttu-id="00c6a-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00c6a-121">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="00c6a-122">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="00c6a-122">Redistributable</span></span><br/>       | <span data-ttu-id="00c6a-123">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="00c6a-123">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="00c6a-124">DLL</span><span class="sxs-lookup"><span data-stu-id="00c6a-124">DLL</span></span><br/>                   | <dl> <span data-ttu-id="00c6a-125"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00c6a-125"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
