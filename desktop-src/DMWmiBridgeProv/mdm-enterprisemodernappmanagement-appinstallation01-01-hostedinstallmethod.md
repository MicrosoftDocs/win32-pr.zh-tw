---
title: MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別的 HostedInstallMethod 方法
description: 從託管位置（例如本機磁片磁碟機、UNC 或 HTTPS 資料來源）執行應用程式套件安裝的方法。 另請參閱 HostedInstall。
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- HostedInstallMethod 方法
- HostedInstallMethod 方法，MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別
- MDM_EnterpriseModernAppManagement_AppInstallation01_01 類別，HostedInstallMethod 方法
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968779"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="bb3b4-107">MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01 類別的 HostedInstallMethod 方法</span><span class="sxs-lookup"><span data-stu-id="bb3b4-107">HostedInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="bb3b4-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="bb3b4-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="bb3b4-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="bb3b4-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="bb3b4-110">從託管位置（例如本機磁片磁碟機、UNC 或 HTTPS 資料來源）執行應用程式套件安裝的方法。</span><span class="sxs-lookup"><span data-stu-id="bb3b4-110">Method to perform an install of an app package from a hosted location, such as a local drive, a UNC, or HTTPS data source.</span></span> <span data-ttu-id="bb3b4-111">另請參閱 [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp)。</span><span class="sxs-lookup"><span data-stu-id="bb3b4-111">See also, [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="bb3b4-112">語法</span><span class="sxs-lookup"><span data-stu-id="bb3b4-112">Syntax</span></span>


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="bb3b4-113">參數</span><span class="sxs-lookup"><span data-stu-id="bb3b4-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb3b4-114">*param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bb3b4-114">*param* \[in\]</span></span>
<span data-ttu-id="bb3b4-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="bb3b4-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="bb3b4-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb3b4-116">Requirements</span></span>



| <span data-ttu-id="bb3b4-117">需求</span><span class="sxs-lookup"><span data-stu-id="bb3b4-117">Requirement</span></span> | <span data-ttu-id="bb3b4-118">值</span><span class="sxs-lookup"><span data-stu-id="bb3b4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb3b4-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb3b4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bb3b4-120">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb3b4-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb3b4-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb3b4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bb3b4-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="bb3b4-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="bb3b4-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="bb3b4-123">Namespace</span></span><br/>                | <span data-ttu-id="bb3b4-124">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="bb3b4-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="bb3b4-125">MOF</span><span class="sxs-lookup"><span data-stu-id="bb3b4-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bb3b4-126"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="bb3b4-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="bb3b4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bb3b4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb3b4-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb3b4-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb3b4-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb3b4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb3b4-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="bb3b4-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="bb3b4-131">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="bb3b4-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

