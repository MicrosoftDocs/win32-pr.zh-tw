---
description: 此類別是硬體設定事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: SystemConfig_V0 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848857"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="6743e-104">SystemConfig \_ V0 類別</span><span class="sxs-lookup"><span data-stu-id="6743e-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="6743e-105">此類別是硬體設定事件的父類別。</span><span class="sxs-lookup"><span data-stu-id="6743e-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="6743e-106">以下是從 MOF 程式碼簡化的語法。</span><span class="sxs-lookup"><span data-stu-id="6743e-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="6743e-107">語法</span><span class="sxs-lookup"><span data-stu-id="6743e-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="6743e-108">成員</span><span class="sxs-lookup"><span data-stu-id="6743e-108">Members</span></span>

<span data-ttu-id="6743e-109">**SystemConfig \_ V0** 類別未定義任何成員。</span><span class="sxs-lookup"><span data-stu-id="6743e-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="6743e-110">備註</span><span class="sxs-lookup"><span data-stu-id="6743e-110">Remarks</span></span>

<span data-ttu-id="6743e-111">如需 Windows XP 上的硬體設定事件，請參閱 [**HWConfig**](hwconfig.md) 類別。</span><span class="sxs-lookup"><span data-stu-id="6743e-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="6743e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="6743e-112">Requirements</span></span>



| <span data-ttu-id="6743e-113">需求</span><span class="sxs-lookup"><span data-stu-id="6743e-113">Requirement</span></span> | <span data-ttu-id="6743e-114">值</span><span class="sxs-lookup"><span data-stu-id="6743e-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6743e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6743e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6743e-116">都不支援</span><span class="sxs-lookup"><span data-stu-id="6743e-116">None supported</span></span><br/>                            |
| <span data-ttu-id="6743e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6743e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6743e-118">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6743e-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6743e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6743e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6743e-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="6743e-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="6743e-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="6743e-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="6743e-122">**SystemConfig \_ V0 \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="6743e-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="6743e-123">**SystemConfig \_ V0 \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="6743e-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="6743e-124">**SystemConfig \_ V0 \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="6743e-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="6743e-125">**SystemConfig \_ V0 \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="6743e-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="6743e-126">**SystemConfig \_ V0 \_ 電源**</span><span class="sxs-lookup"><span data-stu-id="6743e-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="6743e-127">**SystemConfig \_ V0 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="6743e-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="6743e-128">**SystemConfig \_ V0 \_ 影片**</span><span class="sxs-lookup"><span data-stu-id="6743e-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




