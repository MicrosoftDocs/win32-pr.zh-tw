---
description: 抓取此物件所代表之憑證存放區的位置。
ms.assetid: 756ee7cb-5f9f-4fb2-bf10-79b543895189
title: Store. Location 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Location
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 42afe40dffde5a0375928d355508ec75a4076f17
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983222"
---
# <a name="storelocation-property"></a><span data-ttu-id="14ac1-103">Store. Location 屬性</span><span class="sxs-lookup"><span data-stu-id="14ac1-103">Store.Location property</span></span>

<span data-ttu-id="14ac1-104">\[[ **位置** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="14ac1-104">\[The **Location** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="14ac1-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="14ac1-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="14ac1-106">**Location** 屬性會抓取此物件所代表之憑證存放區的位置。</span><span class="sxs-lookup"><span data-stu-id="14ac1-106">The **Location** property retrieves the location of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="14ac1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="14ac1-107">Syntax</span></span>


```VB
Store.Location As CAPICOM_STORE_LOCATION
```



## <a name="property-value"></a><span data-ttu-id="14ac1-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="14ac1-108">Property value</span></span>

<span data-ttu-id="14ac1-109">表示憑證存放區位置的 [**CAPICOM \_ 存放區 \_ 位置**](capicom-store-location.md) 值。</span><span class="sxs-lookup"><span data-stu-id="14ac1-109">The [**CAPICOM\_STORE\_LOCATION**](capicom-store-location.md) value that represents the location of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="14ac1-110">備註</span><span class="sxs-lookup"><span data-stu-id="14ac1-110">Remarks</span></span>

<span data-ttu-id="14ac1-111">**Location** 屬性的值與開啟存放區時，針對 [**Open**](store-open.md)方法的 *StoreLocation* 參數所提供的值相同。</span><span class="sxs-lookup"><span data-stu-id="14ac1-111">The value of the **Location** property is the same as the value supplied for the *StoreLocation* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="14ac1-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="14ac1-112">Requirements</span></span>



| <span data-ttu-id="14ac1-113">需求</span><span class="sxs-lookup"><span data-stu-id="14ac1-113">Requirement</span></span> | <span data-ttu-id="14ac1-114">值</span><span class="sxs-lookup"><span data-stu-id="14ac1-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14ac1-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="14ac1-115">Redistributable</span></span><br/> | <span data-ttu-id="14ac1-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本</span><span class="sxs-lookup"><span data-stu-id="14ac1-116">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="14ac1-117">DLL</span><span class="sxs-lookup"><span data-stu-id="14ac1-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="14ac1-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14ac1-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14ac1-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14ac1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14ac1-120">**市集**</span><span class="sxs-lookup"><span data-stu-id="14ac1-120">**Store**</span></span>](store.md)
</dt> </dl>

 

 
