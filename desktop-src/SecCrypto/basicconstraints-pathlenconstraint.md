---
description: 抓取路徑長度條件約束的值。
ms.assetid: 77a12fdf-e9ed-4c79-aa2c-bd476ab3ff90
title: BasicConstraints. PathLenConstraint 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.PathLenConstraint
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 39656cf4f3cbe768589ba704a0a65c158da000fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985761"
---
# <a name="basicconstraintspathlenconstraint-property"></a><span data-ttu-id="81275-103">BasicConstraints. PathLenConstraint 屬性</span><span class="sxs-lookup"><span data-stu-id="81275-103">BasicConstraints.PathLenConstraint property</span></span>

<span data-ttu-id="81275-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="81275-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="81275-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="81275-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="81275-106">**PathLenConstraint** 屬性會捕獲 path length 條件約束的值。</span><span class="sxs-lookup"><span data-stu-id="81275-106">The **PathLenConstraint** property retrieves the value of the path length constraint.</span></span>

## <a name="syntax"></a><span data-ttu-id="81275-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="81275-107">Syntax</span></span>


```VB
BasicConstraints.PathLenConstraint As Long
```



## <a name="property-value"></a><span data-ttu-id="81275-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="81275-108">Property value</span></span>

<span data-ttu-id="81275-109">路徑長度條件約束的值。</span><span class="sxs-lookup"><span data-stu-id="81275-109">Value of the path length constraint.</span></span>

## <a name="requirements"></a><span data-ttu-id="81275-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="81275-110">Requirements</span></span>



| <span data-ttu-id="81275-111">需求</span><span class="sxs-lookup"><span data-stu-id="81275-111">Requirement</span></span> | <span data-ttu-id="81275-112">值</span><span class="sxs-lookup"><span data-stu-id="81275-112">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="81275-113">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="81275-113">End of client support</span></span><br/> | <span data-ttu-id="81275-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81275-114">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="81275-115">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="81275-115">End of server support</span></span><br/> | <span data-ttu-id="81275-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81275-116">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="81275-117">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="81275-117">Redistributable</span></span><br/>       | <span data-ttu-id="81275-118">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="81275-118">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="81275-119">DLL</span><span class="sxs-lookup"><span data-stu-id="81275-119">DLL</span></span><br/>                   | <dl> <span data-ttu-id="81275-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81275-120"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
