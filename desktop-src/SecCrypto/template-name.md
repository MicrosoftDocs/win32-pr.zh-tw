---
description: 抓取範本的名稱。
ms.assetid: f92346bc-89b6-4063-aa66-85e2fb88d67d
title: Template.Name 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 005a9cc961b1d7be0ebda0b8e76307b95d92a6d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996217"
---
# <a name="templatename-property"></a><span data-ttu-id="489af-103">Template.Name 屬性</span><span class="sxs-lookup"><span data-stu-id="489af-103">Template.Name property</span></span>

<span data-ttu-id="489af-104">\[[ **名稱** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="489af-104">\[The **Name** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="489af-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]</span><span class="sxs-lookup"><span data-stu-id="489af-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="489af-106">**Name** 屬性會抓取範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="489af-106">The **Name** property retrieves the name of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="489af-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="489af-107">Syntax</span></span>


```VB
Template.Name As String
```



## <a name="property-value"></a><span data-ttu-id="489af-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="489af-108">Property value</span></span>

<span data-ttu-id="489af-109">範本名稱。</span><span class="sxs-lookup"><span data-stu-id="489af-109">The name of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="489af-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="489af-110">Requirements</span></span>



| <span data-ttu-id="489af-111">需求</span><span class="sxs-lookup"><span data-stu-id="489af-111">Requirement</span></span> | <span data-ttu-id="489af-112">值</span><span class="sxs-lookup"><span data-stu-id="489af-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="489af-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="489af-113">Redistributable</span></span><br/> | <span data-ttu-id="489af-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="489af-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="489af-115">DLL</span><span class="sxs-lookup"><span data-stu-id="489af-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="489af-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="489af-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="489af-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="489af-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="489af-118">**範本**</span><span class="sxs-lookup"><span data-stu-id="489af-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
