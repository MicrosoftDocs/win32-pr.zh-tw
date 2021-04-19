---
description: 設定在虛擬機器中執行之應用程式的健全狀況狀態。
ms.assetid: 012190CA-9CBF-47B6-9C5D-F75D73B0499B
title: IVmApplicationHealthMonitor：： SetApplicationState 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IVmApplicationHealthMonitor.SetApplicationState
api_type:
- COM
api_location:
- VmApplicationHealthMonitor.idl
ms.openlocfilehash: 8e6c64ecec827f6f75f382fbca7aadf8fc0c7dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989295"
---
# <a name="ivmapplicationhealthmonitorsetapplicationstate-method"></a><span data-ttu-id="20bb1-103">IVmApplicationHealthMonitor：： SetApplicationState 方法</span><span class="sxs-lookup"><span data-stu-id="20bb1-103">IVmApplicationHealthMonitor::SetApplicationState method</span></span>

<span data-ttu-id="20bb1-104">設定在虛擬機器中執行之應用程式的健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="20bb1-104">Sets the health state of an application that is running in a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="20bb1-105">語法</span><span class="sxs-lookup"><span data-stu-id="20bb1-105">Syntax</span></span>


```C++
HRESULT SetApplicationState(
  [in] BSTR              Id,
  [in] BSTR              Name,
  [in] APPLICATION_STATE State
);
```



## <a name="parameters"></a><span data-ttu-id="20bb1-106">參數</span><span class="sxs-lookup"><span data-stu-id="20bb1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20bb1-107"> \[ 中的識別碼\]</span><span class="sxs-lookup"><span data-stu-id="20bb1-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bb1-108">識別應用程式之 **GUID** 的 **BSTR** 標記法。</span><span class="sxs-lookup"><span data-stu-id="20bb1-108">A **BSTR** representation of the **GUID** that identifies the application.</span></span> <span data-ttu-id="20bb1-109">呼叫應用程式必須負責建立和維護其用於受監視應用程式的識別碼。</span><span class="sxs-lookup"><span data-stu-id="20bb1-109">It is the calling application's responsibility to create and maintain the identifiers it uses for the applications being monitored.</span></span>

</dd> <dt>

<span data-ttu-id="20bb1-110">*名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="20bb1-110">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bb1-111">應用程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="20bb1-111">The display name of the application.</span></span> <span data-ttu-id="20bb1-112">此名稱會用於狀態變更的參考事件記錄專案中。</span><span class="sxs-lookup"><span data-stu-id="20bb1-112">This name is used in an informational event log entry for the state change.</span></span>

</dd> <dt>

<span data-ttu-id="20bb1-113">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="20bb1-113">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20bb1-114">[**應用程式 \_ 狀態**](application-state.md)列舉值，這個值會指定應用程式的新健全狀況狀態。</span><span class="sxs-lookup"><span data-stu-id="20bb1-114">A value of the [**APPLICATION\_STATE**](application-state.md) enumeration that specifies the new health state of the application.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20bb1-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="20bb1-115">Return value</span></span>

<span data-ttu-id="20bb1-116">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="20bb1-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="20bb1-117">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="20bb1-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="20bb1-118">備註</span><span class="sxs-lookup"><span data-stu-id="20bb1-118">Remarks</span></span>

<span data-ttu-id="20bb1-119">在虛擬機器中執行之應用程式的狀態會反映在 \[ \] [**Msvm \_ HeartbeatComponent**](msvm-heartbeatcomponent.md)類別的 OperationalStatus 1 屬性值中。</span><span class="sxs-lookup"><span data-stu-id="20bb1-119">The state of the applications running in the virtual machine are reflected in the **OperationalStatus**\[1\] property value of the [**Msvm\_HeartbeatComponent**](msvm-heartbeatcomponent.md) class.</span></span>

<span data-ttu-id="20bb1-120">若要使用這個程式設計項目，Windows 8 的整合元件必須安裝在執行應用程式的虛擬機器上。</span><span class="sxs-lookup"><span data-stu-id="20bb1-120">To use this programming element, the Windows 8 integration components must be installed on the virtual machine that the application is running in.</span></span>

## <a name="requirements"></a><span data-ttu-id="20bb1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="20bb1-121">Requirements</span></span>



| <span data-ttu-id="20bb1-122">需求</span><span class="sxs-lookup"><span data-stu-id="20bb1-122">Requirement</span></span> | <span data-ttu-id="20bb1-123">值</span><span class="sxs-lookup"><span data-stu-id="20bb1-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20bb1-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="20bb1-124">Minimum supported client</span></span><br/> | <span data-ttu-id="20bb1-125">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20bb1-125">Windows 8 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="20bb1-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="20bb1-126">Minimum supported server</span></span><br/> | <span data-ttu-id="20bb1-127">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="20bb1-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="20bb1-128">版本</span><span class="sxs-lookup"><span data-stu-id="20bb1-128">Version</span></span><br/>                  | <span data-ttu-id="20bb1-129">Windows 8 的整合元件</span><span class="sxs-lookup"><span data-stu-id="20bb1-129">Integration components for Windows 8</span></span><br/>                                                           |
| <span data-ttu-id="20bb1-130">Idl</span><span class="sxs-lookup"><span data-stu-id="20bb1-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="20bb1-131"><dt>VmApplicationHealthMonitor .idl</dt></span><span class="sxs-lookup"><span data-stu-id="20bb1-131"><dt>VmApplicationHealthMonitor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="20bb1-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="20bb1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20bb1-133">**IVmApplicationHealthMonitor**</span><span class="sxs-lookup"><span data-stu-id="20bb1-133">**IVmApplicationHealthMonitor**</span></span>](ivmapplicationhealthmonitor.md)
</dt> </dl>

 

 




