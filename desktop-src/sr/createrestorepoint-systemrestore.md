---
title: SystemRestore 類別的 CreateRestorePoint 方法
description: 建立還原點。
ms.assetid: 30e1ff03-816c-463f-9f80-6d84149f0e0b
keywords:
- CreateRestorePoint 方法系統還原
- CreateRestorePoint 方法系統還原，SystemRestore 類別
- SystemRestore 類別系統還原，CreateRestorePoint 方法
topic_type:
- apiref
api_name:
- SystemRestore.CreateRestorePoint
api_location:
- Root\Default
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1cae9e78d1845f628d62dc46362f1bc2bd8a37e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465593"
---
# <a name="createrestorepoint-method-of-the-systemrestore-class"></a><span data-ttu-id="a8f9e-106">SystemRestore 類別的 CreateRestorePoint 方法</span><span class="sxs-lookup"><span data-stu-id="a8f9e-106">CreateRestorePoint method of the SystemRestore class</span></span>

<span data-ttu-id="a8f9e-107">建立還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-107">Creates a restore point.</span></span>

<span data-ttu-id="a8f9e-108">這個方法是可編寫腳本的 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 函式對等專案。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-108">This method is the scriptable equivalent of the [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f9e-109">語法</span><span class="sxs-lookup"><span data-stu-id="a8f9e-109">Syntax</span></span>


```mof
uint32 CreateRestorePoint(
  [in] String Description,
  [in] uint32 RestorePointType,
  [in] uint32 EventType
);
```



## <a name="parameters"></a><span data-ttu-id="a8f9e-110">參數</span><span class="sxs-lookup"><span data-stu-id="a8f9e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f9e-111">*描述* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8f9e-111">*Description* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f9e-112">要顯示的描述，讓使用者可以輕鬆地識別還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-112">The description to be displayed so the user can easily identify a restore point.</span></span> <span data-ttu-id="a8f9e-113">ANSI 字串的最大長度為最大 \_ DESC。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-113">The maximum length of an ANSI string is MAX\_DESC.</span></span> <span data-ttu-id="a8f9e-114">Unicode 字串的最大長度為最大 \_ DESC \_ W。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-114">The maximum length of a Unicode string is MAX\_DESC\_W.</span></span> <span data-ttu-id="a8f9e-115">如需詳細資訊，請參閱 [還原點描述文字](restore-point-description-text.md)。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-115">For more information, see [Restore Point Description Text](restore-point-description-text.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8f9e-116">*RestorePointType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a8f9e-116">*RestorePointType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f9e-117">還原點的類型。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-117">The type of restore point.</span></span> <span data-ttu-id="a8f9e-118">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-118">This member can be one of the following values.</span></span>



| <span data-ttu-id="a8f9e-119">還原點類型</span><span class="sxs-lookup"><span data-stu-id="a8f9e-119">Restore point type</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="a8f9e-120">意義</span><span class="sxs-lookup"><span data-stu-id="a8f9e-120">Meaning</span></span>                                                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APPLICATION_INSTALL"></span><span id="application_install"></span><dl> <span data-ttu-id="a8f9e-121"><dt>**應用程式 \_安裝**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-121"><dt>**APPLICATION\_INSTALL**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="a8f9e-122">已安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-122">An application has been installed.</span></span><br/>                                                                                                                |
| <span id="APPLICATION_UNINSTALL"></span><span id="application_uninstall"></span><dl> <span data-ttu-id="a8f9e-123"><dt>**應用程式 \_卸載**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-123"><dt>**APPLICATION\_UNINSTALL**</dt> <dt>1</dt></span></span> </dl>   | <span data-ttu-id="a8f9e-124">已卸載應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-124">An application has been uninstalled.</span></span><br/>                                                                                                              |
| <span id="DEVICE_DRIVER_INSTALL"></span><span id="device_driver_install"></span><dl> <span data-ttu-id="a8f9e-125"><dt>**裝置 \_驅動程式 \_ 安裝**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-125"><dt>**DEVICE\_DRIVER\_INSTALL**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="a8f9e-126">已安裝設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-126">A device driver has been installed.</span></span><br/>                                                                                                               |
| <span id="MODIFY_SETTINGS"></span><span id="modify_settings"></span><dl> <span data-ttu-id="a8f9e-127"><dt>**修改 \_設定**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-127"><dt>**MODIFY\_SETTINGS**</dt> <dt>12</dt></span></span> </dl>                    | <span data-ttu-id="a8f9e-128">應用程式已新增或移除功能。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-128">An application has had features added or removed.</span></span><br/>                                                                                                 |
| <span id="CANCELLED_OPERATION"></span><span id="cancelled_operation"></span><dl> <span data-ttu-id="a8f9e-129">已 <dt>**取消 \_操作**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-129"><dt>**CANCELLED\_OPERATION**</dt> <dt>13</dt></span></span> </dl>        | <span data-ttu-id="a8f9e-130">應用程式必須刪除它所建立的還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-130">An application needs to delete the restore point it created.</span></span> <span data-ttu-id="a8f9e-131">例如，當使用者取消安裝時，應用程式會使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-131">For example, an application would use this flag when a user cancels an installation.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a8f9e-132">*事件* \[ 的在\]</span><span class="sxs-lookup"><span data-stu-id="a8f9e-132">*EventType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f9e-133">事件的類型。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-133">The type of event.</span></span> <span data-ttu-id="a8f9e-134">這個成員可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-134">This member can be one of the following values.</span></span>



