---
title: MDM_EnterpriseModernAppManagement_AppManagement01 類別的 RemovePackageMethod 方法
description: 移除封裝的方法。 另請參閱 RemovePackage。
ms.assetid: 0f48fd9c-5a3f-48e5-a954-e937e79af049
keywords:
- RemovePackageMethod 方法
- RemovePackageMethod 方法，MDM_EnterpriseModernAppManagement_AppManagement01 類別
- MDM_EnterpriseModernAppManagement_AppManagement01 類別，RemovePackageMethod 方法
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.RemovePackageMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2cdeb2c1a8dfaebdde73e52b2910da180b638c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967556"
---
# <a name="removepackagemethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="b2b78-107">MDM \_ EnterpriseModernAppManagement AppManagement01 類別的 RemovePackageMethod \_ 方法</span><span class="sxs-lookup"><span data-stu-id="b2b78-107">RemovePackageMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="b2b78-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="b2b78-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="b2b78-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="b2b78-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="b2b78-110">移除封裝的方法。</span><span class="sxs-lookup"><span data-stu-id="b2b78-110">Method for removing packages.</span></span> <span data-ttu-id="b2b78-111">另請參閱 [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp)。</span><span class="sxs-lookup"><span data-stu-id="b2b78-111">See also [RemovePackage](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b78-112">語法</span><span class="sxs-lookup"><span data-stu-id="b2b78-112">Syntax</span></span>


```mof
uint32 RemovePackageMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="b2b78-113">參數</span><span class="sxs-lookup"><span data-stu-id="b2b78-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b78-114">*param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2b78-114">*param* \[in\]</span></span>
<span data-ttu-id="b2b78-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="b2b78-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="b2b78-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2b78-116">Requirements</span></span>



| <span data-ttu-id="b2b78-117">需求</span><span class="sxs-lookup"><span data-stu-id="b2b78-117">Requirement</span></span> | <span data-ttu-id="b2b78-118">值</span><span class="sxs-lookup"><span data-stu-id="b2b78-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b78-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b2b78-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b78-120">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b2b78-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2b78-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b2b78-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b78-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="b2b78-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="b2b78-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="b2b78-123">Namespace</span></span><br/>                | <span data-ttu-id="b2b78-124">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="b2b78-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="b2b78-125">MOF</span><span class="sxs-lookup"><span data-stu-id="b2b78-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2b78-126"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2b78-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2b78-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b2b78-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b78-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2b78-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2b78-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2b78-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2b78-130">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01**</span><span class="sxs-lookup"><span data-stu-id="b2b78-130">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> </dl>

 

