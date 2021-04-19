---
description: 關閉開啟的憑證存放區。
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001153"
---
# <a name="storeclose-method"></a><span data-ttu-id="93b89-103">Store. Close 方法</span><span class="sxs-lookup"><span data-stu-id="93b89-103">Store.Close method</span></span>

<span data-ttu-id="93b89-104">\[**Close** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="93b89-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="93b89-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="93b89-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="93b89-106">**Close** 方法會關閉已開啟的 [*憑證存放區*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="93b89-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="93b89-107">語法</span><span class="sxs-lookup"><span data-stu-id="93b89-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="93b89-108">參數</span><span class="sxs-lookup"><span data-stu-id="93b89-108">Parameters</span></span>

<span data-ttu-id="93b89-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="93b89-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="93b89-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="93b89-110">Return value</span></span>

<span data-ttu-id="93b89-111">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="93b89-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93b89-112">備註</span><span class="sxs-lookup"><span data-stu-id="93b89-112">Remarks</span></span>

<span data-ttu-id="93b89-113">呼叫 **Close** 方法之後，就會終結 [**存放區**](store.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="93b89-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="93b89-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="93b89-114">Requirements</span></span>



| <span data-ttu-id="93b89-115">需求</span><span class="sxs-lookup"><span data-stu-id="93b89-115">Requirement</span></span> | <span data-ttu-id="93b89-116">值</span><span class="sxs-lookup"><span data-stu-id="93b89-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93b89-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="93b89-117">Redistributable</span></span><br/> | <span data-ttu-id="93b89-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本</span><span class="sxs-lookup"><span data-stu-id="93b89-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="93b89-119">DLL</span><span class="sxs-lookup"><span data-stu-id="93b89-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="93b89-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93b89-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b89-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93b89-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b89-122">**市集**</span><span class="sxs-lookup"><span data-stu-id="93b89-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="93b89-123">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="93b89-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="93b89-124">**打開**</span><span class="sxs-lookup"><span data-stu-id="93b89-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
