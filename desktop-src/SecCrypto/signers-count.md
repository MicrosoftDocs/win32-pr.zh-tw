---
description: 抓取集合中的簽署者物件數目。
ms.assetid: 990e273a-8f3d-4a77-b0a4-243eeb32e6f3
title: 簽署者. 計數屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Count
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fd8296acfaf5e0d25f7d8a80c1c96e53cfa35578
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984751"
---
# <a name="signerscount-property"></a><span data-ttu-id="eb02e-103">簽署者. 計數屬性</span><span class="sxs-lookup"><span data-stu-id="eb02e-103">Signers.Count property</span></span>

<span data-ttu-id="eb02e-104">\[[ **計數** ] 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="eb02e-104">\[The **Count** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eb02e-105">相反地，請使用 CmsSigner 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="eb02e-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="eb02e-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span><span class="sxs-lookup"><span data-stu-id="eb02e-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="eb02e-107">**Count** 屬性會抓取集合中的 [**簽署者**](signer.md)物件數目。</span><span class="sxs-lookup"><span data-stu-id="eb02e-107">The **Count** property retrieves the number of [**Signer**](signer.md) objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb02e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eb02e-108">Syntax</span></span>


```VB
Signers.Count As Long
```



## <a name="property-value"></a><span data-ttu-id="eb02e-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="eb02e-109">Property value</span></span>

<span data-ttu-id="eb02e-110">集合中的 [**簽署者**](signer.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="eb02e-110">Number of [**Signer**](signer.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb02e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb02e-111">Requirements</span></span>



| <span data-ttu-id="eb02e-112">需求</span><span class="sxs-lookup"><span data-stu-id="eb02e-112">Requirement</span></span> | <span data-ttu-id="eb02e-113">值</span><span class="sxs-lookup"><span data-stu-id="eb02e-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb02e-114">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="eb02e-114">Redistributable</span></span><br/> | <span data-ttu-id="eb02e-115">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="eb02e-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="eb02e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="eb02e-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="eb02e-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb02e-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb02e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb02e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb02e-119">**簽名**</span><span class="sxs-lookup"><span data-stu-id="eb02e-119">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
