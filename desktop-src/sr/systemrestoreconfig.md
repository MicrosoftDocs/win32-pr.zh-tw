---
title: SystemRestoreConfig 類別
description: 提供屬性來控制排程的還原點建立頻率，以及每個磁片磁碟機上耗用的磁碟空間量。
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- SystemRestoreConfig 類別系統還原
- SystemRestoreConfig 類別系統還原，說明
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384845"
---
# <a name="systemrestoreconfig-class"></a><span data-ttu-id="306cd-105">SystemRestoreConfig 類別</span><span class="sxs-lookup"><span data-stu-id="306cd-105">SystemRestoreConfig class</span></span>

<span data-ttu-id="306cd-106">提供屬性來控制排程的還原點建立頻率，以及每個磁片磁碟機上耗用的磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="306cd-106">Provides properties for controlling the frequency of scheduled restore point creation and the amount of disk space consumed on each drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="306cd-107">語法</span><span class="sxs-lookup"><span data-stu-id="306cd-107">Syntax</span></span>

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a><span data-ttu-id="306cd-108">成員</span><span class="sxs-lookup"><span data-stu-id="306cd-108">Members</span></span>

<span data-ttu-id="306cd-109">**SystemRestoreConfig** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="306cd-109">The **SystemRestoreConfig** class has these types of members:</span></span>

