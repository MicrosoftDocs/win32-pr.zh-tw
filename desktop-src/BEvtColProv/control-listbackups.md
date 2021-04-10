---
description: 傳回可以還原的已儲存備份配置檔案清單。
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Control 類別的 ListBackups 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110060"
---
# <a name="listbackups-method-of-the-control-class"></a><span data-ttu-id="4d5a6-103">Control 類別的 ListBackups 方法</span><span class="sxs-lookup"><span data-stu-id="4d5a6-103">ListBackups method of the Control class</span></span>

<span data-ttu-id="4d5a6-104">傳回可以還原的已儲存備份配置檔案清單。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-104">Returns the list of the saved backup configuration files that can be restored.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d5a6-105">語法</span><span class="sxs-lookup"><span data-stu-id="4d5a6-105">Syntax</span></span>


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a><span data-ttu-id="4d5a6-106">參數</span><span class="sxs-lookup"><span data-stu-id="4d5a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d5a6-107">*OriginalTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d5a6-107">*OriginalTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d5a6-108">目前設定的設定時間戳記 (如果從備份還原，將會包含原始的時間戳記) 。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-108">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="4d5a6-109">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-109">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4d5a6-110">*OriginalTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d5a6-110">*OriginalTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d5a6-111">目前設定的設定時間戳記 (如果從備份還原，將會包含原始的時間戳記) 。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-111">The timestamp of when the current configuration was set (if restored from backup, will contain the original timestamp).</span></span> <span data-ttu-id="4d5a6-112">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-112">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4d5a6-113">檔案 \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d5a6-113">*Files* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d5a6-114">可用備份檔案的清單，順序從最新到最舊。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-114">The list of available backup files, in order from the newest to the oldest.</span></span>

</dd> <dt>

<span data-ttu-id="4d5a6-115">*FilesTimestampLow* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d5a6-115">*FilesTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d5a6-116">針對每個備份檔案，設定其設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-116">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="4d5a6-117">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的低部分。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-117">This is the low part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> <dt>

<span data-ttu-id="4d5a6-118">*FilesTimestampHigh* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4d5a6-118">*FilesTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d5a6-119">針對每個備份檔案，設定其設定的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-119">For each backup file, the timestamp of when its configuration was set.</span></span> <span data-ttu-id="4d5a6-120">這是 [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)的高部分。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-120">This is the high part of [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d5a6-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d5a6-121">Return value</span></span>

<span data-ttu-id="4d5a6-122">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="4d5a6-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d5a6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d5a6-123">Requirements</span></span>



| <span data-ttu-id="4d5a6-124">需求</span><span class="sxs-lookup"><span data-stu-id="4d5a6-124">Requirement</span></span> | <span data-ttu-id="4d5a6-125">值</span><span class="sxs-lookup"><span data-stu-id="4d5a6-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d5a6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d5a6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4d5a6-127">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d5a6-127">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4d5a6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d5a6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4d5a6-129">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="4d5a6-129">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="4d5a6-130">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d5a6-130">Namespace</span></span><br/>                | <span data-ttu-id="4d5a6-131">根 \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="4d5a6-131">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="4d5a6-132">MOF</span><span class="sxs-lookup"><span data-stu-id="4d5a6-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d5a6-133"><dt>BootEventCollectorWMI mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d5a6-133"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d5a6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="4d5a6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d5a6-135"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d5a6-135"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="4d5a6-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d5a6-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d5a6-137">**控制**</span><span class="sxs-lookup"><span data-stu-id="4d5a6-137">**Control**</span></span>](control.md)
</dt> </dl>

 

