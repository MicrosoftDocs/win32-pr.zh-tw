---
description: 抓取代表索引簽署者的簽署者物件。
ms.assetid: a95f4e33-ab92-44e1-91ab-2c5335a04f05
title: 簽署者. 專案屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Signers.Item
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9b0b4179c1ea7e2ded5d945f64f03124eb864fdc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990843"
---
# <a name="signersitem-property"></a><span data-ttu-id="9c493-103">簽署者. 專案屬性</span><span class="sxs-lookup"><span data-stu-id="9c493-103">Signers.Item property</span></span>

<span data-ttu-id="9c493-104">\[**專案** 屬性可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="9c493-104">\[The **Item** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9c493-105">相反地，請使用 CmsSigner 物件的集合。</span><span class="sxs-lookup"><span data-stu-id="9c493-105">Instead, use a collection of CmsSigner objects.</span></span> <span data-ttu-id="9c493-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span><span class="sxs-lookup"><span data-stu-id="9c493-106">For more information, see the [**CmsSigner Class**](/dotnet/api/system.security.cryptography.pkcs.cmssigner?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9c493-107">**Item** 屬性會抓取代表索引簽署者的 [**簽署者**](signer.md)物件。</span><span class="sxs-lookup"><span data-stu-id="9c493-107">The **Item** property retrieves the [**Signer**](signer.md) object that represents the indexed signer.</span></span> <span data-ttu-id="9c493-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="9c493-108">This is the default property.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c493-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c493-109">Syntax</span></span>


```VB
Signers.Item( _
  ByVal Index _
) As Variant
```



## <a name="property-value"></a><span data-ttu-id="9c493-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="9c493-110">Property value</span></span>

<span data-ttu-id="9c493-111">代表索引簽署者的 [**簽署者**](signer.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="9c493-111">The [**Signer**](signer.md) object that represents the indexed signer.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c493-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c493-112">Requirements</span></span>



| <span data-ttu-id="9c493-113">需求</span><span class="sxs-lookup"><span data-stu-id="9c493-113">Requirement</span></span> | <span data-ttu-id="9c493-114">值</span><span class="sxs-lookup"><span data-stu-id="9c493-114">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c493-115">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9c493-115">Redistributable</span></span><br/> | <span data-ttu-id="9c493-116">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9c493-116">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9c493-117">DLL</span><span class="sxs-lookup"><span data-stu-id="9c493-117">DLL</span></span><br/>             | <dl> <span data-ttu-id="9c493-118"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c493-118"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c493-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c493-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c493-120">**簽名**</span><span class="sxs-lookup"><span data-stu-id="9c493-120">**Signers**</span></span>](signers.md)
</dt> </dl>

 

 
