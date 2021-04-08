---
description: 代表 Windows 電腦系統上的環境或系統內容設定。
ms.assetid: da7ee891-c759-4046-a9d8-d3caf66ab5a9
ms.tgt_platform: multiple
title: Win32_Environment 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Environment
- Win32_Environment.Caption
- Win32_Environment.Description
- Win32_Environment.InstallDate
- Win32_Environment.Status
- Win32_Environment.Name
- Win32_Environment.SystemVariable
- Win32_Environment.UserName
- Win32_Environment.VariableValue
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b7267e3ac03c14cfc6ad6ca73ede42cc8478b41
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847589"
---
# <a name="win32_environment-class"></a><span data-ttu-id="1088a-103">Win32 \_ 環境類別</span><span class="sxs-lookup"><span data-stu-id="1088a-103">Win32\_Environment class</span></span>

<span data-ttu-id="1088a-104">**Win32 \_ 環境** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)代表 Windows 電腦系統上的環境或系統內容設定。</span><span class="sxs-lookup"><span data-stu-id="1088a-104">The **Win32\_Environment** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents an environment or system environment setting on a Windows computer system.</span></span> <span data-ttu-id="1088a-105">查詢這個類別會傳回在中找到的環境變數：</span><span class="sxs-lookup"><span data-stu-id="1088a-105">Querying this class returns environment variables found in:</span></span>

<span data-ttu-id="1088a-106">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Sessionmanager** \\ **環境**</span><span class="sxs-lookup"><span data-stu-id="1088a-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="1088a-107">及</span><span class="sxs-lookup"><span data-stu-id="1088a-107">and</span></span>

