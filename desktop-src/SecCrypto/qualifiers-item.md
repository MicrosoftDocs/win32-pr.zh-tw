---
description: 根據指定的索引來抓取限定詞。
ms.assetid: 4d54358d-99de-4a1c-b843-41006f47a279
title: 限定詞。 Item 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 798b1f212aabd5b1ab34a1eefb626be4572b9c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981386"
---
# <a name="qualifiersitem-property"></a><span data-ttu-id="ec48e-103">限定詞。 Item 屬性</span><span class="sxs-lookup"><span data-stu-id="ec48e-103">Qualifiers.Item property</span></span>

<span data-ttu-id="ec48e-104">\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ec48e-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ec48e-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="ec48e-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="ec48e-106">**Item** 屬性會根據指定的索引來抓取限定詞。</span><span class="sxs-lookup"><span data-stu-id="ec48e-106">The **Item** property retrieves a qualifier based on a specified index.</span></span> <span data-ttu-id="ec48e-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="ec48e-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec48e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec48e-108">Syntax</span></span>


```VB
Qualifiers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="ec48e-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="ec48e-109">Property value</span></span>

<span data-ttu-id="ec48e-110">代表集合之索引限定詞的辨識 [**符號**](qualifier.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="ec48e-110">A [**Qualifier**](qualifier.md) object that represents the indexed qualifier of the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec48e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec48e-111">Requirements</span></span>



| <span data-ttu-id="ec48e-112">需求</span><span class="sxs-lookup"><span data-stu-id="ec48e-112">Requirement</span></span> | <span data-ttu-id="ec48e-113">值</span><span class="sxs-lookup"><span data-stu-id="ec48e-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec48e-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ec48e-114">Redistributable</span></span><br/> | <span data-ttu-id="ec48e-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="ec48e-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ec48e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ec48e-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="ec48e-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec48e-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec48e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec48e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec48e-119">**限定詞**</span><span class="sxs-lookup"><span data-stu-id="ec48e-119">**Qualifiers**</span></span>](qualifiers.md)
</dt> </dl>

 

 