-   [<span data-ttu-id="306cd-110">屬性</span><span class="sxs-lookup"><span data-stu-id="306cd-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="306cd-111">屬性</span><span class="sxs-lookup"><span data-stu-id="306cd-111">Properties</span></span>

<span data-ttu-id="306cd-112">**SystemRestoreConfig** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="306cd-112">The **SystemRestoreConfig** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="306cd-113">**DiskPercent**</span><span class="sxs-lookup"><span data-stu-id="306cd-113">**DiskPercent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="306cd-114">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="306cd-114">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="306cd-115">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="306cd-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="306cd-116">系統還原可使用的每個磁片磁碟機上的最大磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="306cd-116">The maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="306cd-117">此值會指定為總磁片磁碟機空間的百分比。</span><span class="sxs-lookup"><span data-stu-id="306cd-117">This value is specified as a percentage of the total drive space.</span></span> <span data-ttu-id="306cd-118">預設值為12%。</span><span class="sxs-lookup"><span data-stu-id="306cd-118">The default value is 12 percent.</span></span>

<span data-ttu-id="306cd-119">**Windows Vista：** 從磁碟區陰影複製服務 (VSS) 接收值。</span><span class="sxs-lookup"><span data-stu-id="306cd-119">**Windows Vista:** Receives a value from the Volume Shadow Copy Service (VSS).</span></span> <span data-ttu-id="306cd-120">這是系統還原可使用的每個磁片磁碟機上的最大磁碟空間量。</span><span class="sxs-lookup"><span data-stu-id="306cd-120">This this is the maximum amount of disk space on each drive that can be used by System Restore.</span></span> <span data-ttu-id="306cd-121">預設值是總磁片磁碟機空間的15% 或可用空間的百分之30，以較小者為准。</span><span class="sxs-lookup"><span data-stu-id="306cd-121">The default value is 15 percent of the total drive space or 30 percent of the available free space, whichever is smaller.</span></span>

</dd> <dt>

<span data-ttu-id="306cd-122">**RPGlobalInterval**</span><span class="sxs-lookup"><span data-stu-id="306cd-122">**RPGlobalInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="306cd-123">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="306cd-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="306cd-124">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="306cd-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="306cd-125">排程的系統檢查點建立的絕對時間間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="306cd-125">The absolute time interval at which scheduled system checkpoints are created, in seconds.</span></span> <span data-ttu-id="306cd-126">預設值為 86400 (24 小時) 。</span><span class="sxs-lookup"><span data-stu-id="306cd-126">The default value is 86,400 (24 hours).</span></span>

<span data-ttu-id="306cd-127">**Windows Vista：** 從工作排程器接收系統還原的值。</span><span class="sxs-lookup"><span data-stu-id="306cd-127">**Windows Vista:** Receives a value from the task scheduler for System Restore.</span></span> <span data-ttu-id="306cd-128">如果工作已停用，則為零。</span><span class="sxs-lookup"><span data-stu-id="306cd-128">Zero if the task is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="306cd-129">**RPLifeInterval**</span><span class="sxs-lookup"><span data-stu-id="306cd-129">**RPLifeInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="306cd-130">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="306cd-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="306cd-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="306cd-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="306cd-132">保留還原點的時間間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="306cd-132">The time interval for which restore points are preserved, in seconds.</span></span> <span data-ttu-id="306cd-133">當還原點變得超過此指定的間隔時，便會將其刪除。</span><span class="sxs-lookup"><span data-stu-id="306cd-133">When a restore point becomes older than this specified interval, it is deleted.</span></span> <span data-ttu-id="306cd-134">預設的存留期限制為90天。</span><span class="sxs-lookup"><span data-stu-id="306cd-134">The default age limit is 90 days.</span></span>

<span data-ttu-id="306cd-135">**Windows Vista：** 接收 **UINTMAX** 的值。</span><span class="sxs-lookup"><span data-stu-id="306cd-135">**Windows Vista:** Receives a value of **UINTMAX**.</span></span>

</dd> <dt>

<span data-ttu-id="306cd-136">**RPSessionInterval**</span><span class="sxs-lookup"><span data-stu-id="306cd-136">**RPSessionInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="306cd-137">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="306cd-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="306cd-138">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="306cd-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="306cd-139">在會話期間建立排程系統檢查點的時間間隔（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="306cd-139">The time interval at which scheduled system checkpoints are created during the session, in seconds.</span></span> <span data-ttu-id="306cd-140">預設值為零，表示此功能已關閉。</span><span class="sxs-lookup"><span data-stu-id="306cd-140">The default value is zero, indicating that the feature is turned off.</span></span>

<span data-ttu-id="306cd-141">**Windows Vista：** 如果系統還原已停用，則接收零。</span><span class="sxs-lookup"><span data-stu-id="306cd-141">**Windows Vista:** Receives zero if System Restore is disabled.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="306cd-142">範例</span><span class="sxs-lookup"><span data-stu-id="306cd-142">Examples</span></span>

<span data-ttu-id="306cd-143">不支援下列範例程式碼。</span><span class="sxs-lookup"><span data-stu-id="306cd-143">The following sample code is not supported.</span></span> <span data-ttu-id="306cd-144">使用命令列工具 Vssadmin.exe 來變更保留磁片磁碟機空間的大小。</span><span class="sxs-lookup"><span data-stu-id="306cd-144">Use the command-line tool Vssadmin.exe to change the size of reserved drive space.</span></span>

<span data-ttu-id="306cd-145">**WINDOWS XP：** 支援此範例。</span><span class="sxs-lookup"><span data-stu-id="306cd-145">**Windows XP:** This sample is supported.</span></span>


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a><span data-ttu-id="306cd-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="306cd-146">Requirements</span></span>



| <span data-ttu-id="306cd-147">需求</span><span class="sxs-lookup"><span data-stu-id="306cd-147">Requirement</span></span> | <span data-ttu-id="306cd-148">值</span><span class="sxs-lookup"><span data-stu-id="306cd-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="306cd-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="306cd-149">Minimum supported client</span></span><br/> | <span data-ttu-id="306cd-150">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="306cd-150">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="306cd-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="306cd-151">Minimum supported server</span></span><br/> | <span data-ttu-id="306cd-152">都不支援</span><span class="sxs-lookup"><span data-stu-id="306cd-152">None supported</span></span><br/>                                                         |
| <span data-ttu-id="306cd-153">命名空間</span><span class="sxs-lookup"><span data-stu-id="306cd-153">Namespace</span></span><br/>                | <span data-ttu-id="306cd-154">根 \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="306cd-154">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="306cd-155">MOF</span><span class="sxs-lookup"><span data-stu-id="306cd-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="306cd-156"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="306cd-156"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="306cd-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="306cd-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="306cd-158">還原點</span><span class="sxs-lookup"><span data-stu-id="306cd-158">Restore Points</span></span>](restore-points.md)
</dt> <dt>

[<span data-ttu-id="306cd-159">Windows Management Instrumentation</span><span class="sxs-lookup"><span data-stu-id="306cd-159">Windows Management Instrumentation</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

