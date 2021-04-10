---
title: 'VMDriveBusType 列舉 (VPCCOMInterfaces) '
description: 指定匯流排的類型。
ms.assetid: 7e0926f3-8218-49c9-8d3a-27214c111a77
keywords:
- VMDriveBusType 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMDriveBusType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c53b8da4b9c7a6943f083eec62a144dcfb5bd68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104267"
---
# <a name="vmdrivebustype-enumeration"></a><span data-ttu-id="fa288-104">VMDriveBusType 列舉</span><span class="sxs-lookup"><span data-stu-id="fa288-104">VMDriveBusType enumeration</span></span>

<span data-ttu-id="fa288-105">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="fa288-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="fa288-106">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="fa288-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="fa288-107">指定匯流排的類型。</span><span class="sxs-lookup"><span data-stu-id="fa288-107">Specifies the type of bus.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa288-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa288-108">Syntax</span></span>


```C++
typedef enum  { 
  vmDriveBusType_Invalid  = -1,
  vmDriveBusType_IDE      = 0,
  vmDriveBusType_SCSI     = 1
} VMDriveBusType;
```



## <a name="constants"></a><span data-ttu-id="fa288-109">常數</span><span class="sxs-lookup"><span data-stu-id="fa288-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="fa288-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="fa288-110"><span id="vmDriveBusType_Invalid"></span><span id="vmdrivebustype_invalid"></span><span id="VMDRIVEBUSTYPE_INVALID"></span>**vmDriveBusType\_Invalid**</span></span>
</dt> <dd>

<span data-ttu-id="fa288-111">沒有匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="fa288-111">No bus type.</span></span>

</dd> <dt>

<span data-ttu-id="fa288-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType \_ IDE**</span><span class="sxs-lookup"><span data-stu-id="fa288-112"><span id="vmDriveBusType_IDE"></span><span id="vmdrivebustype_ide"></span><span id="VMDRIVEBUSTYPE_IDE"></span>**vmDriveBusType\_IDE**</span></span>
</dt> <dd>

<span data-ttu-id="fa288-113">IDE 匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="fa288-113">IDE bus type.</span></span>

</dd> <dt>

<span data-ttu-id="fa288-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType \_ SCSI**</span><span class="sxs-lookup"><span data-stu-id="fa288-114"><span id="vmDriveBusType_SCSI"></span><span id="vmdrivebustype_scsi"></span><span id="VMDRIVEBUSTYPE_SCSI"></span>**vmDriveBusType\_SCSI**</span></span>
</dt> <dd>

<span data-ttu-id="fa288-115">SCSI 匯流排類型。</span><span class="sxs-lookup"><span data-stu-id="fa288-115">SCSI bus type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fa288-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="fa288-116">Requirements</span></span>



| <span data-ttu-id="fa288-117">需求</span><span class="sxs-lookup"><span data-stu-id="fa288-117">Requirement</span></span> | <span data-ttu-id="fa288-118">值</span><span class="sxs-lookup"><span data-stu-id="fa288-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fa288-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fa288-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fa288-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fa288-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fa288-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fa288-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fa288-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="fa288-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="fa288-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="fa288-123">End of client support</span></span><br/>    | <span data-ttu-id="fa288-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fa288-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="fa288-125">產品</span><span class="sxs-lookup"><span data-stu-id="fa288-125">Product</span></span><br/>                  | <span data-ttu-id="fa288-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="fa288-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="fa288-127">標頭</span><span class="sxs-lookup"><span data-stu-id="fa288-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fa288-128"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="fa288-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



 

