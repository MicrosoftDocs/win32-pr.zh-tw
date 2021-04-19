---
description: 抓取已驗證之屬性的集合。
ms.assetid: d4b3efab-d71e-4fef-9691-0c0bbcb27281
title: AuthenticatedAttributes 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signer.AuthenticatedAttributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3963ec60d699300c4cde368d4d78c39c0873edd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977618"
---
# <a name="signerauthenticatedattributes-property"></a><span data-ttu-id="616c6-103">AuthenticatedAttributes 屬性</span><span class="sxs-lookup"><span data-stu-id="616c6-103">Signer.AuthenticatedAttributes property</span></span>

<span data-ttu-id="616c6-104">\[**AuthenticatedAttributes** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="616c6-104">\[The **AuthenticatedAttributes** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="616c6-105">相反地，請使用 [**CmsSigner 類別**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="616c6-105">Instead, use the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="616c6-106">**AuthenticatedAttributes** 屬性會抓取已驗證之屬性的集合。</span><span class="sxs-lookup"><span data-stu-id="616c6-106">The **AuthenticatedAttributes** property retrieves the collection of authenticated attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="616c6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="616c6-107">Syntax</span></span>


```VB
Signer.AuthenticatedAttributes As Attributes
```



## <a name="property-value"></a><span data-ttu-id="616c6-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="616c6-108">Property value</span></span>

<span data-ttu-id="616c6-109">代表簽署者之已驗證屬性的 [**屬性**](attributes.md) 集合。</span><span class="sxs-lookup"><span data-stu-id="616c6-109">An [**Attributes**](attributes.md) collection that represents the signer's authenticated attributes.</span></span>

## <a name="requirements"></a><span data-ttu-id="616c6-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="616c6-110">Requirements</span></span>



| <span data-ttu-id="616c6-111">需求</span><span class="sxs-lookup"><span data-stu-id="616c6-111">Requirement</span></span> | <span data-ttu-id="616c6-112">值</span><span class="sxs-lookup"><span data-stu-id="616c6-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="616c6-113">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="616c6-113">Redistributable</span></span><br/> | <span data-ttu-id="616c6-114">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="616c6-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="616c6-115">DLL</span><span class="sxs-lookup"><span data-stu-id="616c6-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="616c6-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616c6-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="616c6-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="616c6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616c6-118">**簽署者**</span><span class="sxs-lookup"><span data-stu-id="616c6-118">**Signer**</span></span>](signer.md)
</dt> </dl>

 

 
