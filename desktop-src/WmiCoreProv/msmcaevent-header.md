---
description: 代表所有 MSMCAEvent 類別使用的一般標頭。 此類別僅適用于64位的 Windows 系統。
ms.assetid: ff20522c-f805-47dc-bef2-4176211de698
title: MSMCAEvent_Header 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAEvent_Header
- MSMCAEvent_Header.AdditionalErrors
- MSMCAEvent_Header.Cpu
- MSMCAEvent_Header.ErrorSeverity
- MSMCAEvent_Header.RecordId
- MSMCAEvent_Header.Type
- MSMCAEvent_Header.LogToEventlog
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 426f943014f3b6cfbdba5a25d331c0ea621048cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991899"
---
# <a name="msmcaevent_header-class"></a><span data-ttu-id="11d43-104">MSMCAEvent \_ 標頭類別</span><span class="sxs-lookup"><span data-stu-id="11d43-104">MSMCAEvent\_Header class</span></span>

<span data-ttu-id="11d43-105">**MSMCAEvent \_ 標頭** 類別代表所有 [MSMCA 類別](msmca-classes.md)使用的一般標頭。</span><span class="sxs-lookup"><span data-stu-id="11d43-105">The **MSMCAEvent\_Header** class represents the common header that all [MSMCA classes](msmca-classes.md) use.</span></span> <span data-ttu-id="11d43-106">使用標頭檔案，C 和 c + + 程式碼可以有描述所有事件之一般標頭的資料結構。</span><span class="sxs-lookup"><span data-stu-id="11d43-106">The header files are used so that C and C++ code can have a data structure that describes the common header for all events.</span></span> <span data-ttu-id="11d43-107">此類別已保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="11d43-107">This class is reserved for internal use.</span></span> <span data-ttu-id="11d43-108">此類別僅適用于64位的 Windows 系統。</span><span class="sxs-lookup"><span data-stu-id="11d43-108">This class is available only in 64-bit Windows systems.</span></span>

<span data-ttu-id="11d43-109">下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="11d43-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="11d43-110">屬性和方法是以字母順序排列，而不是 MOF 順序。</span><span class="sxs-lookup"><span data-stu-id="11d43-110">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="11d43-111">語法</span><span class="sxs-lookup"><span data-stu-id="11d43-111">Syntax</span></span>

``` syntax
class MSMCAEvent_Header
{
  uint32 AdditionalErrors;
  uint32 Cpu;
  uint8  ErrorSeverity;
  uint64 RecordId;
  uint32 Type;
  uint32 LogToEventlog;
};
```

## <a name="members"></a><span data-ttu-id="11d43-112">成員</span><span class="sxs-lookup"><span data-stu-id="11d43-112">Members</span></span>

<span data-ttu-id="11d43-113">**MSMCAEvent \_ 標頭** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="11d43-113">The **MSMCAEvent\_Header** class has these types of members:</span></span>