| <span data-ttu-id="a8f9e-135">事件類型</span><span class="sxs-lookup"><span data-stu-id="a8f9e-135">Event type</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="a8f9e-136">意義</span><span class="sxs-lookup"><span data-stu-id="a8f9e-136">Meaning</span></span>                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BEGIN_NESTED_SYSTEM_CHANGE"></span><span id="begin_nested_system_change"></span><dl> <span data-ttu-id="a8f9e-137"><dt>**開始 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>102</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-137"><dt>**BEGIN\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>102</dt></span></span> </dl> | <span data-ttu-id="a8f9e-138">系統變更已開始。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-138">A system change has begun.</span></span> <span data-ttu-id="a8f9e-139">後續的嵌套呼叫不會建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-139">A subsequent nested call does not create a new restore point.</span></span> <br/> <span data-ttu-id="a8f9e-140">後續呼叫必須使用 END \_ NESTED \_ 系統 \_ 變更，而不是終端 \_ 系統 \_ 變更。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-140">Subsequent calls must use END\_NESTED\_SYSTEM\_CHANGE, not END\_SYSTEM\_CHANGE.</span></span><br/> |
| <span id="BEGIN_SYSTEM_CHANGE"></span><span id="begin_system_change"></span><dl> <span data-ttu-id="a8f9e-141"><dt>**開始 \_系統 \_ 變更**</dt> <dt>100</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-141"><dt>**BEGIN\_SYSTEM\_CHANGE**</dt> <dt>100</dt></span></span> </dl>                       | <span data-ttu-id="a8f9e-142">系統變更已開始。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-142">A system change has begun.</span></span> <br/> <span data-ttu-id="a8f9e-143">後續呼叫必須使用終端 \_ 系統 \_ 變更，而不是結束的 \_ 嵌套 \_ 系統 \_ 變更。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-143">A subsequent call must use END\_SYSTEM\_CHANGE, not END\_NESTED\_SYSTEM\_CHANGE.</span></span><br/>                                                              |
| <span id="END_NESTED_SYSTEM_CHANGE"></span><span id="end_nested_system_change"></span><dl> <span data-ttu-id="a8f9e-144"><dt>**結束 \_嵌套 \_ 系統 \_ 變更**</dt> <dt>103</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-144"><dt>**END\_NESTED\_SYSTEM\_CHANGE**</dt> <dt>103</dt></span></span> </dl>       | <span data-ttu-id="a8f9e-145">系統變更已結束。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-145">A system change has ended.</span></span><br/>                                                                                                                                                           |
| <span id="END_SYSTEM_CHANGE"></span><span id="end_system_change"></span><dl> <span data-ttu-id="a8f9e-146"><dt>**結束 \_系統 \_ 變更**</dt> <dt>101</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-146"><dt>**END\_SYSTEM\_CHANGE**</dt> <dt>101</dt></span></span> </dl>                             | <span data-ttu-id="a8f9e-147">系統變更已結束。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-147">A system change has ended.</span></span><br/>                                                                                                                                                           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f9e-148">傳回值</span><span class="sxs-lookup"><span data-stu-id="a8f9e-148">Return value</span></span>

<span data-ttu-id="a8f9e-149">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-149">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a8f9e-150">否則，方法會傳回 Winerror.h 中定義的其中一個 COM 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-150">Otherwise, the method returns one of the COM error codes defined in WinError.h.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f9e-151">備註</span><span class="sxs-lookup"><span data-stu-id="a8f9e-151">Remarks</span></span>

<span data-ttu-id="a8f9e-152">\* \* Windows 8： \* \*</span><span class="sxs-lookup"><span data-stu-id="a8f9e-152">\*\*Windows 8:  \*\*</span></span>

<span data-ttu-id="a8f9e-153">新的登錄機碼可讓應用程式開發人員變更還原點建立的頻率。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-153">A new registry key enables application developers to change the frequency of restore-point creation.</span></span>

