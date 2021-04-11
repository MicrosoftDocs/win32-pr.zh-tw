---
description: 重設虛擬機器中所有應用程式的健全狀況狀態。
ms.assetid: DB0B2FB3-87EB-44B2-9C4E-849BCE594E89
title: IVmApplicationHealthMonitor：： ResetAllApplicationState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.ResetAllApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: b13781d26c256e41ea6685b19a3097236ebbdb91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848515"
---
# <a name="ivmapplicationhealthmonitorresetallapplicationstate-method"></a><span data-ttu-id="6f1e8-103">IVmApplicationHealthMonitor：： ResetAllApplicationState 方法</span><span class="sxs-lookup"><span data-stu-id="6f1e8-103">IVmApplicationHealthMonitor::ResetAllApplicationState method</span></span>

<span data-ttu-id="6f1e8-104">重設虛擬機器中所有應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="6f1e8-104">Resets the health state for all applications in a virtual machine.</span></span> <span data-ttu-id="6f1e8-105">如果成功，所有受監視應用程式的健全狀況狀態將會設定為 **ApplicationStateHealthy**。</span><span class="sxs-lookup"><span data-stu-id="6f1e8-105">If successful, the health state for all monitored applications will be set to **ApplicationStateHealthy**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f1e8-106">語法</span><span class="sxs-lookup"><span data-stu-id="6f1e8-106">Syntax</span></span>


```C++
HRESULT ResetAllApplicationState();
```



## <a name="parameters"></a><span data-ttu-id="6f1e8-107">參數</span><span class="sxs-lookup"><span data-stu-id="6f1e8-107">Parameters</span></span>

<span data-ttu-id="6f1e8-108">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6f1e8-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6f1e8-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6f1e8-109">Return value</span></span>

<span data-ttu-id="6f1e8-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6f1e8-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6f1e8-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="6f1e8-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f1e8-112">備註</span><span class="sxs-lookup"><span data-stu-id="6f1e8-112">Remarks</span></span>

<span data-ttu-id="6f1e8-113">若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="6f1e8-113">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f1e8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6f1e8-114">Requirements</span></span>



| <span data-ttu-id="6f1e8-115">需求</span><span class="sxs-lookup"><span data-stu-id="6f1e8-115">Requirement</span></span> | <span data-ttu-id="6f1e8-116">值</span><span class="sxs-lookup"><span data-stu-id="6f1e8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f1e8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6f1e8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6f1e8-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f1e8-118">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="6f1e8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6f1e8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6f1e8-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6f1e8-120">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6f1e8-121">版本</span><span class="sxs-lookup"><span data-stu-id="6f1e8-121">Version</span></span><br/>                  | <span data-ttu-id="6f1e8-122">Windows 8 的整合元件</span><span class="sxs-lookup"><span data-stu-id="6f1e8-122">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="6f1e8-123">Idl</span><span class="sxs-lookup"><span data-stu-id="6f1e8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6f1e8-124"><dt>VmApplicationHealthMonitor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="6f1e8-124"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f1e8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6f1e8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f1e8-126">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="6f1e8-126">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




