---
description: 抓取資料的簽名建立者。
ms.assetid: 3e28f08a-c4d8-4dd7-953a-e1500eb5bee0
title: SignedData。簽署者屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignedData.Signers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5f4c58c2a69c483fc38412a6aa8377742d52d39a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985746"
---
# <a name="signeddatasigners-property"></a><span data-ttu-id="6b66d-103">SignedData。簽署者屬性</span><span class="sxs-lookup"><span data-stu-id="6b66d-103">SignedData.Signers property</span></span>

<span data-ttu-id="6b66d-104">\[[ **簽署** 者] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="6b66d-104">\[The **Signers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6b66d-105">相反地，請使用 [**SignedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="6b66d-105">Instead, use the [**SignedCms Class**](/dotnet/api/system.security.cryptography.pkcs.signedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="6b66d-106">**簽署** 者屬性會抓取資料的簽章建立者。</span><span class="sxs-lookup"><span data-stu-id="6b66d-106">The **Signers** property retrieves the signature creators of the data.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b66d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b66d-107">Syntax</span></span>


```VB
SignedData.Signers As Signers
```



## <a name="property-value"></a><span data-ttu-id="6b66d-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="6b66d-108">Property value</span></span>

<span data-ttu-id="6b66d-109">代表資料簽章建立者的 [**簽署**](signers.md) 者集合。</span><span class="sxs-lookup"><span data-stu-id="6b66d-109">The [**Signers**](signers.md) collection that represents the signature creators of the data.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b66d-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b66d-110">Requirements</span></span>



| <span data-ttu-id="6b66d-111">需求</span><span class="sxs-lookup"><span data-stu-id="6b66d-111">Requirement</span></span> | <span data-ttu-id="6b66d-112">值</span><span class="sxs-lookup"><span data-stu-id="6b66d-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b66d-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="6b66d-113">Redistributable</span></span><br/> | <span data-ttu-id="6b66d-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6b66d-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6b66d-115">DLL</span><span class="sxs-lookup"><span data-stu-id="6b66d-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="6b66d-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b66d-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b66d-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b66d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b66d-118">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="6b66d-118">**SignedData**</span></span>](signeddata.md)
</dt> </dl>

 

 
