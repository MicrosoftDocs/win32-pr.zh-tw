---
description: 抓取與辨識符號相關聯的組織名稱。
ms.assetid: 4ceb2c0f-903d-4fcd-8446-abf3175fe8e0
title: OrganizationName 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.OrganizationName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1e1ebb2b948d5a933b59e86c8753b6b68a3a94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001584"
---
# <a name="qualifierorganizationname-property"></a><span data-ttu-id="4b7b7-103">OrganizationName 屬性</span><span class="sxs-lookup"><span data-stu-id="4b7b7-103">Qualifier.OrganizationName property</span></span>

<span data-ttu-id="4b7b7-104">\[**OrganizationName** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4b7b7-104">\[The **OrganizationName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4b7b7-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="4b7b7-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="4b7b7-106">**OrganizationName** 屬性會抓取與辨識符號相關聯的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b7-106">The **OrganizationName** property retrieves the name of the organization associated with the qualifier.</span></span> <span data-ttu-id="4b7b7-107">這個屬性可以是空的。</span><span class="sxs-lookup"><span data-stu-id="4b7b7-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b7b7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b7b7-108">Syntax</span></span>


```VB
Qualifier.OrganizationName As String
```



## <a name="property-value"></a><span data-ttu-id="4b7b7-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="4b7b7-109">Property value</span></span>

<span data-ttu-id="4b7b7-110">與辨識符號相關聯的組織名稱。</span><span class="sxs-lookup"><span data-stu-id="4b7b7-110">The name of the organization associated with the qualifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="4b7b7-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4b7b7-111">Requirements</span></span>



| <span data-ttu-id="4b7b7-112">需求</span><span class="sxs-lookup"><span data-stu-id="4b7b7-112">Requirement</span></span> | <span data-ttu-id="4b7b7-113">值</span><span class="sxs-lookup"><span data-stu-id="4b7b7-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4b7b7-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4b7b7-114">Redistributable</span></span><br/> | <span data-ttu-id="4b7b7-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4b7b7-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4b7b7-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4b7b7-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="4b7b7-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4b7b7-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b7b7-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4b7b7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b7b7-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="4b7b7-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
