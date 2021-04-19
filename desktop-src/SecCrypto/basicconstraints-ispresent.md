---
description: 抓取布林值，這個值會指出基本條件約束延伸是否存在。 這是預設屬性。
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints. IsPresent 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9632f0d1297f2effd7d1bcc6056b2327d7f38e26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992905"
---
# <a name="basicconstraintsispresent-property"></a><span data-ttu-id="8f6f4-104">BasicConstraints. IsPresent 屬性</span><span class="sxs-lookup"><span data-stu-id="8f6f4-104">BasicConstraints.IsPresent property</span></span>

<span data-ttu-id="8f6f4-105">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="8f6f4-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="8f6f4-106">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="8f6f4-106">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="8f6f4-107">**IsPresent** 屬性會抓取布林值，指出基本條件約束延伸是否存在。</span><span class="sxs-lookup"><span data-stu-id="8f6f4-107">The **IsPresent** property retrieves a Boolean value that indicates whether the basic constraints extension is present.</span></span> <span data-ttu-id="8f6f4-108">這是預設屬性。</span><span class="sxs-lookup"><span data-stu-id="8f6f4-108">This is the default property.</span></span>

<span data-ttu-id="8f6f4-109">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8f6f4-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f6f4-110">語法</span><span class="sxs-lookup"><span data-stu-id="8f6f4-110">Syntax</span></span>


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a><span data-ttu-id="8f6f4-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="8f6f4-111">Property value</span></span>

<span data-ttu-id="8f6f4-112">若 **為 true**，則會出現基本限制延伸。</span><span class="sxs-lookup"><span data-stu-id="8f6f4-112">If **true**, the basic constraints extension is present.</span></span>

## <a name="requirements"></a><span data-ttu-id="8f6f4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f6f4-113">Requirements</span></span>



| <span data-ttu-id="8f6f4-114">需求</span><span class="sxs-lookup"><span data-stu-id="8f6f4-114">Requirement</span></span> | <span data-ttu-id="8f6f4-115">值</span><span class="sxs-lookup"><span data-stu-id="8f6f4-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f6f4-116">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8f6f4-116">End of client support</span></span><br/> | <span data-ttu-id="8f6f4-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f6f4-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8f6f4-118">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="8f6f4-118">End of server support</span></span><br/> | <span data-ttu-id="8f6f4-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f6f4-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8f6f4-120">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8f6f4-120">Redistributable</span></span><br/>       | <span data-ttu-id="8f6f4-121">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8f6f4-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="8f6f4-122">DLL</span><span class="sxs-lookup"><span data-stu-id="8f6f4-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="8f6f4-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f6f4-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f6f4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f6f4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f6f4-125">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="8f6f4-125">**BasicConstraints**</span></span>](basicconstraints.md)
</dt> </dl>

 

 
