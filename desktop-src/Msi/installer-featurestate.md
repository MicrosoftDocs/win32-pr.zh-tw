---
description: 唯讀 FeatureState 屬性會傳回功能的已安裝狀態。
ms.assetid: a3d30296-191e-4446-b5b1-a92f8991926a
title: FeatureState 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf6fe61899ea1daac37fd678e9f0e70dfcc3af69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000672"
---
# <a name="installerfeaturestate-property"></a><span data-ttu-id="05220-103">FeatureState 屬性</span><span class="sxs-lookup"><span data-stu-id="05220-103">Installer.FeatureState property</span></span>

<span data-ttu-id="05220-104">唯讀 **FeatureState** 屬性會傳回功能的已安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="05220-104">The read-only **FeatureState** property returns the installed state of a feature.</span></span>

<span data-ttu-id="05220-105">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="05220-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="05220-106">語法</span><span class="sxs-lookup"><span data-stu-id="05220-106">Syntax</span></span>


```JScript
propVal = Installer.FeatureState
```



## <a name="property-value"></a><span data-ttu-id="05220-107">屬性值</span><span class="sxs-lookup"><span data-stu-id="05220-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="05220-108">備註</span><span class="sxs-lookup"><span data-stu-id="05220-108">Remarks</span></span>

<span data-ttu-id="05220-109">這個屬性會傳回下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="05220-109">This property returns one of the following values.</span></span>



| <span data-ttu-id="05220-110">值</span><span class="sxs-lookup"><span data-stu-id="05220-110">Value</span></span>                     | <span data-ttu-id="05220-111">描述</span><span class="sxs-lookup"><span data-stu-id="05220-111">Description</span></span>                                      |
|---------------------------|--------------------------------------------------|
| <span data-ttu-id="05220-112">msiInstallStateAbsent</span><span class="sxs-lookup"><span data-stu-id="05220-112">msiInstallStateAbsent</span></span>     | <span data-ttu-id="05220-113">未安裝此功能。</span><span class="sxs-lookup"><span data-stu-id="05220-113">The feature is not installed.</span></span>                    |
| <span data-ttu-id="05220-114">msiInstallStateAdvertised</span><span class="sxs-lookup"><span data-stu-id="05220-114">msiInstallStateAdvertised</span></span> | <span data-ttu-id="05220-115">已公告此功能。</span><span class="sxs-lookup"><span data-stu-id="05220-115">The feature is advertised.</span></span>                       |
| <span data-ttu-id="05220-116">msiInstallStateLocal</span><span class="sxs-lookup"><span data-stu-id="05220-116">msiInstallStateLocal</span></span>      | <span data-ttu-id="05220-117">這項功能會安裝在本機執行。</span><span class="sxs-lookup"><span data-stu-id="05220-117">The feature is installed to run locally.</span></span>         |
| <span data-ttu-id="05220-118">msiInstallStateSource</span><span class="sxs-lookup"><span data-stu-id="05220-118">msiInstallStateSource</span></span>     | <span data-ttu-id="05220-119">這項功能已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="05220-119">The feature is installed to run from source.</span></span>     |
| <span data-ttu-id="05220-120">msiInstallStateInvalidArg</span><span class="sxs-lookup"><span data-stu-id="05220-120">msiInstallStateInvalidArg</span></span> | <span data-ttu-id="05220-121">傳遞給函數的參數無效。</span><span class="sxs-lookup"><span data-stu-id="05220-121">An invalid parameter was passed to the function.</span></span> |
| <span data-ttu-id="05220-122">msiInstallStateUnknown</span><span class="sxs-lookup"><span data-stu-id="05220-122">msiInstallStateUnknown</span></span>    | <span data-ttu-id="05220-123">產品代碼或功能識別碼未知。</span><span class="sxs-lookup"><span data-stu-id="05220-123">The product code or feature ID is unknown.</span></span>       |
| <span data-ttu-id="05220-124">msiInstallStateBadConfig</span><span class="sxs-lookup"><span data-stu-id="05220-124">msiInstallStateBadConfig</span></span>  | <span data-ttu-id="05220-125">設定資料已損毀。</span><span class="sxs-lookup"><span data-stu-id="05220-125">The configuration data is corrupt.</span></span>               |



 

 

<span data-ttu-id="05220-126">**FeatureState** 屬性不會驗證是否可存取此功能。</span><span class="sxs-lookup"><span data-stu-id="05220-126">The **FeatureState** property does not validate that the feature is accessible.</span></span>

## <a name="requirements"></a><span data-ttu-id="05220-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="05220-127">Requirements</span></span>



| <span data-ttu-id="05220-128">需求</span><span class="sxs-lookup"><span data-stu-id="05220-128">Requirement</span></span> | <span data-ttu-id="05220-129">值</span><span class="sxs-lookup"><span data-stu-id="05220-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05220-130">版本</span><span class="sxs-lookup"><span data-stu-id="05220-130">Version</span></span><br/> | <span data-ttu-id="05220-131">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="05220-131">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="05220-132">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="05220-132">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="05220-133">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="05220-133">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="05220-134">DLL</span><span class="sxs-lookup"><span data-stu-id="05220-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="05220-135"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05220-135"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="05220-136">IID</span><span class="sxs-lookup"><span data-stu-id="05220-136">IID</span></span><br/>     | <span data-ttu-id="05220-137">IID \_ IInstaller 定義為000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="05220-137">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="05220-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="05220-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05220-139">**MsiQueryFeatureState**</span><span class="sxs-lookup"><span data-stu-id="05220-139">**MsiQueryFeatureState**</span></span>](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea)
</dt> </dl>

 

 