<span data-ttu-id="1088a-108">**HKEY \_使用者** \\ **< 使用者 >** \\ **環境**</span><span class="sxs-lookup"><span data-stu-id="1088a-108">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="1088a-109">下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="1088a-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1088a-110">屬性會依字母順序列出，而不是依 MOF 順序列出。</span><span class="sxs-lookup"><span data-stu-id="1088a-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1088a-111">語法</span><span class="sxs-lookup"><span data-stu-id="1088a-111">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{8502C4D2-5FBB-11D2-AAC1-006008C78BC7}"), SupportsCreate, CreateBy("PutInstance"), SupportsDelete, DeleteBy("DeleteInstance"), SupportsUpdate, AMENDMENT]
class Win32_Environment : CIM_SystemResource
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Status;
  string   Name;
  boolean  SystemVariable;
  string   UserName;
  string   VariableValue;
};
```

## <a name="members"></a><span data-ttu-id="1088a-112">成員</span><span class="sxs-lookup"><span data-stu-id="1088a-112">Members</span></span>

<span data-ttu-id="1088a-113">**Win32 \_ 環境** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="1088a-113">The **Win32\_Environment** class has these types of members:</span></span>

-   [<span data-ttu-id="1088a-114">屬性</span><span class="sxs-lookup"><span data-stu-id="1088a-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1088a-115">屬性</span><span class="sxs-lookup"><span data-stu-id="1088a-115">Properties</span></span>

<span data-ttu-id="1088a-116">**Win32 \_ 環境** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="1088a-116">The **Win32\_Environment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1088a-117">**標題**</span><span class="sxs-lookup"><span data-stu-id="1088a-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-118">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1088a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-119">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1088a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1088a-120">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Caption" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-120">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-121">物件的簡短文字描述。</span><span class="sxs-lookup"><span data-stu-id="1088a-121">A short textual description of the object.</span></span>

<span data-ttu-id="1088a-122">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1088a-122">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1088a-123">**說明**</span><span class="sxs-lookup"><span data-stu-id="1088a-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-124">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1088a-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-125">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1088a-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1088a-126">限定詞： [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Description" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-126">Qualifiers: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-127">物件的文字描述。</span><span class="sxs-lookup"><span data-stu-id="1088a-127">A textual description of the object.</span></span>

<span data-ttu-id="1088a-128">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1088a-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1088a-129">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1088a-129">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-130">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="1088a-130">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-131">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1088a-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1088a-132">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" 安裝日期 ") </span><span class="sxs-lookup"><span data-stu-id="1088a-132">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-133">指出物件的安裝時間。</span><span class="sxs-lookup"><span data-stu-id="1088a-133">Indicates when the object was installed.</span></span> <span data-ttu-id="1088a-134">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="1088a-134">Lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="1088a-135">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1088a-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1088a-136">**名稱**</span><span class="sxs-lookup"><span data-stu-id="1088a-136">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-137">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1088a-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-138">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1088a-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1088a-139">限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Name" ) ， [**key**](/windows/desktop/WmiSdk/key-qualifier)， [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ 環境" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-139">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-140">指定以 Windows 為基礎的環境變數名稱的字元字串。</span><span class="sxs-lookup"><span data-stu-id="1088a-140">Character string that specifies the name of a Windows-based environment variable.</span></span> <span data-ttu-id="1088a-141">藉由指定尚未存在的變數名稱，應用程式會建立新的環境變數。</span><span class="sxs-lookup"><span data-stu-id="1088a-141">By specifying the name of a variable that does not yet exist, an application creates a new environment variable.</span></span>

<span data-ttu-id="1088a-142">範例： "Path"</span><span class="sxs-lookup"><span data-stu-id="1088a-142">Example: "Path"</span></span>

</dd> <dt>

<span data-ttu-id="1088a-143">**狀態**</span><span class="sxs-lookup"><span data-stu-id="1088a-143">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-144">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1088a-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-145">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1088a-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1088a-146">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) ， [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Status" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-146">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-147">表示物件目前狀態的字串。</span><span class="sxs-lookup"><span data-stu-id="1088a-147">String that indicates the current status of the object.</span></span> <span data-ttu-id="1088a-148">您可以定義操作和非運作狀態。</span><span class="sxs-lookup"><span data-stu-id="1088a-148">Operational and non-operational status can be defined.</span></span> <span data-ttu-id="1088a-149">操作狀態可以包含「確定」、「降級」和「Pred 失敗」。</span><span class="sxs-lookup"><span data-stu-id="1088a-149">Operational status can include "OK", "Degraded", and "Pred Fail".</span></span> <span data-ttu-id="1088a-150">「Pred 失敗」表示專案正常運作，但正在預測失敗 (例如，啟用智慧型硬碟) 。</span><span class="sxs-lookup"><span data-stu-id="1088a-150">"Pred Fail" indicates that an element is functioning properly, but is predicting a failure (for example, a SMART-enabled hard disk drive).</span></span>

<span data-ttu-id="1088a-151">非操作狀態可能包括「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="1088a-151">Non-operational status can include "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="1088a-152">「服務」可以在磁片鏡像重新同步處理、重載使用者權限清單或其他系統管理工作時套用。</span><span class="sxs-lookup"><span data-stu-id="1088a-152">"Service" can apply during disk mirror-resilvering, reloading a user permissions list, or other administrative work.</span></span> <span data-ttu-id="1088a-153">並非所有這類工作都在線上，但是受控元素不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="1088a-153">Not all such work is online, but the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="1088a-154">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="1088a-154">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1088a-155">包括下列值：</span><span class="sxs-lookup"><span data-stu-id="1088a-155">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1088a-156">**確定** ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="1088a-156">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1088a-157">**錯誤** ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-157">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1088a-158">**降級** ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-158">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1088a-159">**未知** 的 ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-159">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1088a-160">**Pred 失敗** ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-160">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1088a-161">**開始** ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-161">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1088a-162">**停止** ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-162">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1088a-163">**服務** ( 「服務」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-163">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1088a-164">**壓力** ( 「壓力」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-164">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1088a-165">**NonRecover** ( "NonRecover" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-165">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1088a-166">**沒有連絡人** ( 「沒有連絡人」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-166">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1088a-167">**遺失的 comm** ( 「遺失的通訊」 ) </span><span class="sxs-lookup"><span data-stu-id="1088a-167">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1088a-168">**SystemVariable**</span><span class="sxs-lookup"><span data-stu-id="1088a-168">**SystemVariable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-169">資料類型： **布林值**</span><span class="sxs-lookup"><span data-stu-id="1088a-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-170">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1088a-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1088a-171">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ 環境" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-171">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-172">指出變數是否為系統變數。</span><span class="sxs-lookup"><span data-stu-id="1088a-172">Indicates whether the variable is a system variable.</span></span> <span data-ttu-id="1088a-173">系統變數是由作業系統設定，而且與使用者環境設定無關。</span><span class="sxs-lookup"><span data-stu-id="1088a-173">A system variable is set by the operating system, and is independent from user environment settings.</span></span>

</dd> <dt>

<span data-ttu-id="1088a-174">**使用者名稱**</span><span class="sxs-lookup"><span data-stu-id="1088a-174">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-175">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1088a-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-176">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="1088a-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1088a-177">限定詞： [**key**](/windows/desktop/WmiSdk/key-qualifier)、 [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260) 、 [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ 環境" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-177">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (260), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-178">環境設定的擁有者名稱。</span><span class="sxs-lookup"><span data-stu-id="1088a-178">Name of the owner of the environment setting.</span></span> <span data-ttu-id="1088a-179">它會設定為，以 <SYSTEM> 針對 Windows 系統 (特定的設定，而不是特定使用者) 和 <DEFAULT> 預設使用者設定。</span><span class="sxs-lookup"><span data-stu-id="1088a-179">It is set to <SYSTEM> for settings that are specific to the Windows-based system (as opposed to a specific user) and <DEFAULT> for default user settings.</span></span>

<span data-ttu-id="1088a-180">範例： "JSmith"</span><span class="sxs-lookup"><span data-stu-id="1088a-180">Example: "JSmith"</span></span>

</dd> <dt>

<span data-ttu-id="1088a-181">**VariableValue**</span><span class="sxs-lookup"><span data-stu-id="1088a-181">**VariableValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1088a-182">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="1088a-182">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1088a-183">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="1088a-183">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="1088a-184">限定詞： [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Session Manager \\ \\ 環境" ) </span><span class="sxs-lookup"><span data-stu-id="1088a-184">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Session Manager\\\\Environment")</span></span>
</dt> </dl>

<span data-ttu-id="1088a-185">以 Windows 為基礎之環境變數的預留位置變數。</span><span class="sxs-lookup"><span data-stu-id="1088a-185">Placeholder variable of a Windows-based environment variable.</span></span> <span data-ttu-id="1088a-186">檔案系統目錄之類的資訊可從電腦變更為電腦。</span><span class="sxs-lookup"><span data-stu-id="1088a-186">Information like the file system directory can change from computer to computer.</span></span> <span data-ttu-id="1088a-187">作業系統會替代這些預留位置。</span><span class="sxs-lookup"><span data-stu-id="1088a-187">The operating system substitutes placeholders for these.</span></span>

<span data-ttu-id="1088a-188">範例： "% SystemRoot%"</span><span class="sxs-lookup"><span data-stu-id="1088a-188">Example: "%SystemRoot%"</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1088a-189">備註</span><span class="sxs-lookup"><span data-stu-id="1088a-189">Remarks</span></span>

<span data-ttu-id="1088a-190">**Win32 \_ 環境** 類別衍生自 [**CIM \_ SystemResource**](cim-systemresource.md)。</span><span class="sxs-lookup"><span data-stu-id="1088a-190">The **Win32\_Environment** class is derived from [**CIM\_SystemResource**](cim-systemresource.md).</span></span> <span data-ttu-id="1088a-191">您可以使用這個類別來尋找特殊資料夾的路徑，例如系統資料夾或遠端電腦上的程式檔。</span><span class="sxs-lookup"><span data-stu-id="1088a-191">You can use this class to find the paths of special folders such as the System folder or Program files on a remote machine.</span></span> <span data-ttu-id="1088a-192">一些範例包括： windir、systemroot、programfiles 和 userprofile。</span><span class="sxs-lookup"><span data-stu-id="1088a-192">Some examples are: windir, systemroot, programfiles, and userprofile.</span></span> <span data-ttu-id="1088a-193">**Win32 \_環境** 基本上會傳回可在中找到的內容：</span><span class="sxs-lookup"><span data-stu-id="1088a-193">**Win32\_Environment** basically returns what can be found in:</span></span>

<span data-ttu-id="1088a-194">**HKEY \_本機 \_ 電腦** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Sessionmanager** \\ **環境**</span><span class="sxs-lookup"><span data-stu-id="1088a-194">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Sessionmanager**\\**Environment**</span></span>

<span data-ttu-id="1088a-195">及</span><span class="sxs-lookup"><span data-stu-id="1088a-195">and</span></span>

<span data-ttu-id="1088a-196">**HKEY \_使用者** \\ **< 使用者 >** \\ **環境**</span><span class="sxs-lookup"><span data-stu-id="1088a-196">**HKEY\_USERS**\\**<*user*>**\\**Environment**</span></span>

<span data-ttu-id="1088a-197">使用這個類別的呼叫進程必須在登錄所在的電腦上具有「 **SE \_ 還原 \_ 名稱** 」許可權。</span><span class="sxs-lookup"><span data-stu-id="1088a-197">The calling process that uses this class must have the **SE\_RESTORE\_NAME** privilege on the computer in which the registry resides.</span></span> <span data-ttu-id="1088a-198">例如，如果您在本機電腦上列舉此類別，您的應用程式執行所在的帳戶必須具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="1088a-198">For example, if you enumerate this class on the local computer, the account under which your application runs must have this privilege.</span></span> <span data-ttu-id="1088a-199">如需詳細資訊，請參閱 [執行特殊許可權作業](/windows/desktop/WmiSdk/executing-privileged-operations)。</span><span class="sxs-lookup"><span data-stu-id="1088a-199">For more information, see [Executing Privileged Operations](/windows/desktop/WmiSdk/executing-privileged-operations).</span></span>

## <a name="examples"></a><span data-ttu-id="1088a-200">範例</span><span class="sxs-lookup"><span data-stu-id="1088a-200">Examples</span></span>

<span data-ttu-id="1088a-201">電腦 Perl 範例 [上的清單環境變數](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) 會使用 WMI 來傳回電腦上所有環境變數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1088a-201">The [List Environment Variables on a Computer](https://Gallery.TechNet.Microsoft.Com/79ae998e-2e29-4a6d-b0a6-34ed5b709d49) Perl sample uses WMI to return information about all the environment variables on a computer.</span></span>

<span data-ttu-id="1088a-202">下列 VBScript 程式碼範例會列舉本機電腦上的環境變數。</span><span class="sxs-lookup"><span data-stu-id="1088a-202">The following VBScript code example enumerates the environment variables on the local computer.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colVar = objWMIService.ExecQuery("Select * from Win32_Environment")
For Each objVar in colVar
    Wscript.Echo "Description: " & objVar.Description & VBNewLine _
               & "Name: " & objVar.Name & VBNewLine _
               & "System Variable: " & objVar.SystemVariable & VBNewLine _
               & "User Name: " & objVar.UserName & VBNewLine _
               & "Variable Value: " & objVar.VariableValue 
Next
```



