---
description: 抓取此物件所代表的憑證存放區名稱。
ms.assetid: db61b464-0e8e-4b19-be12-04e00d6bba53
title: Store.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 85679bb594bdb59c41773b7f956deea95021381f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990849"
---
# <a name="storename-property"></a><span data-ttu-id="2386c-103">Store.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="2386c-103">Store.Name property</span></span>

<span data-ttu-id="2386c-104">\[[ [**名稱**](store-location.md) ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2386c-104">\[The [**Name**](store-location.md) property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2386c-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="2386c-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="2386c-106">[**Name**](store-location.md)屬性會抓取此物件所代表的憑證存放區名稱。</span><span class="sxs-lookup"><span data-stu-id="2386c-106">The [**Name**](store-location.md) property retrieves the name of the certificate store that this object represents.</span></span>

## <a name="syntax"></a><span data-ttu-id="2386c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2386c-107">Syntax</span></span>


```VB
Store.Name As String
```



## <a name="property-value"></a><span data-ttu-id="2386c-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="2386c-108">Property value</span></span>

<span data-ttu-id="2386c-109">表示憑證存放區名稱的 **字串** 值。</span><span class="sxs-lookup"><span data-stu-id="2386c-109">The **String** value that represents the name of the certificate store.</span></span>

## <a name="remarks"></a><span data-ttu-id="2386c-110">備註</span><span class="sxs-lookup"><span data-stu-id="2386c-110">Remarks</span></span>

<span data-ttu-id="2386c-111">憑證存放區名稱的範例包括 My 和 Root。</span><span class="sxs-lookup"><span data-stu-id="2386c-111">Examples of certificate store names include My and Root.</span></span>

<span data-ttu-id="2386c-112">[**Name**](store-location.md)屬性的值與開啟存放區時，針對 [**Open**](store-open.md)方法的 *StoreName* 參數所提供的值相同。</span><span class="sxs-lookup"><span data-stu-id="2386c-112">The value of the [**Name**](store-location.md) property is the same as the value supplied for the *StoreName* parameter of the [**Open**](store-open.md) method when the store was opened.</span></span>

## <a name="requirements"></a><span data-ttu-id="2386c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2386c-113">Requirements</span></span>



| <span data-ttu-id="2386c-114">需求</span><span class="sxs-lookup"><span data-stu-id="2386c-114">Requirement</span></span> | <span data-ttu-id="2386c-115">值</span><span class="sxs-lookup"><span data-stu-id="2386c-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2386c-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2386c-116">Redistributable</span></span><br/> | <span data-ttu-id="2386c-117">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.1 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2386c-117">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2386c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="2386c-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="2386c-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2386c-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2386c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2386c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2386c-121">**市集**</span><span class="sxs-lookup"><span data-stu-id="2386c-121">**Store**</span></span>](store.md)
</dt> </dl>

 

 
