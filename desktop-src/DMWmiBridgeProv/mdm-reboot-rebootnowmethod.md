---
title: MDM_Reboot 類別的 RebootNowMethod 方法
description: 此方法會執行裝置的重新開機。
ms.assetid: b1bacad8-06db-4e56-9f3d-46c9a0036729
keywords:
- RebootNowMethod 方法
- RebootNowMethod 方法，MDM_Reboot 類別
- MDM_Reboot 類別，RebootNowMethod 方法
topic_type:
- apiref
api_name:
- MDM_Reboot.RebootNowMethod
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d35d297858588ade6655ea84876c6e75abd719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093911"
---
# <a name="rebootnowmethod-method-of-the-mdm_reboot-class"></a><span data-ttu-id="3e80a-106">MDM \_ 重新開機類別的 RebootNowMethod 方法</span><span class="sxs-lookup"><span data-stu-id="3e80a-106">RebootNowMethod method of the MDM\_Reboot class</span></span>

<span data-ttu-id="3e80a-107">\[某些資訊與預先發行的產品有關，在正式發行之前可能會經過大幅修改。</span><span class="sxs-lookup"><span data-stu-id="3e80a-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="3e80a-108">Microsoft 對此處提供的資訊，不做任何明確或隱含的瑕疵擔保。\]</span><span class="sxs-lookup"><span data-stu-id="3e80a-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="3e80a-109">此方法會執行裝置的重新開機。</span><span class="sxs-lookup"><span data-stu-id="3e80a-109">This method executes a reboot of the device.</span></span> <span data-ttu-id="3e80a-110">另請參閱 [RebootNow](/windows/client-management/mdm/reboot-csp)。</span><span class="sxs-lookup"><span data-stu-id="3e80a-110">See also, [RebootNow](/windows/client-management/mdm/reboot-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e80a-111">語法</span><span class="sxs-lookup"><span data-stu-id="3e80a-111">Syntax</span></span>


```mof
uint32 RebootNowMethod();
```



## <a name="parameters"></a><span data-ttu-id="3e80a-112">參數</span><span class="sxs-lookup"><span data-stu-id="3e80a-112">Parameters</span></span>

<span data-ttu-id="3e80a-113">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3e80a-113">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e80a-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="3e80a-114">Requirements</span></span>



| <span data-ttu-id="3e80a-115">需求</span><span class="sxs-lookup"><span data-stu-id="3e80a-115">Requirement</span></span> | <span data-ttu-id="3e80a-116">值</span><span class="sxs-lookup"><span data-stu-id="3e80a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e80a-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3e80a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e80a-118">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3e80a-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e80a-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3e80a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e80a-120">都不支援</span><span class="sxs-lookup"><span data-stu-id="3e80a-120">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="3e80a-121">命名空間</span><span class="sxs-lookup"><span data-stu-id="3e80a-121">Namespace</span></span><br/>                | <span data-ttu-id="3e80a-122">根 \\ cimv2 \\ mdm \\ dmmap</span><span class="sxs-lookup"><span data-stu-id="3e80a-122">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="3e80a-123">MOF</span><span class="sxs-lookup"><span data-stu-id="3e80a-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e80a-124"><dt>DMWmiBridgeProv1 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e80a-124"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="3e80a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e80a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e80a-126"><dt>Mof \\DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e80a-126"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e80a-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3e80a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e80a-128">**MDM \_ 重新開機**</span><span class="sxs-lookup"><span data-stu-id="3e80a-128">**MDM\_Reboot**</span></span>](mdm-reboot.md)
</dt> </dl>

 

