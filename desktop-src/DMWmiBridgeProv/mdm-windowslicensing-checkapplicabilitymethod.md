---
title: MDM_WindowsLicensing 類別的 CheckApplicabilityMethod 方法
description: 檢查輸入的產品金鑰是否可用於版本升級、啟用或變更桌面裝置 Windows 10 的產品金鑰。 另請參閱 CheckApplicability。
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- CheckApplicabilityMethod 方法
- CheckApplicabilityMethod 方法，MDM_WindowsLicensing 類別
- MDM_WindowsLicensing 類別，CheckApplicabilityMethod 方法
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104940"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="229cf-107">MDM WindowsLicensing 類別的 CheckApplicabilityMethod 方法 \_</span><span class="sxs-lookup"><span data-stu-id="229cf-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="229cf-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="229cf-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="229cf-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="229cf-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="229cf-110">檢查輸入的產品金鑰是否可用於版本升級、啟用或變更桌面裝置 Windows 10 的產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="229cf-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="229cf-111">另請參閱 [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp)。</span><span class="sxs-lookup"><span data-stu-id="229cf-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="229cf-112">語法</span><span class="sxs-lookup"><span data-stu-id="229cf-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="229cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="229cf-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="229cf-114">*param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="229cf-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="229cf-115">產品金鑰。</span><span class="sxs-lookup"><span data-stu-id="229cf-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="229cf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="229cf-116">Return value</span></span>

<span data-ttu-id="229cf-117">TRUE 或 FALSE</span><span class="sxs-lookup"><span data-stu-id="229cf-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="229cf-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="229cf-118">Requirements</span></span>



| <span data-ttu-id="229cf-119">需求</span><span class="sxs-lookup"><span data-stu-id="229cf-119">Requirement</span></span> | <span data-ttu-id="229cf-120">值</span><span class="sxs-lookup"><span data-stu-id="229cf-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="229cf-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="229cf-121">Minimum supported client</span></span><br/> | <span data-ttu-id="229cf-122">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="229cf-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="229cf-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="229cf-123">Minimum supported server</span></span><br/> | <span data-ttu-id="229cf-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="229cf-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="229cf-125">命名空間</span><span class="sxs-lookup"><span data-stu-id="229cf-125">Namespace</span></span><br/>                | <span data-ttu-id="229cf-126">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="229cf-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="229cf-127">MOF</span><span class="sxs-lookup"><span data-stu-id="229cf-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="229cf-128"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="229cf-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="229cf-129">DLL</span><span class="sxs-lookup"><span data-stu-id="229cf-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="229cf-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="229cf-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="229cf-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="229cf-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="229cf-132">**MDM \_ WindowsLicensing**</span><span class="sxs-lookup"><span data-stu-id="229cf-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="229cf-133">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="229cf-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

