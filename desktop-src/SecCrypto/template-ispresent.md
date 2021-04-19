---
description: 抓取布林值，指出範本延伸是否存在。
ms.assetid: cc7f9853-8212-470d-b372-43a4bbd517f7
title: IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 23dcd8cc5ee92a689300078d439998e43933af93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986799"
---
# <a name="templateispresent-property"></a><span data-ttu-id="2dd72-103">IsPresent 屬性</span><span class="sxs-lookup"><span data-stu-id="2dd72-103">Template.IsPresent property</span></span>

<span data-ttu-id="2dd72-104">\[**IsPresent** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="2dd72-104">\[The **IsPresent** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2dd72-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]</span><span class="sxs-lookup"><span data-stu-id="2dd72-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="2dd72-106">**IsPresent** 屬性會抓取布林值，指出範本延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="2dd72-106">The **IsPresent** property retrieves a Boolean value that indicates whether the template extension is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dd72-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2dd72-107">Syntax</span></span>


```VB
Template.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="2dd72-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="2dd72-108">Property value</span></span>

<span data-ttu-id="2dd72-109">若 **為 true**，表示範本延伸模組存在。</span><span class="sxs-lookup"><span data-stu-id="2dd72-109">If **true**, the template extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dd72-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="2dd72-110">Requirements</span></span>



| <span data-ttu-id="2dd72-111">需求</span><span class="sxs-lookup"><span data-stu-id="2dd72-111">Requirement</span></span> | <span data-ttu-id="2dd72-112">值</span><span class="sxs-lookup"><span data-stu-id="2dd72-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2dd72-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2dd72-113">Redistributable</span></span><br/> | <span data-ttu-id="2dd72-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="2dd72-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="2dd72-115">DLL</span><span class="sxs-lookup"><span data-stu-id="2dd72-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="2dd72-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2dd72-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dd72-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2dd72-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dd72-118">**範本**</span><span class="sxs-lookup"><span data-stu-id="2dd72-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
