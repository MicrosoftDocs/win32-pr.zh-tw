---
description: ComponentPath 屬性是唯讀屬性，會傳回已安裝元件的完整路徑。 如果元件的金鑰路徑是登錄機碼，則會傳回登錄機碼。
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: ComponentPath 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989643"
---
# <a name="installercomponentpath-property"></a><span data-ttu-id="c389d-104">ComponentPath 屬性</span><span class="sxs-lookup"><span data-stu-id="c389d-104">Installer.ComponentPath property</span></span>

<span data-ttu-id="c389d-105">**ComponentPath** 屬性是唯讀屬性，會傳回已安裝元件的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="c389d-105">The **ComponentPath** property is a read-only property that returns the full path to an installed component.</span></span> <span data-ttu-id="c389d-106">如果元件的金鑰路徑是登錄機碼，則會傳回登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="c389d-106">If the key path for the component is a registry key then the registry key is returned.</span></span>

<span data-ttu-id="c389d-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="c389d-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c389d-108">語法</span><span class="sxs-lookup"><span data-stu-id="c389d-108">Syntax</span></span>


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a><span data-ttu-id="c389d-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="c389d-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c389d-110">備註</span><span class="sxs-lookup"><span data-stu-id="c389d-110">Remarks</span></span>

<span data-ttu-id="c389d-111">如果元件是登錄機碼，則會以數位表示登錄根目錄。</span><span class="sxs-lookup"><span data-stu-id="c389d-111">If the component is a registry key, the registry roots are represented numerically.</span></span> <span data-ttu-id="c389d-112">例如，"HKEY \_ CURRENT \_ USER SOFTWARE microsoft" 的登錄路徑會 \\ \\ 以 "01： \\ SOFTWARE \\ microsoft" 傳回。</span><span class="sxs-lookup"><span data-stu-id="c389d-112">For example, a registry path of "HKEY\_CURRENT\_USER\\SOFTWARE\\Microsoft" would be returned as "01:\\SOFTWARE\\Microsoft".</span></span> <span data-ttu-id="c389d-113">傳回的登錄根目錄定義如下：</span><span class="sxs-lookup"><span data-stu-id="c389d-113">The registry roots returned are defined as follows:</span></span>



| <span data-ttu-id="c389d-114">Root</span><span class="sxs-lookup"><span data-stu-id="c389d-114">Root</span></span>                    | <span data-ttu-id="c389d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="c389d-115">Returned value</span></span> |
|-------------------------|----------------|
| <span data-ttu-id="c389d-116">HKEY \_ 類別 \_ 根目錄</span><span class="sxs-lookup"><span data-stu-id="c389d-116">HKEY\_CLASSES\_ROOT</span></span>     | <span data-ttu-id="c389d-117">00</span><span class="sxs-lookup"><span data-stu-id="c389d-117">00</span></span>             |
| <span data-ttu-id="c389d-118">HKEY \_ 目前的 \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="c389d-118">HKEY\_CURRENT\_USER</span></span>     | <span data-ttu-id="c389d-119">01</span><span class="sxs-lookup"><span data-stu-id="c389d-119">01</span></span>             |
| <span data-ttu-id="c389d-120">HKEY \_ 本機 \_ 電腦</span><span class="sxs-lookup"><span data-stu-id="c389d-120">HKEY\_LOCAL\_MACHINE</span></span>    | <span data-ttu-id="c389d-121">02</span><span class="sxs-lookup"><span data-stu-id="c389d-121">02</span></span>             |
| <span data-ttu-id="c389d-122">HKEY \_ 使用者</span><span class="sxs-lookup"><span data-stu-id="c389d-122">HKEY\_USERS</span></span>             | <span data-ttu-id="c389d-123">03</span><span class="sxs-lookup"><span data-stu-id="c389d-123">03</span></span>             |
| <span data-ttu-id="c389d-124">HKEY \_ 效能 \_ 資料</span><span class="sxs-lookup"><span data-stu-id="c389d-124">HKEY\_PERFORMANCE\_DATA</span></span> | <span data-ttu-id="c389d-125">04</span><span class="sxs-lookup"><span data-stu-id="c389d-125">04</span></span>             |



 

## <a name="requirements"></a><span data-ttu-id="c389d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="c389d-126">Requirements</span></span>



| <span data-ttu-id="c389d-127">需求</span><span class="sxs-lookup"><span data-stu-id="c389d-127">Requirement</span></span> | <span data-ttu-id="c389d-128">值</span><span class="sxs-lookup"><span data-stu-id="c389d-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c389d-129">版本</span><span class="sxs-lookup"><span data-stu-id="c389d-129">Version</span></span><br/> | <span data-ttu-id="c389d-130">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="c389d-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c389d-131">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="c389d-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c389d-132">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="c389d-132">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c389d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="c389d-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="c389d-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c389d-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c389d-135">IID</span><span class="sxs-lookup"><span data-stu-id="c389d-135">IID</span></span><br/>     | <span data-ttu-id="c389d-136">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c389d-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="c389d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c389d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c389d-138">**MsiGetComponentPath**</span><span class="sxs-lookup"><span data-stu-id="c389d-138">**MsiGetComponentPath**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




