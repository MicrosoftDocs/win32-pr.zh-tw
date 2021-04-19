---
description: 抓取識別範本物件的 OID 物件。
ms.assetid: bdd9d401-e9c4-4307-9817-7dcb55c539f8
title: Template 的 OID 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.OID
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 4a8599ac999c7d6a3e3403d94ff2c6daf0eba48b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994791"
---
# <a name="templateoid-property"></a><span data-ttu-id="e3b17-103">Template 的 OID 屬性</span><span class="sxs-lookup"><span data-stu-id="e3b17-103">Template.OID property</span></span>

<span data-ttu-id="e3b17-104">\[**OID** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="e3b17-104">\[The **OID** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="e3b17-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]</span><span class="sxs-lookup"><span data-stu-id="e3b17-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="e3b17-106">**Oid** 屬性會抓取可識別 [**範本**](template.md)物件的 [**oid**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="e3b17-106">The **OID** property retrieves an [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

<span data-ttu-id="e3b17-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e3b17-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3b17-108">語法</span><span class="sxs-lookup"><span data-stu-id="e3b17-108">Syntax</span></span>


```VB
Template.OID As OID
```



## <a name="property-value"></a><span data-ttu-id="e3b17-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e3b17-109">Property value</span></span>

<span data-ttu-id="e3b17-110">識別 [**範本**](template.md)物件的 [**OID**](oid.md)物件。</span><span class="sxs-lookup"><span data-stu-id="e3b17-110">An [**OID**](oid.md) object that identifies the [**Template**](template.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3b17-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3b17-111">Requirements</span></span>



| <span data-ttu-id="e3b17-112">需求</span><span class="sxs-lookup"><span data-stu-id="e3b17-112">Requirement</span></span> | <span data-ttu-id="e3b17-113">值</span><span class="sxs-lookup"><span data-stu-id="e3b17-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b17-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e3b17-114">Redistributable</span></span><br/> | <span data-ttu-id="e3b17-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e3b17-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e3b17-116">DLL</span><span class="sxs-lookup"><span data-stu-id="e3b17-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="e3b17-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3b17-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3b17-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3b17-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3b17-119">**範本**</span><span class="sxs-lookup"><span data-stu-id="e3b17-119">**Template**</span></span>](template.md)
</dt> </dl>

 

 
