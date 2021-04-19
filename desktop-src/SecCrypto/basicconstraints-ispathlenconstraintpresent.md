---
description: 抓取布林值，指出路徑長度條件約束是否存在。
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: BasicConstraints. IsPathLenConstraintPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9809b6747bac548b14b37384719dbe2660188582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981352"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a><span data-ttu-id="1f40b-103">BasicConstraints. IsPathLenConstraintPresent 屬性</span><span class="sxs-lookup"><span data-stu-id="1f40b-103">BasicConstraints.IsPathLenConstraintPresent property</span></span>

<span data-ttu-id="1f40b-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="1f40b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="1f40b-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="1f40b-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="1f40b-106">**IsPathLenConstraintPresent** 屬性會抓取布林值，指出路徑長度條件約束是否存在。</span><span class="sxs-lookup"><span data-stu-id="1f40b-106">The **IsPathLenConstraintPresent** property retrieves a Boolean value that indicates whether the path length constraint is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f40b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f40b-107">Syntax</span></span>


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="1f40b-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="1f40b-108">Property value</span></span>

<span data-ttu-id="1f40b-109">若 **為 True**，則表示路徑長度條件約束存在。</span><span class="sxs-lookup"><span data-stu-id="1f40b-109">If **True**, the path length constraint is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f40b-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="1f40b-110">Requirements</span></span>



| <span data-ttu-id="1f40b-111">需求</span><span class="sxs-lookup"><span data-stu-id="1f40b-111">Requirement</span></span> | <span data-ttu-id="1f40b-112">值</span><span class="sxs-lookup"><span data-stu-id="1f40b-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f40b-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1f40b-113">End of client support</span></span><br/> | <span data-ttu-id="1f40b-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f40b-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="1f40b-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="1f40b-115">End of server support</span></span><br/> | <span data-ttu-id="1f40b-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f40b-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="1f40b-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1f40b-117">Redistributable</span></span><br/>       | <span data-ttu-id="1f40b-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="1f40b-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="1f40b-119">DLL</span><span class="sxs-lookup"><span data-stu-id="1f40b-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="1f40b-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f40b-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
