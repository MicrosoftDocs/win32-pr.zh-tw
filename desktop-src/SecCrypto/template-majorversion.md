---
description: 捕獲範本的主要版本號碼。
ms.assetid: efde3a7c-48e0-4bfe-9118-3098c7ef8771
title: MajorVersion 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Template.MajorVersion
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a193a36ed7e914d1ed45d26c21008a7e59a5b8a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998655"
---
# <a name="templatemajorversion-property"></a><span data-ttu-id="4e308-103">MajorVersion 屬性</span><span class="sxs-lookup"><span data-stu-id="4e308-103">Template.MajorVersion property</span></span>

<span data-ttu-id="4e308-104">\[**MajorVersion** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4e308-104">\[The **MajorVersion** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4e308-105">相反地，請使用 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中的 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫接受 OID 作為參數的函式，然後使用憑證範本的 oid 來取得憑證延伸範本。\]</span><span class="sxs-lookup"><span data-stu-id="4e308-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Template to retrieve the certificate extension template.\]</span></span>

<span data-ttu-id="4e308-106">**MajorVersion** 屬性會捕獲範本的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="4e308-106">The **MajorVersion** property retrieves the major version number of the template.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e308-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e308-107">Syntax</span></span>


```VB
Template.MajorVersion As Long
```



## <a name="property-value"></a><span data-ttu-id="4e308-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="4e308-108">Property value</span></span>

<span data-ttu-id="4e308-109">範本的主要版本號碼。</span><span class="sxs-lookup"><span data-stu-id="4e308-109">The major version number of the template.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e308-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e308-110">Requirements</span></span>



| <span data-ttu-id="4e308-111">需求</span><span class="sxs-lookup"><span data-stu-id="4e308-111">Requirement</span></span> | <span data-ttu-id="4e308-112">值</span><span class="sxs-lookup"><span data-stu-id="4e308-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4e308-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="4e308-113">Redistributable</span></span><br/> | <span data-ttu-id="4e308-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="4e308-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4e308-115">DLL</span><span class="sxs-lookup"><span data-stu-id="4e308-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="4e308-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e308-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4e308-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e308-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e308-118">**範本**</span><span class="sxs-lookup"><span data-stu-id="4e308-118">**Template**</span></span>](template.md)
</dt> </dl>

 

 
