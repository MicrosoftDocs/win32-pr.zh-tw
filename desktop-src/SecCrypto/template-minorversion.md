---
description: 捕獲範本的次要版本號碼。
ms.assetid: 3fc51d43-9113-4b4b-88ab-27cf6e5c4fa0
title: MinorVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MinorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a1de0beb41cbe87ca86b443c5cc2145c2058073
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999634"
---
# <a name="templateminorversion-property"></a><span data-ttu-id="6d398-103">MinorVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="6d398-103">Template.MinorVersion property</span></span>

<span data-ttu-id="6d398-104">\[**MinorVersion** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6d398-104">\[The **MinorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d398-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]</span><span class="sxs-lookup"><span data-stu-id="6d398-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="6d398-106">**MinorVersion** 屬性會捕獲範本的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6d398-106">The **MinorVersion** property retrieves the minor version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d398-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6d398-107">Syntax</span></span>


```VB
Template.MinorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="6d398-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="6d398-108">Property value</span></span>

<span data-ttu-id="6d398-109">範本的次要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="6d398-109">The minor version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d398-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d398-110">Requirements</span></span>



| <span data-ttu-id="6d398-111">需求</span><span class="sxs-lookup"><span data-stu-id="6d398-111">Requirement</span></span> | <span data-ttu-id="6d398-112">值</span><span class="sxs-lookup"><span data-stu-id="6d398-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d398-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6d398-113">Redistributable</span></span><br/> | <span data-ttu-id="6d398-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6d398-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6d398-115">DLL</span><span class="sxs-lookup"><span data-stu-id="6d398-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6d398-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d398-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d398-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d398-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d398-118">**範本**</span><span class="sxs-lookup"><span data-stu-id="6d398-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
