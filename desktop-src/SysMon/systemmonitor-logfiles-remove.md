---
title: 記錄檔. Remove 方法
description: 從集合中移除指定的 LogFileItem 實例。
ms.assetid: d2885ffd-5957-472c-9a67-2f1469d9b48b
keywords:
- 移除方法 SysMon
- Remove 方法 SysMon，記錄檔類別
- 記錄檔類別 SysMon、移除方法
topic_type:
- apiref
api_name:
- LogFiles.Remove
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 057607c57db600ca7a28c8a5bb6d75d5570829cb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686266"
---
# <a name="logfilesremove-method"></a><span data-ttu-id="60437-106">記錄檔. Remove 方法</span><span class="sxs-lookup"><span data-stu-id="60437-106">LogFiles.Remove method</span></span>

<span data-ttu-id="60437-107">從集合中移除指定的 [**LogFileItem**](logfileitem.md) 實例。</span><span class="sxs-lookup"><span data-stu-id="60437-107">Removes the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="60437-108">語法</span><span class="sxs-lookup"><span data-stu-id="60437-108">Syntax</span></span>


```VB
LogFiles.Remove( _
  ByVal index As Object _
)
```



## <a name="parameters"></a><span data-ttu-id="60437-109">參數</span><span class="sxs-lookup"><span data-stu-id="60437-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60437-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60437-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60437-111">要從集合中移除之記錄檔的整數索引。</span><span class="sxs-lookup"><span data-stu-id="60437-111">Integer index of the log file to remove from the collection.</span></span> <span data-ttu-id="60437-112">索引是以一為基礎。</span><span class="sxs-lookup"><span data-stu-id="60437-112">The index is one-based.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60437-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="60437-113">Return value</span></span>

<span data-ttu-id="60437-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="60437-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="60437-115">備註</span><span class="sxs-lookup"><span data-stu-id="60437-115">Remarks</span></span>

<span data-ttu-id="60437-116">**在 Windows Vista 之前：** 如果 [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md)的值設定為 sysmonLogFiles，您就無法從 [**記錄檔集合**](systemmonitor-logfiles.md)中移除記錄檔。</span><span class="sxs-lookup"><span data-stu-id="60437-116">**Prior to Windows Vista:** You cannot remove log files from the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to sysmonLogFiles.</span></span>

## <a name="requirements"></a><span data-ttu-id="60437-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="60437-117">Requirements</span></span>



| <span data-ttu-id="60437-118">需求</span><span class="sxs-lookup"><span data-stu-id="60437-118">Requirement</span></span> | <span data-ttu-id="60437-119">值</span><span class="sxs-lookup"><span data-stu-id="60437-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60437-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60437-120">Minimum supported client</span></span><br/> | <span data-ttu-id="60437-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60437-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="60437-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60437-122">Minimum supported server</span></span><br/> | <span data-ttu-id="60437-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60437-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="60437-124">DLL</span><span class="sxs-lookup"><span data-stu-id="60437-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60437-125"><dt>Sysmon .ocx</dt></span><span class="sxs-lookup"><span data-stu-id="60437-125"><dt>Sysmon.ocx</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60437-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60437-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60437-127">LogFiles</span><span class="sxs-lookup"><span data-stu-id="60437-127">LogFiles</span></span>](logfiles.md)
</dt> <dt>

[<span data-ttu-id="60437-128">**LogFileItem**</span><span class="sxs-lookup"><span data-stu-id="60437-128">**LogFileItem**</span></span>](logfileitem.md)
</dt> <dt>

[<span data-ttu-id="60437-129">**LogFiles**</span><span class="sxs-lookup"><span data-stu-id="60437-129">**LogFiles**</span></span>](systemmonitor-logfiles.md)
</dt> </dl>

 

 





