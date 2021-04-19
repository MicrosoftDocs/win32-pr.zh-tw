---
description: 捕獲使用者聲明編號的集合。
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: NoticeNumbers 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990658"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="76182-103">NoticeNumbers 屬性</span><span class="sxs-lookup"><span data-stu-id="76182-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="76182-104">\[**NoticeNumbers** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="76182-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="76182-105">相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]</span><span class="sxs-lookup"><span data-stu-id="76182-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="76182-106">**NoticeNumbers** 屬性會抓取使用者聲明編號的集合。</span><span class="sxs-lookup"><span data-stu-id="76182-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="76182-107">這個屬性可以是空的。</span><span class="sxs-lookup"><span data-stu-id="76182-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="76182-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="76182-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="76182-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="76182-109">Property value</span></span>

<span data-ttu-id="76182-110">使用者聲明編號的集合。</span><span class="sxs-lookup"><span data-stu-id="76182-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="76182-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="76182-111">Requirements</span></span>



| <span data-ttu-id="76182-112">需求</span><span class="sxs-lookup"><span data-stu-id="76182-112">Requirement</span></span> | <span data-ttu-id="76182-113">值</span><span class="sxs-lookup"><span data-stu-id="76182-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76182-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="76182-114">Redistributable</span></span><br/> | <span data-ttu-id="76182-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="76182-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="76182-116">DLL</span><span class="sxs-lookup"><span data-stu-id="76182-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="76182-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76182-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76182-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76182-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76182-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="76182-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
