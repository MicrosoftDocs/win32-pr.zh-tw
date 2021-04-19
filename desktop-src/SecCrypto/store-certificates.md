---
description: 抓取包含存放區中所有憑證的集合。
ms.assetid: 06cfc0e9-8a77-4e10-b559-4d42ac93c01b
title: 存放區憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 979cf31c98286ca5bdd2df709176a27a5abb2321
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984048"
---
# <a name="storecertificates-property"></a><span data-ttu-id="f95e3-103">存放區憑證屬性</span><span class="sxs-lookup"><span data-stu-id="f95e3-103">Store.Certificates property</span></span>

<span data-ttu-id="f95e3-104">\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="f95e3-104">\[The **Certificates** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f95e3-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**system.security.cryptography.x509certificates.x509store 類別**](/previous-versions/windows/embedded/hh424027(v=msdn.10))。\]</span><span class="sxs-lookup"><span data-stu-id="f95e3-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="f95e3-106">[ **憑證** ] 屬性會抓取包含存放區中所有憑證的集合。</span><span class="sxs-lookup"><span data-stu-id="f95e3-106">The **Certificates** property retrieves the collection that includes all of the certificates in the store.</span></span> <span data-ttu-id="f95e3-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="f95e3-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f95e3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f95e3-108">Syntax</span></span>


```VB
Store.Certificates As Certificates
```



## <a name="property-value"></a><span data-ttu-id="f95e3-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f95e3-109">Property value</span></span>

<span data-ttu-id="f95e3-110">存放區中的憑證集合。</span><span class="sxs-lookup"><span data-stu-id="f95e3-110">The collection of certificates in the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="f95e3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="f95e3-111">Requirements</span></span>



| <span data-ttu-id="f95e3-112">需求</span><span class="sxs-lookup"><span data-stu-id="f95e3-112">Requirement</span></span> | <span data-ttu-id="f95e3-113">值</span><span class="sxs-lookup"><span data-stu-id="f95e3-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f95e3-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f95e3-114">Redistributable</span></span><br/> | <span data-ttu-id="f95e3-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f95e3-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="f95e3-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f95e3-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="f95e3-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f95e3-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f95e3-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f95e3-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f95e3-119">**市集**</span><span class="sxs-lookup"><span data-stu-id="f95e3-119">**Store**</span></span>](store.md)
</dt> </dl>

 

 
