---
description: 從收件者集合移除所有的憑證物件。
ms.assetid: 456fcfbc-4388-40f4-ab58-04508ee2141b
title: 收件者. Clear 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Clear
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 7d9bd711bbc97997045989f2eb4ffdbc51ae3559
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994008"
---
# <a name="recipientsclear-method"></a><span data-ttu-id="ba3c7-103">收件者. Clear 方法</span><span class="sxs-lookup"><span data-stu-id="ba3c7-103">Recipients.Clear method</span></span>

<span data-ttu-id="ba3c7-104">\[**Clear** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ba3c7-104">\[The **Clear** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ba3c7-105">相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="ba3c7-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="ba3c7-106">**Clear** 方法會從收件 [**者集合移除**](recipients.md)所有的 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="ba3c7-106">The **Clear** method removes all [**Certificate**](certificate.md) objects from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba3c7-107">語法</span><span class="sxs-lookup"><span data-stu-id="ba3c7-107">Syntax</span></span>


```VB
Recipients.Clear()
```



## <a name="parameters"></a><span data-ttu-id="ba3c7-108">參數</span><span class="sxs-lookup"><span data-stu-id="ba3c7-108">Parameters</span></span>

<span data-ttu-id="ba3c7-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="ba3c7-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba3c7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ba3c7-110">Return value</span></span>

<span data-ttu-id="ba3c7-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ba3c7-111">This method does not return a value.</span></span> <span data-ttu-id="ba3c7-112">使用這個方法的應用程式必須包含程式碼，以處理此方法所引發的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="ba3c7-112">An application that uses this method must contain code to handle an exception raised by this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba3c7-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba3c7-113">Requirements</span></span>



| <span data-ttu-id="ba3c7-114">需求</span><span class="sxs-lookup"><span data-stu-id="ba3c7-114">Requirement</span></span> | <span data-ttu-id="ba3c7-115">值</span><span class="sxs-lookup"><span data-stu-id="ba3c7-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3c7-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ba3c7-116">Redistributable</span></span><br/> | <span data-ttu-id="ba3c7-117">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ba3c7-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ba3c7-118">DLL</span><span class="sxs-lookup"><span data-stu-id="ba3c7-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="ba3c7-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba3c7-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba3c7-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba3c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba3c7-121">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="ba3c7-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="ba3c7-122">**收件者**</span><span class="sxs-lookup"><span data-stu-id="ba3c7-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
