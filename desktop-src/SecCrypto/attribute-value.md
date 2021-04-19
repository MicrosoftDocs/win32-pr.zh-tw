---
description: 設定或抓取屬性的值。
ms.assetid: aaf0c07c-756f-48c8-b4cd-def40f7cb1a3
title: Attribute。 Value 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Value
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 6b3d2f41c56fc47277bd71354279e75b423d0c0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106980138"
---
# <a name="attributevalue-property"></a><span data-ttu-id="9b2a6-103">Attribute。 Value 屬性</span><span class="sxs-lookup"><span data-stu-id="9b2a6-103">Attribute.Value property</span></span>

<span data-ttu-id="9b2a6-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="9b2a6-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="9b2a6-105">請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObject 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true)。\]</span><span class="sxs-lookup"><span data-stu-id="9b2a6-105">Instead, use the [**CryptographicAttributeObject Class**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="9b2a6-106">**Value** 屬性會設定或抓取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="9b2a6-106">The **Value** property sets or retrieves the value of the attribute.</span></span>

<span data-ttu-id="9b2a6-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9b2a6-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b2a6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b2a6-108">Syntax</span></span>


```VB
Attribute.Value As Variant
```



## <a name="property-value"></a><span data-ttu-id="9b2a6-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="9b2a6-109">Property value</span></span>

<span data-ttu-id="9b2a6-110">包含屬性值的 **Variant** 變數。</span><span class="sxs-lookup"><span data-stu-id="9b2a6-110">A **Variant** variable that contains the value of the attribute.</span></span> <span data-ttu-id="9b2a6-111">若為 **CAPICOM \_ 驗證的 \_ 屬性 \_ 簽署 \_ 時間** 屬性，資料類型為 **DATE**。</span><span class="sxs-lookup"><span data-stu-id="9b2a6-111">For **CAPICOM\_AUTHENTICATED\_ATTRIBUTE\_SIGNING\_TIME** attributes, the data type is **DATE**.</span></span> <span data-ttu-id="9b2a6-112">若為其他所有屬性，則屬性值為字串。</span><span class="sxs-lookup"><span data-stu-id="9b2a6-112">For all other attributes, the property value is a string.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b2a6-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b2a6-113">Requirements</span></span>



| <span data-ttu-id="9b2a6-114">需求</span><span class="sxs-lookup"><span data-stu-id="9b2a6-114">Requirement</span></span> | <span data-ttu-id="9b2a6-115">值</span><span class="sxs-lookup"><span data-stu-id="9b2a6-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b2a6-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9b2a6-116">End of client support</span></span><br/> | <span data-ttu-id="9b2a6-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b2a6-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9b2a6-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9b2a6-118">End of server support</span></span><br/> | <span data-ttu-id="9b2a6-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b2a6-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9b2a6-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="9b2a6-120">Redistributable</span></span><br/>       | <span data-ttu-id="9b2a6-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="9b2a6-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9b2a6-122">DLL</span><span class="sxs-lookup"><span data-stu-id="9b2a6-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9b2a6-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b2a6-123"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
