---
description: 指定應用程式的健全狀況狀態。
ms.assetid: CA06AA34-A549-4CFC-9B52-D2E0B200C3E9
title: APPLICATION_STATE 列舉
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPLICATION_STATE
api_type:
- IDLDef
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 4b7e288f41c863dc3f0365db3c6aae867605e5c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982432"
---
# <a name="application_state-enumeration"></a><span data-ttu-id="6b05f-103">應用程式 \_ 狀態列舉</span><span class="sxs-lookup"><span data-stu-id="6b05f-103">APPLICATION\_STATE enumeration</span></span>

<span data-ttu-id="6b05f-104">指定應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="6b05f-104">Specifies the health state of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b05f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b05f-105">Syntax</span></span>


```C++
typedef enum _APPLICATION_STATE { 
  ApplicationStateHealthy   = 0,
  ApplicationStateCritical
} APPLICATION_STATE, *PAPPLICATION_STATE;
```



## <a name="constants"></a><span data-ttu-id="6b05f-106">常數</span><span class="sxs-lookup"><span data-stu-id="6b05f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6b05f-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span><span class="sxs-lookup"><span data-stu-id="6b05f-107"><span id="ApplicationStateHealthy"></span><span id="applicationstatehealthy"></span><span id="APPLICATIONSTATEHEALTHY"></span>**ApplicationStateHealthy**</span></span>
</dt> <dd>

<span data-ttu-id="6b05f-108">應用程式狀態為狀況良好。</span><span class="sxs-lookup"><span data-stu-id="6b05f-108">The application state is healthy.</span></span>

</dd> <dt>

<span data-ttu-id="6b05f-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span><span class="sxs-lookup"><span data-stu-id="6b05f-109"><span id="ApplicationStateCritical"></span><span id="applicationstatecritical"></span><span id="APPLICATIONSTATECRITICAL"></span>**ApplicationStateCritical**</span></span>
</dt> <dd>

<span data-ttu-id="6b05f-110">應用程式狀態為 [重大]。</span><span class="sxs-lookup"><span data-stu-id="6b05f-110">The application state is critical.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6b05f-111">備註</span><span class="sxs-lookup"><span data-stu-id="6b05f-111">Remarks</span></span>

<span data-ttu-id="6b05f-112">若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="6b05f-112">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b05f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6b05f-113">Requirements</span></span>



| <span data-ttu-id="6b05f-114">需求</span><span class="sxs-lookup"><span data-stu-id="6b05f-114">Requirement</span></span> | <span data-ttu-id="6b05f-115">值</span><span class="sxs-lookup"><span data-stu-id="6b05f-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b05f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6b05f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b05f-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b05f-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="6b05f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6b05f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b05f-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6b05f-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6b05f-120">版本</span><span class="sxs-lookup"><span data-stu-id="6b05f-120">Version</span></span><br/>                  | <span data-ttu-id="6b05f-121">Windows 8 的整合元件</span><span class="sxs-lookup"><span data-stu-id="6b05f-121">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="6b05f-122">Idl</span><span class="sxs-lookup"><span data-stu-id="6b05f-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6b05f-123"><dt>VmApplicationHealthMonitor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6b05f-123"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b05f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6b05f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b05f-125">**SetApplicationState**</span><span class="sxs-lookup"><span data-stu-id="6b05f-125">**SetApplicationState**</span></span>](ivmapplicationhealthmonitor-setapplicationstate.md)
</dt> </dl>

 

 




