---
title: MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別的 GetLicenseFromStoreMethod 方法
description: 從存放區取得授權的方法。 另請參閱 GetLicenseFromStore。
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- GetLicenseFromStoreMethod 方法
- GetLicenseFromStoreMethod 方法，MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01 類別，GetLicenseFromStoreMethod 方法
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104975"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="dcb2d-107">MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01 類別的 GetLicenseFromStoreMethod 方法</span><span class="sxs-lookup"><span data-stu-id="dcb2d-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="dcb2d-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="dcb2d-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dcb2d-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="dcb2d-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dcb2d-110">從存放區取得授權的方法。</span><span class="sxs-lookup"><span data-stu-id="dcb2d-110">Method for getting a license from the store.</span></span> <span data-ttu-id="dcb2d-111">另請參閱 [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp)。</span><span class="sxs-lookup"><span data-stu-id="dcb2d-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="dcb2d-112">語法</span><span class="sxs-lookup"><span data-stu-id="dcb2d-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="dcb2d-113">參數</span><span class="sxs-lookup"><span data-stu-id="dcb2d-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcb2d-114">*param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dcb2d-114">*param* \[in\]</span></span>
<span data-ttu-id="dcb2d-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dcb2d-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dcb2d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="dcb2d-116">Requirements</span></span>



| <span data-ttu-id="dcb2d-117">需求</span><span class="sxs-lookup"><span data-stu-id="dcb2d-117">Requirement</span></span> | <span data-ttu-id="dcb2d-118">值</span><span class="sxs-lookup"><span data-stu-id="dcb2d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcb2d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dcb2d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="dcb2d-120">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dcb2d-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dcb2d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dcb2d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="dcb2d-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="dcb2d-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dcb2d-123">命名空間</span><span class="sxs-lookup"><span data-stu-id="dcb2d-123">Namespace</span></span><br/>                | <span data-ttu-id="dcb2d-124">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="dcb2d-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dcb2d-125">MOF</span><span class="sxs-lookup"><span data-stu-id="dcb2d-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcb2d-126"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2d-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcb2d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="dcb2d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcb2d-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcb2d-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcb2d-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dcb2d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcb2d-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="dcb2d-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="dcb2d-131">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="dcb2d-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