<span data-ttu-id="a8f9e-154">應用程式應該建立此金鑰來使用它，因為它不會在系統中之外。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-154">Applications should create this key to use it because it will not preexist in the system.</span></span> <span data-ttu-id="a8f9e-155">如果機碼不存在，則預設會套用下列各項。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-155">The following will apply by default if the key does not exist.</span></span> <span data-ttu-id="a8f9e-156">如果應用程式呼叫 **CreateRestorePoint** 方法來建立還原點，則 Windows 會在過去24小時內建立任何還原點時，略過建立這個新的還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-156">If an application calls the **CreateRestorePoint** method to create a restore point, Windows skips creating this new restore point if any restore points have been created in the last 24 hours.</span></span> <span data-ttu-id="a8f9e-157">**CreateRestorePoint** 方法會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-157">The **CreateRestorePoint** method returns **S\_OK**.</span></span>

<span data-ttu-id="a8f9e-158">開發人員可以撰寫應用程式，以在登錄機碼 **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** 下建立 **DWORD** 值 **SystemRestorePointCreationFrequency** 。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-158">Developers can write applications that create the **DWORD** value **SystemRestorePointCreationFrequency** under the registry key **HKLM\\Software\\Microsoft\\Windows NT\\CurrentVersion\\SystemRestore**.</span></span> <span data-ttu-id="a8f9e-159">此登錄機碼的值可以變更還原點建立的頻率。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-159">The value of this registry key can change the frequency of restore point creation.</span></span> <span data-ttu-id="a8f9e-160">此登錄機碼的值可以變更還原點建立的頻率。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-160">The value of this registry key can change the frequency of restore point creation.</span></span>

<span data-ttu-id="a8f9e-161">如果應用程式呼叫 **CreateRestorePoint** 來建立還原點，而登錄機碼值為0，則系統還原不會略過建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-161">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is 0, system restore does not skip creating the new restore point.</span></span>

<span data-ttu-id="a8f9e-162">如果應用程式呼叫 **CreateRestorePoint** 來建立還原點，而登錄機碼值是整數 n，則系統還原會在前 N 分鐘內建立任何還原點時，略過建立新的還原點。</span><span class="sxs-lookup"><span data-stu-id="a8f9e-162">If the application calls **CreateRestorePoint** to create a restore point, and the registry key value is the integer N, system restore skips creating a new restore point if any restore points were created in the previous N minutes.</span></span>

## <a name="examples"></a><span data-ttu-id="a8f9e-163">範例</span><span class="sxs-lookup"><span data-stu-id="a8f9e-163">Examples</span></span>


```VB
'CreateRestorePoint Method of the SystemRestore Class
'Creates a restore point. Specifies the beginning and 
'the ending of a set of changes so that System Restore 
'can create a restore point.This method is the 
'scriptable equivalent of the SRSetRestorePoint function.

Set Args = wscript.Arguments
If Args.Count() > 0 Then
    RpName = Args.item(0)
Else 
    RpName = "Vbscript"
End If

Set obj = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestore")

If (obj.CreateRestorePoint(RpName, 0, 100)) = 0 Then
    wscript.Echo "Success"
Else 
    wscript.Echo "Failed"
End If
```



## <a name="requirements"></a><span data-ttu-id="a8f9e-164">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8f9e-164">Requirements</span></span>



| <span data-ttu-id="a8f9e-165">需求</span><span class="sxs-lookup"><span data-stu-id="a8f9e-165">Requirement</span></span> | <span data-ttu-id="a8f9e-166">值</span><span class="sxs-lookup"><span data-stu-id="a8f9e-166">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="a8f9e-167">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8f9e-167">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f9e-168">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8f9e-168">Windows XP \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a8f9e-169">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8f9e-169">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f9e-170">都不支援</span><span class="sxs-lookup"><span data-stu-id="a8f9e-170">None supported</span></span><br/>                                                         |
| <span data-ttu-id="a8f9e-171">命名空間</span><span class="sxs-lookup"><span data-stu-id="a8f9e-171">Namespace</span></span><br/>                | <span data-ttu-id="a8f9e-172">根 \\ 預設值</span><span class="sxs-lookup"><span data-stu-id="a8f9e-172">Root\\Default</span></span><br/>                                                          |
| <span data-ttu-id="a8f9e-173">MOF</span><span class="sxs-lookup"><span data-stu-id="a8f9e-173">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8f9e-174"><dt>Sr-iov</dt></span><span class="sxs-lookup"><span data-stu-id="a8f9e-174"><dt>Sr.mof</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8f9e-175">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8f9e-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f9e-176">**SystemRestore**</span><span class="sxs-lookup"><span data-stu-id="a8f9e-176">**SystemRestore**</span></span>](systemrestore.md)
</dt> </dl>

 

 





