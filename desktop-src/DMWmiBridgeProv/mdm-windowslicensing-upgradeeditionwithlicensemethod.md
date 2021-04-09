---
title: MDM_WindowsLicensing 類別的 UpgradeEditionWithLicenseMethod 方法
description: 為 Windows 10 行動裝置的版本升級提供授權的方法。 另請參閱 UpgradeEditionWithLicense。
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- UpgradeEditionWithLicenseMethod 方法
- UpgradeEditionWithLicenseMethod 方法，MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，UpgradeEditionWithLicenseMethod 方法
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934763"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="7a0be-107">MDM WindowsLicensing 類別的 UpgradeEditionWithLicenseMethod 方法 \_</span><span class="sxs-lookup"><span data-stu-id="7a0be-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="7a0be-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="7a0be-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7a0be-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="7a0be-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7a0be-110">為 Windows 10 行動裝置的版本升級提供授權的方法。</span><span class="sxs-lookup"><span data-stu-id="7a0be-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="7a0be-111">另請參閱 [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp)。</span><span class="sxs-lookup"><span data-stu-id="7a0be-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a0be-112">語法</span><span class="sxs-lookup"><span data-stu-id="7a0be-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7a0be-113">參數</span><span class="sxs-lookup"><span data-stu-id="7a0be-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a0be-114">*param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7a0be-114">*param* \[in\]</span></span>
<span data-ttu-id="7a0be-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7a0be-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7a0be-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="7a0be-116">Requirements</span></span>



| <span data-ttu-id="7a0be-117">需求</span><span class="sxs-lookup"><span data-stu-id="7a0be-117">Requirement</span></span> | <span data-ttu-id="7a0be-118">值</span><span class="sxs-lookup"><span data-stu-id="7a0be-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7a0be-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7a0be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7a0be-120">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7a0be-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7a0be-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7a0be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7a0be-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="7a0be-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7a0be-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="7a0be-123">Namespace</span></span><br/>                | <span data-ttu-id="7a0be-124">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="7a0be-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7a0be-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7a0be-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a0be-126"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="7a0be-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a0be-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7a0be-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a0be-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a0be-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a0be-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7a0be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0be-130">**MDM \_ WindowsLicensing**</span><span class="sxs-lookup"><span data-stu-id="7a0be-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="7a0be-131">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="7a0be-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

