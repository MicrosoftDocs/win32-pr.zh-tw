---
title: MDM_EnterpriseModernAppManagement_AppManagement01 類別的 UpdateScanMethod 方法
description: 開始 Windows Update 掃描的方法。 另請參閱 UpdateScan。
ms.assetid: 61d17072-0fe5-4d5b-8e9e-fed536883ac9
keywords:
- UpdateScanMethod 方法
- UpdateScanMethod 方法，MDM_EnterpriseModernAppManagement_AppManagement01 類別
- MDM_EnterpriseModernAppManagement_AppManagement01 類別，UpdateScanMethod 方法
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.UpdateScanMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6cb5b744243b78f737ea44fbc27ef40708c6f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967555"
---
# <a name="updatescanmethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="04479-107">MDM \_ EnterpriseModernAppManagement AppManagement01 類別的 UpdateScanMethod \_ 方法</span><span class="sxs-lookup"><span data-stu-id="04479-107">UpdateScanMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="04479-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="04479-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="04479-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="04479-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="04479-110">開始 Windows Update 掃描的方法。</span><span class="sxs-lookup"><span data-stu-id="04479-110">Method for starting the Windows Update scan.</span></span> <span data-ttu-id="04479-111">另請參閱 [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp)。</span><span class="sxs-lookup"><span data-stu-id="04479-111">See also, [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="04479-112">語法</span><span class="sxs-lookup"><span data-stu-id="04479-112">Syntax</span></span>


```mof
uint32 UpdateScanMethod();
```



## <a name="parameters"></a><span data-ttu-id="04479-113">參數</span><span class="sxs-lookup"><span data-stu-id="04479-113">Parameters</span></span>

<span data-ttu-id="04479-114">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="04479-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="04479-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="04479-115">Requirements</span></span>



| <span data-ttu-id="04479-116">需求</span><span class="sxs-lookup"><span data-stu-id="04479-116">Requirement</span></span> | <span data-ttu-id="04479-117">值</span><span class="sxs-lookup"><span data-stu-id="04479-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04479-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="04479-118">Minimum supported client</span></span><br/> | <span data-ttu-id="04479-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="04479-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="04479-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="04479-120">Minimum supported server</span></span><br/> | <span data-ttu-id="04479-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="04479-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="04479-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="04479-122">Namespace</span></span><br/>                | <span data-ttu-id="04479-123">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="04479-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="04479-124">MOF</span><span class="sxs-lookup"><span data-stu-id="04479-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="04479-125"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="04479-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="04479-126">DLL</span><span class="sxs-lookup"><span data-stu-id="04479-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="04479-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="04479-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04479-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="04479-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04479-129">**MDM \_ EnterpriseModernAppManagement \_ AppManagement01**</span><span class="sxs-lookup"><span data-stu-id="04479-129">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> <dt>

[<span data-ttu-id="04479-130">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="04479-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

