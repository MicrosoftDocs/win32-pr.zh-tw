---
title: MDM_RemoteWipe 類別的 doWipeMethod 方法
description: 觸發裝置以啟動遠端清除。
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- doWipeMethod 方法
- doWipeMethod 方法，MDM_RemoteWipe 類別
- MDM_RemoteWipe 類別，doWipeMethod 方法
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464353"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="dc43c-106">MDM RemoteWipe 類別的 doWipeMethod 方法 \_</span><span class="sxs-lookup"><span data-stu-id="dc43c-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="dc43c-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="dc43c-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dc43c-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="dc43c-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dc43c-109">觸發裝置以啟動遠端清除。</span><span class="sxs-lookup"><span data-stu-id="dc43c-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="dc43c-110">另請參閱 [doWipe](/windows/client-management/mdm/remotewipe-csp)。</span><span class="sxs-lookup"><span data-stu-id="dc43c-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc43c-111">語法</span><span class="sxs-lookup"><span data-stu-id="dc43c-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="dc43c-112">參數</span><span class="sxs-lookup"><span data-stu-id="dc43c-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc43c-113">*param* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dc43c-113">*param* \[in\]</span></span>
<span data-ttu-id="dc43c-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="dc43c-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="dc43c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="dc43c-115">Requirements</span></span>



| <span data-ttu-id="dc43c-116">需求</span><span class="sxs-lookup"><span data-stu-id="dc43c-116">Requirement</span></span> | <span data-ttu-id="dc43c-117">值</span><span class="sxs-lookup"><span data-stu-id="dc43c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc43c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dc43c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dc43c-119">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dc43c-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dc43c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dc43c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dc43c-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="dc43c-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dc43c-122">命名空間</span><span class="sxs-lookup"><span data-stu-id="dc43c-122">Namespace</span></span><br/>                | <span data-ttu-id="dc43c-123">根 \\ CIMv2 \\ MDM \\ DMMap</span><span class="sxs-lookup"><span data-stu-id="dc43c-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="dc43c-124">MOF</span><span class="sxs-lookup"><span data-stu-id="dc43c-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc43c-125"><dt>DMWmiBridgeProv mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc43c-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc43c-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dc43c-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc43c-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc43c-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc43c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dc43c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc43c-129">**MDM \_ RemoteWipe**</span><span class="sxs-lookup"><span data-stu-id="dc43c-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="dc43c-130">使用 PowerShell 指令碼搭配 WMI 橋接器提供者</span><span class="sxs-lookup"><span data-stu-id="dc43c-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

