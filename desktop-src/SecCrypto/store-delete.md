---
description: 刪除目前存放區物件所代表的憑證存放區。
ms.assetid: 274914ee-27a0-4bd6-8510-af897aab3a2d
title: Store. Delete 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 41c6417dae5006eb2ecaf64660fd0007cdf37fd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976292"
---
# <a name="storedelete-method"></a><span data-ttu-id="c0f55-103">Store. Delete 方法</span><span class="sxs-lookup"><span data-stu-id="c0f55-103">Store.Delete method</span></span>

<span data-ttu-id="c0f55-104">\[**Delete** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="c0f55-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c0f55-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="c0f55-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c0f55-106">**Delete** 方法會刪除目前 [**存放區**](certificate.md)物件所代表的 [*憑證存放區*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c0f55-106">The **Delete** method deletes the [*certificate store*](../secgloss/c-gly.md) that is represented by the current [**Store**](certificate.md) object.</span></span> <span data-ttu-id="c0f55-107">這個方法只會刪除非系統存放區。</span><span class="sxs-lookup"><span data-stu-id="c0f55-107">This method deletes only nonsystem stores.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0f55-108">語法</span><span class="sxs-lookup"><span data-stu-id="c0f55-108">Syntax</span></span>


```VB
Store.Delete()
```



## <a name="parameters"></a><span data-ttu-id="c0f55-109">參數</span><span class="sxs-lookup"><span data-stu-id="c0f55-109">Parameters</span></span>

<span data-ttu-id="c0f55-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="c0f55-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0f55-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c0f55-111">Return value</span></span>

<span data-ttu-id="c0f55-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c0f55-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0f55-113">備註</span><span class="sxs-lookup"><span data-stu-id="c0f55-113">Remarks</span></span>

<span data-ttu-id="c0f55-114">下列存放區是系統存放區，無法刪除：</span><span class="sxs-lookup"><span data-stu-id="c0f55-114">The following stores are system stores and cannot be deleted:</span></span>

-   <span data-ttu-id="c0f55-115">My</span><span class="sxs-lookup"><span data-stu-id="c0f55-115">My</span></span>
-   <span data-ttu-id="c0f55-116">Root</span><span class="sxs-lookup"><span data-stu-id="c0f55-116">Root</span></span>
-   <span data-ttu-id="c0f55-117">信任</span><span class="sxs-lookup"><span data-stu-id="c0f55-117">Trust</span></span>
-   <span data-ttu-id="c0f55-118">CA</span><span class="sxs-lookup"><span data-stu-id="c0f55-118">CA</span></span>
-   <span data-ttu-id="c0f55-119">UserDS</span><span class="sxs-lookup"><span data-stu-id="c0f55-119">UserDS</span></span>
-   <span data-ttu-id="c0f55-120">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="c0f55-120">TrustedPublisher</span></span>
-   <span data-ttu-id="c0f55-121">不允許</span><span class="sxs-lookup"><span data-stu-id="c0f55-121">Disallowed</span></span>
-   <span data-ttu-id="c0f55-122">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="c0f55-122">AuthRoot</span></span>
-   <span data-ttu-id="c0f55-123">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="c0f55-123">TrustedPeople</span></span>

<span data-ttu-id="c0f55-124">如果從 web 腳本呼叫， **Delete** 方法會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="c0f55-124">The **Delete** method returns an error if called from a web script.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0f55-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0f55-125">Requirements</span></span>



| <span data-ttu-id="c0f55-126">需求</span><span class="sxs-lookup"><span data-stu-id="c0f55-126">Requirement</span></span> | <span data-ttu-id="c0f55-127">值</span><span class="sxs-lookup"><span data-stu-id="c0f55-127">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0f55-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c0f55-128">Redistributable</span></span><br/> | <span data-ttu-id="c0f55-129">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c0f55-129">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c0f55-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c0f55-130">DLL</span></span><br/>             | <dl> <span data-ttu-id="c0f55-131"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0f55-131"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0f55-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0f55-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0f55-133">**市集**</span><span class="sxs-lookup"><span data-stu-id="c0f55-133">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="c0f55-134">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="c0f55-134">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