-   [<span data-ttu-id="11d43-114">屬性</span><span class="sxs-lookup"><span data-stu-id="11d43-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="11d43-115">屬性</span><span class="sxs-lookup"><span data-stu-id="11d43-115">Properties</span></span>

<span data-ttu-id="11d43-116">**MSMCAEvent \_ 標頭** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="11d43-116">The **MSMCAEvent\_Header** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="11d43-117">**AdditionalErrors**</span><span class="sxs-lookup"><span data-stu-id="11d43-117">**AdditionalErrors**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d43-118">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="11d43-118">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d43-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11d43-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d43-120">MCA 記錄中的其他錯誤數目。</span><span class="sxs-lookup"><span data-stu-id="11d43-120">Number of additional errors in the MCA record.</span></span>

</dd> <dt>

<span data-ttu-id="11d43-121">**Cpu**</span><span class="sxs-lookup"><span data-stu-id="11d43-121">**Cpu**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d43-122">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="11d43-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d43-123">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11d43-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d43-124">報告錯誤的 CPU。</span><span class="sxs-lookup"><span data-stu-id="11d43-124">CPU that reports the error.</span></span> <span data-ttu-id="11d43-125">這個屬性只適用于處理器系統，其中第一個處理器被指派數位0，第二個處理器指派編號1，依此類推。</span><span class="sxs-lookup"><span data-stu-id="11d43-125">This property only applies to a multiprocessor system in which the first processor is assigned the number 0, the second processor is assigned the number 1, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="11d43-126">**ErrorSeverity**</span><span class="sxs-lookup"><span data-stu-id="11d43-126">**ErrorSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d43-127">資料類型： **uint8**</span><span class="sxs-lookup"><span data-stu-id="11d43-127">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="11d43-128">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11d43-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d43-129">回報之錯誤的嚴重性層級。</span><span class="sxs-lookup"><span data-stu-id="11d43-129">Severity level of the error reported.</span></span>



| <span data-ttu-id="11d43-130">值</span><span class="sxs-lookup"><span data-stu-id="11d43-130">Value</span></span>                                                                                                | <span data-ttu-id="11d43-131">意義</span><span class="sxs-lookup"><span data-stu-id="11d43-131">Meaning</span></span>                |
|------------------------------------------------------------------------------------------------------|------------------------|
| <span id="0"></span><dl> <span data-ttu-id="11d43-132"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="11d43-132"><dt>**0**</dt></span></span> </dl> | <span data-ttu-id="11d43-133">可復原</span><span class="sxs-lookup"><span data-stu-id="11d43-133">Recoverable</span></span><br/> |
| <span id="1"></span><dl> <span data-ttu-id="11d43-134"><dt>**1**</dt></span><span class="sxs-lookup"><span data-stu-id="11d43-134"><dt>**1**</dt></span></span> </dl> | <span data-ttu-id="11d43-135">嚴重</span><span class="sxs-lookup"><span data-stu-id="11d43-135">Fatal</span></span><br/>       |
| <span id="2"></span><dl> <span data-ttu-id="11d43-136"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="11d43-136"><dt>**2**</dt></span></span> </dl> | <span data-ttu-id="11d43-137">時發生</span><span class="sxs-lookup"><span data-stu-id="11d43-137">Correctable</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="11d43-138">**LogToEventlog**</span><span class="sxs-lookup"><span data-stu-id="11d43-138">**LogToEventlog**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d43-139">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="11d43-139">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d43-140">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11d43-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d43-141">如果 0 (零) 則不會將此事件記錄到系統事件記錄檔。</span><span class="sxs-lookup"><span data-stu-id="11d43-141">If 0 (zero) then this event is not logged to the system event log.</span></span>

</dd> <dt>

<span data-ttu-id="11d43-142">**記錄識別碼**</span><span class="sxs-lookup"><span data-stu-id="11d43-142">**RecordId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d43-143">資料類型： **uint64**</span><span class="sxs-lookup"><span data-stu-id="11d43-143">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="11d43-144">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11d43-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d43-145">此錯誤之錯誤記錄的記錄識別碼。</span><span class="sxs-lookup"><span data-stu-id="11d43-145">Record identifier of the error record for this error.</span></span>

<span data-ttu-id="11d43-146">如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/previous-versions//aa393262(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="11d43-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="11d43-147">**型別**</span><span class="sxs-lookup"><span data-stu-id="11d43-147">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11d43-148">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="11d43-148">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="11d43-149">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="11d43-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="11d43-150">事件記錄檔訊息的類型。</span><span class="sxs-lookup"><span data-stu-id="11d43-150">Type of event log message.</span></span> <span data-ttu-id="11d43-151">這些訊息會對應到事件記錄檔訊息程式碼，當 Windows 事件記錄取用者提供者收到其中一個事件時，該訊息會用來插入事件記錄檔訊息。</span><span class="sxs-lookup"><span data-stu-id="11d43-151">These messages correspond to the event log message codes used to insert event log messages by the Windows event log consumer provider when it receives one of the events.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11d43-152">規格需求</span><span class="sxs-lookup"><span data-stu-id="11d43-152">Requirements</span></span>



| <span data-ttu-id="11d43-153">需求</span><span class="sxs-lookup"><span data-stu-id="11d43-153">Requirement</span></span> | <span data-ttu-id="11d43-154">值</span><span class="sxs-lookup"><span data-stu-id="11d43-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11d43-155">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11d43-155">Minimum supported client</span></span><br/> | <span data-ttu-id="11d43-156">Windows XP</span><span class="sxs-lookup"><span data-stu-id="11d43-156">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="11d43-157">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11d43-157">Minimum supported server</span></span><br/> | <span data-ttu-id="11d43-158">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="11d43-158">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="11d43-159">命名空間</span><span class="sxs-lookup"><span data-stu-id="11d43-159">Namespace</span></span><br/>                | <span data-ttu-id="11d43-160">根 \\ wmi</span><span class="sxs-lookup"><span data-stu-id="11d43-160">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="11d43-161">MOF</span><span class="sxs-lookup"><span data-stu-id="11d43-161">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11d43-162"><dt>Wmicore mof</dt></span><span class="sxs-lookup"><span data-stu-id="11d43-162"><dt>Wmicore.mof</dt></span></span> </dl> |
| <span data-ttu-id="11d43-163">DLL</span><span class="sxs-lookup"><span data-stu-id="11d43-163">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11d43-164"><dt>Wmiprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11d43-164"><dt>Wmiprov.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11d43-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11d43-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11d43-166">MSMCA 類別</span><span class="sxs-lookup"><span data-stu-id="11d43-166">MSMCA Classes</span></span>](msmca-classes.md)
</dt> <dt>

[<span data-ttu-id="11d43-167">WMI c + + 類別</span><span class="sxs-lookup"><span data-stu-id="11d43-167">WMI C++ Classes</span></span>](/windows/desktop/WmiSdk/wmi-c-classes)
</dt> </dl>

 

