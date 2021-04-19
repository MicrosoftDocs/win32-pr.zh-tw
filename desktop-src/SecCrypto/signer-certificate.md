---
description: 設定或抓取代表資料簽署者之憑證的憑證物件。
ms.assetid: 92ac209e-59b5-4a75-922d-d61629ca41b1
title: 簽署者憑證屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 96652f85e6058682dedd3370965ea7ff2408b3b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992384"
---
# <a name="signercertificate-property"></a><span data-ttu-id="215c9-103">簽署者憑證屬性</span><span class="sxs-lookup"><span data-stu-id="215c9-103">Signer.Certificate property</span></span>

<span data-ttu-id="215c9-104">\[[ **憑證** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="215c9-104">\[The **Certificate** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="215c9-105">相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="215c9-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="215c9-106">**Certificate** 屬性會設定或抓取代表資料簽署者之憑證的 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="215c9-106">The **Certificate** property sets or retrieves the [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span> <span data-ttu-id="215c9-107">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="215c9-107">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="215c9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="215c9-108">Syntax</span></span>


```VB
Signer.Certificate As Certificate
```



## <a name="property-value"></a><span data-ttu-id="215c9-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="215c9-109">Property value</span></span>

<span data-ttu-id="215c9-110">代表資料簽署者之憑證的 [**憑證**](certificate.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="215c9-110">The [**Certificate**](certificate.md) object that represents the certificate of a signer of the data.</span></span>

## <a name="remarks"></a><span data-ttu-id="215c9-111">備註</span><span class="sxs-lookup"><span data-stu-id="215c9-111">Remarks</span></span>

<span data-ttu-id="215c9-112">當這個屬性的值是直接或間接重設時，會重設物件的整個 [*狀態*](../secgloss/s-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="215c9-112">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="215c9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="215c9-113">Requirements</span></span>



| <span data-ttu-id="215c9-114">需求</span><span class="sxs-lookup"><span data-stu-id="215c9-114">Requirement</span></span> | <span data-ttu-id="215c9-115">值</span><span class="sxs-lookup"><span data-stu-id="215c9-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="215c9-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="215c9-116">Redistributable</span></span><br/> | <span data-ttu-id="215c9-117">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="215c9-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="215c9-118">DLL</span><span class="sxs-lookup"><span data-stu-id="215c9-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="215c9-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="215c9-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215c9-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="215c9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215c9-121">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="215c9-121">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
