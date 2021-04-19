---
description: 抓取布林值，指出基本條件約束延伸是否標記為重大。
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: BasicConstraints. IsCritical 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 8f3f61a0c458229977abae60258ba4cb71420e72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990755"
---
# <a name="basicconstraintsiscritical-property"></a><span data-ttu-id="e4545-103">BasicConstraints. IsCritical 屬性</span><span class="sxs-lookup"><span data-stu-id="e4545-103">BasicConstraints.IsCritical property</span></span>

<span data-ttu-id="e4545-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="e4545-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="e4545-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="e4545-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="e4545-106">**IsCritical** 屬性會抓取布林值，指出基本條件約束延伸是否標記為重大。</span><span class="sxs-lookup"><span data-stu-id="e4545-106">The **IsCritical** property retrieves a Boolean value that indicates whether the basic constraint extension is marked critical.</span></span>

<span data-ttu-id="e4545-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e4545-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4545-108">語法</span><span class="sxs-lookup"><span data-stu-id="e4545-108">Syntax</span></span>


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a><span data-ttu-id="e4545-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="e4545-109">Property value</span></span>

<span data-ttu-id="e4545-110">若 **為 true**，則基本條件約束延伸標示為「重大」。</span><span class="sxs-lookup"><span data-stu-id="e4545-110">If **true**, the basic constraint extension is marked critical.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4545-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="e4545-111">Requirements</span></span>



| <span data-ttu-id="e4545-112">需求</span><span class="sxs-lookup"><span data-stu-id="e4545-112">Requirement</span></span> | <span data-ttu-id="e4545-113">值</span><span class="sxs-lookup"><span data-stu-id="e4545-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4545-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e4545-114">End of client support</span></span><br/> | <span data-ttu-id="e4545-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e4545-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e4545-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e4545-116">End of server support</span></span><br/> | <span data-ttu-id="e4545-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e4545-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e4545-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="e4545-118">Redistributable</span></span><br/>       | <span data-ttu-id="e4545-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e4545-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="e4545-120">DLL</span><span class="sxs-lookup"><span data-stu-id="e4545-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="e4545-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4545-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