<span data-ttu-id="1088a-203">下列 VBScript 程式碼範例會將名為 BUILD TYPE 的環境變數變更 \_ 為使用者輸入的值。</span><span class="sxs-lookup"><span data-stu-id="1088a-203">The following VBScript code example changes an environment variable named BUILD\_TYPE to a value input by the user.</span></span> <span data-ttu-id="1088a-204">腳本會假設組建 \_ 類型變數已經存在。</span><span class="sxs-lookup"><span data-stu-id="1088a-204">The script assumes that the BUILD\_TYPE variable already exists.</span></span> <span data-ttu-id="1088a-205">如果不存在，腳本便會結束。</span><span class="sxs-lookup"><span data-stu-id="1088a-205">If it does not exist then the script ends.</span></span> <span data-ttu-id="1088a-206">已檢查輸入值：它必須是 "Build1"、"Build2" 或 "Build3"，而且不接受任何其他值。</span><span class="sxs-lookup"><span data-stu-id="1088a-206">The input value is checked: it must be either "Build1", "Build2", or "Build3", and no other value is accepted.</span></span> <span data-ttu-id="1088a-207">VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) 函式會使輸入不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="1088a-207">The VBScript [UCase](https://msdn.microsoft.com/library/aa902519.aspx) function makes the input case-insensitive.</span></span> <span data-ttu-id="1088a-208">如果中輸入的內容不是三個可接受值的其中一個，則腳本會結束。</span><span class="sxs-lookup"><span data-stu-id="1088a-208">If what is typed in is not one of the three acceptable values, the script ends.</span></span>


```VB
On Error Resume Next
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colItems = objWMIService.ExecQuery("Select * from Win32_Environment")
Found = False
For Each objItem in colItems
    If objItem.Name = "BUILD_TYPE" Then
    Found = True
    Change = UCase(InputBox("BUILD_TYPE currently = " & objItem.VariableValue & VBNewLine _
                          & "Change options are Build1, Build2, Build3 "))
        If UCase(Change) = "BUILD1" OR Change = "BUILD2" OR Change = "BUILD3" Then
            objItem.VariableValue = Change
            objItem.Put_
        WScript.Echo "BUILD_TYPE changed to " & objItem.VariableValue
        Else 
        WScript.Echo "No input or unacceptable input." & " No change to BUILD_TYPE"
        End If
    End If
Next
If Found = False Then
    WScript.Echo "User-defined environment variable BUILD_TYPE not found."
End If
```



## <a name="requirements"></a><span data-ttu-id="1088a-209">規格需求</span><span class="sxs-lookup"><span data-stu-id="1088a-209">Requirements</span></span>



| <span data-ttu-id="1088a-210">需求</span><span class="sxs-lookup"><span data-stu-id="1088a-210">Requirement</span></span> | <span data-ttu-id="1088a-211">值</span><span class="sxs-lookup"><span data-stu-id="1088a-211">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1088a-212">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1088a-212">Minimum supported client</span></span><br/> | <span data-ttu-id="1088a-213">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1088a-213">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1088a-214">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1088a-214">Minimum supported server</span></span><br/> | <span data-ttu-id="1088a-215">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1088a-215">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1088a-216">命名空間</span><span class="sxs-lookup"><span data-stu-id="1088a-216">Namespace</span></span><br/>                | <span data-ttu-id="1088a-217">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="1088a-217">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1088a-218">MOF</span><span class="sxs-lookup"><span data-stu-id="1088a-218">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1088a-219"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="1088a-219"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1088a-220">DLL</span><span class="sxs-lookup"><span data-stu-id="1088a-220">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1088a-221"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1088a-221"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1088a-222">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1088a-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1088a-223">**CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="1088a-223">**CIM\_SystemResource**</span></span>](cim-systemresource.md)
</dt> <dt>

<span data-ttu-id="1088a-224">[作業系統類別](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1088a-224">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

