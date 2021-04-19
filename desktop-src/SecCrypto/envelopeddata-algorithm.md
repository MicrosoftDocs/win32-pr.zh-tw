---
description: 抓取加密演算法和金鑰長度。
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData 演算法屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989598"
---
# <a name="envelopeddataalgorithm-property"></a><span data-ttu-id="c2b4f-103">EnvelopedData 演算法屬性</span><span class="sxs-lookup"><span data-stu-id="c2b4f-103">EnvelopedData.Algorithm property</span></span>

<span data-ttu-id="c2b4f-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista 和 Windows XP。</span><span class="sxs-lookup"><span data-stu-id="c2b4f-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c2b4f-105">相反地，請使用 [**EnvelopedCms 類別**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="c2b4f-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="c2b4f-106">**演算法** 屬性會捕獲加密演算法和 [*金鑰長度*](../secgloss/k-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="c2b4f-106">The **Algorithm** property retrieves the encryption algorithm and [*key length*](../secgloss/k-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c2b4f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2b4f-107">Syntax</span></span>


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="c2b4f-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="c2b4f-108">Property value</span></span>

<span data-ttu-id="c2b4f-109">包含加密演算法和金鑰長度的 [**演算法**](algorithm.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="c2b4f-109">An [**Algorithm**](algorithm.md) object that contains the encryption algorithm and key length.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2b4f-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="c2b4f-110">Requirements</span></span>



| <span data-ttu-id="c2b4f-111">需求</span><span class="sxs-lookup"><span data-stu-id="c2b4f-111">Requirement</span></span> | <span data-ttu-id="c2b4f-112">值</span><span class="sxs-lookup"><span data-stu-id="c2b4f-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b4f-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="c2b4f-113">End of client support</span></span><br/> | <span data-ttu-id="c2b4f-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c2b4f-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c2b4f-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="c2b4f-115">End of server support</span></span><br/> | <span data-ttu-id="c2b4f-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c2b4f-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c2b4f-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="c2b4f-117">Redistributable</span></span><br/>       | <span data-ttu-id="c2b4f-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="c2b4f-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c2b4f-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c2b4f-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c2b4f-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2b4f-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2b4f-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c2b4f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2b4f-122">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="c2b4f-122">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
