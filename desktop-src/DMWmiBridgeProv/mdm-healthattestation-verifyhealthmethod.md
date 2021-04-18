---
title: MDM_HealthAttestation 類別的 VerifyHealthMethod 方法
description: 通知裝置以準備健康情況憑證驗證要求的方法。 另請參閱 VerifyHealth。
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- VerifyHealthMethod 方法
- VerifyHealthMethod 方法，MDM_HealthAttestation 類別
- MDM_HealthAttestation 類別，VerifyHealthMethod 方法
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965078"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="cd88b-107">MDM HealthAttestation 類別的 VerifyHealthMethod 方法 \_</span><span class="sxs-lookup"><span data-stu-id="cd88b-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="cd88b-108">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="cd88b-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="cd88b-109">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="cd88b-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="cd88b-110">通知裝置以準備健康情況憑證驗證要求的方法。</span><span class="sxs-lookup"><span data-stu-id="cd88b-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="cd88b-111">另請參閱 [VerifyHealth](/windows/client-management/mdm/healthattestation-csp)。</span><span class="sxs-lookup"><span data-stu-id="cd88b-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd88b-112">語法</span><span class="sxs-lookup"><span data-stu-id="cd88b-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="cd88b-113">參數</span><span class="sxs-lookup"><span data-stu-id="cd88b-113">Parameters</span></span>

<span data-ttu-id="cd88b-114">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="cd88b-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd88b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd88b-115">Requirements</span></span>



| <span data-ttu-id="cd88b-116">需求</span><span class="sxs-lookup"><span data-stu-id="cd88b-116">Requirement</span></span> | <span data-ttu-id="cd88b-117">值</span><span class="sxs-lookup"><span data-stu-id="cd88b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd88b-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd88b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="cd88b-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd88b-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cd88b-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd88b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="cd88b-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="cd88b-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="cd88b-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="cd88b-122">Namespace</span></span><br/>                | <span data-ttu-id="cd88b-123">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="cd88b-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="cd88b-124">MOF</span><span class="sxs-lookup"><span data-stu-id="cd88b-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cd88b-125"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="cd88b-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="cd88b-126">DLL</span><span class="sxs-lookup"><span data-stu-id="cd88b-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd88b-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd88b-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd88b-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd88b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd88b-129">**MDM \_ HealthAttestation**</span><span class="sxs-lookup"><span data-stu-id="cd88b-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="cd88b-130">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="cd88b-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

