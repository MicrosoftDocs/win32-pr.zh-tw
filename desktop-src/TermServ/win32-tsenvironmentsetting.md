---
title: Win32_TSEnvironmentSetting 類別
description: 定義 Win32 終端機類別的配置設定， \_ 包括初始程式原則。
ms.assetid: 2d310a1e-a1bd-4ccb-965e-8389aaa2e4c1
ms.tgt_platform: multiple
keywords:
- Win32_TSEnvironmentSetting 類別遠端桌面服務
- Win32_TSEnvironmentSetting 類別遠端桌面服務，描述
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting.Caption
- Win32_TSEnvironmentSetting.Description
- Win32_TSEnvironmentSetting.InstallDate
- Win32_TSEnvironmentSetting.Name
- Win32_TSEnvironmentSetting.Status
- Win32_TSEnvironmentSetting.TerminalName
- Win32_TSEnvironmentSetting.ClientWallPaper
- Win32_TSEnvironmentSetting.InitialProgramPath
- Win32_TSEnvironmentSetting.InitialProgramPolicy
- Win32_TSEnvironmentSetting.PolicySourceClientWallPaper
- Win32_TSEnvironmentSetting.PolicySourceInitialProgramPath
- Win32_TSEnvironmentSetting.PolicySourceStartIn
- Win32_TSEnvironmentSetting.Startin
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0689536385644ae3ef95d106e50ab198e5a57f93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509267"
---
# <a name="win32_tsenvironmentsetting-class"></a><span data-ttu-id="d1005-105">Win32 \_ TSEnvironmentSetting 類別</span><span class="sxs-lookup"><span data-stu-id="d1005-105">Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="d1005-106">**Win32 \_ TSEnvironmentSetting** WMI 類別會定義 [**win32 \_ 終端**](win32-terminal.md)機類別的設定，包括初始程式原則。</span><span class="sxs-lookup"><span data-stu-id="d1005-106">The **Win32\_TSEnvironmentSetting** WMI class defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

<span data-ttu-id="d1005-107">下列語法簡化自 MOF 程式碼，並依字母順序包含所有定義和繼承的屬性。</span><span class="sxs-lookup"><span data-stu-id="d1005-107">The following syntax is simplified from MOF code and includes all defined and inherited properties, in alphabetical order.</span></span> <span data-ttu-id="d1005-108">如需方法的參考資訊，請參閱本主題稍後的方法表格。</span><span class="sxs-lookup"><span data-stu-id="d1005-108">For reference information on methods, see the table of methods later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1005-109">語法</span><span class="sxs-lookup"><span data-stu-id="d1005-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_TSENVIRONMENTSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSEnvironmentSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  uint32   ClientWallPaper;
  string   InitialProgramPath;
  uint32   InitialProgramPolicy;
  uint32   PolicySourceClientWallPaper;
  uint32   PolicySourceInitialProgramPath;
  uint32   PolicySourceStartIn;
  string   Startin;
};
```

## <a name="members"></a><span data-ttu-id="d1005-110">成員</span><span class="sxs-lookup"><span data-stu-id="d1005-110">Members</span></span>

<span data-ttu-id="d1005-111">**Win32 \_ TSEnvironmentSetting** 類別具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="d1005-111">The **Win32\_TSEnvironmentSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="d1005-112">方法</span><span class="sxs-lookup"><span data-stu-id="d1005-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="d1005-113">屬性</span><span class="sxs-lookup"><span data-stu-id="d1005-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="d1005-114">方法</span><span class="sxs-lookup"><span data-stu-id="d1005-114">Methods</span></span>

<span data-ttu-id="d1005-115">**Win32 \_ TSEnvironmentSetting** 類別具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="d1005-115">The **Win32\_TSEnvironmentSetting** class has these methods.</span></span>



| <span data-ttu-id="d1005-116">方法</span><span class="sxs-lookup"><span data-stu-id="d1005-116">Method</span></span>                                                                      | <span data-ttu-id="d1005-117">描述</span><span class="sxs-lookup"><span data-stu-id="d1005-117">Description</span></span>                                                            |
|:----------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="d1005-118">**InitialProgram**</span><span class="sxs-lookup"><span data-stu-id="d1005-118">**InitialProgram**</span></span>](win32-tsenvironmentsetting-initialprogram.md)         | <span data-ttu-id="d1005-119">設定包含在此類別中的啟始程式屬性。</span><span class="sxs-lookup"><span data-stu-id="d1005-119">Sets the startup program properties included in this class.</span></span><br/> |
| [<span data-ttu-id="d1005-120">**SetClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="d1005-120">**SetClientWallPaper**</span></span>](win32-tsenvironmentsetting-setclientwallpaper.md) | <span data-ttu-id="d1005-121">設定 **ClientWallPaper** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d1005-121">Sets the **ClientWallPaper** property.</span></span><br/>                      |



 

### <a name="properties"></a><span data-ttu-id="d1005-122">屬性</span><span class="sxs-lookup"><span data-stu-id="d1005-122">Properties</span></span>

<span data-ttu-id="d1005-123">**Win32 \_ TSEnvironmentSetting** 類別具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="d1005-123">The **Win32\_TSEnvironmentSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1005-124">**標題**</span><span class="sxs-lookup"><span data-stu-id="d1005-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-125">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-126">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1005-127">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64) </span><span class="sxs-lookup"><span data-stu-id="d1005-127">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="d1005-128">簡短描述 (物件的單行字串) 。</span><span class="sxs-lookup"><span data-stu-id="d1005-128">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="d1005-129">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d1005-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1005-130">**ClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="d1005-130">**ClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-131">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d1005-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-132">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-132">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-133">指定是否要在用戶端上顯示壁紙影像。</span><span class="sxs-lookup"><span data-stu-id="d1005-133">Specifies whether the wallpaper image is displayed on the client.</span></span> <span data-ttu-id="d1005-134">若未顯示壁紙影像，則可以減少重新繪製螢幕所需的時間來節省系統資源。</span><span class="sxs-lookup"><span data-stu-id="d1005-134">Not displaying the wallpaper image can save system resources by decreasing the time required to repaint the screen.</span></span>

<dt>

<span id="False"></span><span id="false"></span><span id="FALSE"></span>

<span data-ttu-id="d1005-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0) </span><span class="sxs-lookup"><span data-stu-id="d1005-135"><span id="False"></span><span id="false"></span><span id="FALSE"></span>**False** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d1005-136">壁紙影像不會顯示在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="d1005-136">The wallpaper image is not displayed on the client.</span></span>

</dd> <dt>

<span id="True"></span><span id="true"></span><span id="TRUE"></span>

<span data-ttu-id="d1005-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1) </span><span class="sxs-lookup"><span data-stu-id="d1005-137"><span id="True"></span><span id="true"></span><span id="TRUE"></span>**True** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d1005-138">背景圖樣影像會顯示在用戶端上。</span><span class="sxs-lookup"><span data-stu-id="d1005-138">The wallpaper image is displayed on the client.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1005-139">**說明**</span><span class="sxs-lookup"><span data-stu-id="d1005-139">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-140">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-141">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-142">物件的描述。</span><span class="sxs-lookup"><span data-stu-id="d1005-142">Description of the object.</span></span>

<span data-ttu-id="d1005-143">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d1005-143">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1005-144">**InitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="d1005-144">**InitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-145">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-146">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-147">登入 RD 工作階段主機伺服器之後，使用者將立即執行之程式的名稱和路徑。</span><span class="sxs-lookup"><span data-stu-id="d1005-147">The name and the path of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="d1005-148">**InitialProgramPolicy**</span><span class="sxs-lookup"><span data-stu-id="d1005-148">**InitialProgramPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-149">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d1005-149">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-150">存取類型：讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="d1005-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="d1005-151">伺服器用來判斷啟動程式路徑和檔案名的原則，以及它所在的資料夾名稱。</span><span class="sxs-lookup"><span data-stu-id="d1005-151">The policy the server uses to determine the startup program path and file name, and the name of the folder it is located in.</span></span>

<dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="d1005-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**每位使用者** (0) </span><span class="sxs-lookup"><span data-stu-id="d1005-152"><span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>**Per User** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d1005-153">使用者的啟動程式設定生效。</span><span class="sxs-lookup"><span data-stu-id="d1005-153">The user's startup program settings are in effect.</span></span>

</dd> <dt>

<span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>

<span data-ttu-id="d1005-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**伺服器-覆寫** (1) </span><span class="sxs-lookup"><span data-stu-id="d1005-154"><span id="Server-Override"></span><span id="server-override"></span><span id="SERVER-OVERRIDE"></span>**Server-Override** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d1005-155">伺服器會覆寫使用者的啟動程式設定。</span><span class="sxs-lookup"><span data-stu-id="d1005-155">The user's startup program settings are overridden by the server.</span></span>

</dd> <dt>

<span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>

<span data-ttu-id="d1005-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**單一應用程式模式** (2) </span><span class="sxs-lookup"><span data-stu-id="d1005-156"><span id="Single-App_Mode"></span><span id="single-app_mode"></span><span id="SINGLE-APP_MODE"></span>**Single-App Mode** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d1005-157">只有一個應用程式會在此會話中執行。</span><span class="sxs-lookup"><span data-stu-id="d1005-157">Only a single application will be run in this session.</span></span> <span data-ttu-id="d1005-158">會忽略啟動程式資訊。</span><span class="sxs-lookup"><span data-stu-id="d1005-158">The startup program information is ignored.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1005-159">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="d1005-159">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-160">資料類型： **datetime**</span><span class="sxs-lookup"><span data-stu-id="d1005-160">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-161">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1005-162">限定詞： [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ( "MIF。DMTF \| 元件 \| 001.5 ") </span><span class="sxs-lookup"><span data-stu-id="d1005-162">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="d1005-163">物件的安裝日期。</span><span class="sxs-lookup"><span data-stu-id="d1005-163">The date the object was installed.</span></span> <span data-ttu-id="d1005-164">缺少值並不表示物件未安裝。</span><span class="sxs-lookup"><span data-stu-id="d1005-164">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="d1005-165">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d1005-165">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1005-166">**名稱**</span><span class="sxs-lookup"><span data-stu-id="d1005-166">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-167">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-168">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-169">物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1005-169">The name of the object.</span></span>

<span data-ttu-id="d1005-170">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d1005-170">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="d1005-171">**PolicySourceClientWallPaper**</span><span class="sxs-lookup"><span data-stu-id="d1005-171">**PolicySourceClientWallPaper**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-172">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d1005-172">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-173">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-174">指出 **ClientWallPaper** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="d1005-174">Indicates whether the **ClientWallPaper** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="d1005-175">0</span><span class="sxs-lookup"><span data-stu-id="d1005-175">0</span></span>
</dt> <dd>

<span data-ttu-id="d1005-176">伺服器</span><span class="sxs-lookup"><span data-stu-id="d1005-176">Server</span></span>

</dd> <dt>

<span data-ttu-id="d1005-177">1</span><span class="sxs-lookup"><span data-stu-id="d1005-177">1</span></span>
</dt> <dd>

<span data-ttu-id="d1005-178">群組原則</span><span class="sxs-lookup"><span data-stu-id="d1005-178">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="d1005-179">2</span><span class="sxs-lookup"><span data-stu-id="d1005-179">2</span></span>
</dt> <dd>

<span data-ttu-id="d1005-180">預設</span><span class="sxs-lookup"><span data-stu-id="d1005-180">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1005-181">**PolicySourceInitialProgramPath**</span><span class="sxs-lookup"><span data-stu-id="d1005-181">**PolicySourceInitialProgramPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-182">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d1005-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-183">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-183">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-184">指出 **InitialProgramPath** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="d1005-184">Indicates whether the **InitialProgramPath** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="d1005-185">0</span><span class="sxs-lookup"><span data-stu-id="d1005-185">0</span></span>
</dt> <dd>

<span data-ttu-id="d1005-186">伺服器</span><span class="sxs-lookup"><span data-stu-id="d1005-186">Server</span></span>

</dd> <dt>

<span data-ttu-id="d1005-187">1</span><span class="sxs-lookup"><span data-stu-id="d1005-187">1</span></span>
</dt> <dd>

<span data-ttu-id="d1005-188">群組原則</span><span class="sxs-lookup"><span data-stu-id="d1005-188">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="d1005-189">2</span><span class="sxs-lookup"><span data-stu-id="d1005-189">2</span></span>
</dt> <dd>

<span data-ttu-id="d1005-190">預設</span><span class="sxs-lookup"><span data-stu-id="d1005-190">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1005-191">**PolicySourceStartIn**</span><span class="sxs-lookup"><span data-stu-id="d1005-191">**PolicySourceStartIn**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-192">資料類型： **uint32**</span><span class="sxs-lookup"><span data-stu-id="d1005-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-193">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-193">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-194">指出 **StartIn** 屬性是由伺服器、群組原則或預設設定。</span><span class="sxs-lookup"><span data-stu-id="d1005-194">Indicates whether the **StartIn** property is configured by the server, group policy, or by default.</span></span>

<dt>

<span data-ttu-id="d1005-195">0</span><span class="sxs-lookup"><span data-stu-id="d1005-195">0</span></span>
</dt> <dd>

<span data-ttu-id="d1005-196">伺服器</span><span class="sxs-lookup"><span data-stu-id="d1005-196">Server</span></span>

</dd> <dt>

<span data-ttu-id="d1005-197">1</span><span class="sxs-lookup"><span data-stu-id="d1005-197">1</span></span>
</dt> <dd>

<span data-ttu-id="d1005-198">群組原則</span><span class="sxs-lookup"><span data-stu-id="d1005-198">Group policy</span></span>

</dd> <dt>

<span data-ttu-id="d1005-199">2</span><span class="sxs-lookup"><span data-stu-id="d1005-199">2</span></span>
</dt> <dd>

<span data-ttu-id="d1005-200">預設</span><span class="sxs-lookup"><span data-stu-id="d1005-200">Default</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="d1005-201">**Startin**</span><span class="sxs-lookup"><span data-stu-id="d1005-201">**Startin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-202">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-203">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-204">在登入 RD 工作階段主機伺服器之後，使用者將立即執行之程式的工作目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d1005-204">The path of the working directory of the program the user will run immediately after logging on to the RD Session Host server.</span></span>

</dd> <dt>

<span data-ttu-id="d1005-205">**狀態**</span><span class="sxs-lookup"><span data-stu-id="d1005-205">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-206">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-206">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-207">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-207">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1005-208">限定詞： [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10) </span><span class="sxs-lookup"><span data-stu-id="d1005-208">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="d1005-209">物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="d1005-209">Current status of the object.</span></span> <span data-ttu-id="d1005-210">您可以定義各種操作和 nonoperational 狀態。</span><span class="sxs-lookup"><span data-stu-id="d1005-210">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="d1005-211">作業狀態包括：「正常」、「降級」和「Pred 失敗」 (元素（例如啟用智慧的硬碟）可能會正常運作，但在不久的未來) 中預測失敗。</span><span class="sxs-lookup"><span data-stu-id="d1005-211">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="d1005-212">Nonoperational 狀態包括：「錯誤」、「開始」、「正在停止」和「服務」。</span><span class="sxs-lookup"><span data-stu-id="d1005-212">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="d1005-213">後者（「服務」）可以在磁片的鏡像重新同步處理期間套用，重載使用者權限清單或其他系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="d1005-213">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="d1005-214">並非所有這類工作都是線上的，但受管理的元素並不是「確定」，也不是其中一個其他狀態。</span><span class="sxs-lookup"><span data-stu-id="d1005-214">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="d1005-215">這個屬性繼承自 [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)。</span><span class="sxs-lookup"><span data-stu-id="d1005-215">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="d1005-216"> ( [確定] ) </span><span class="sxs-lookup"><span data-stu-id="d1005-216">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-217"> ( 「錯誤」 ) </span><span class="sxs-lookup"><span data-stu-id="d1005-217">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-218"> ( 「降級」 ) </span><span class="sxs-lookup"><span data-stu-id="d1005-218">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-219"> ( 「未知」 ) </span><span class="sxs-lookup"><span data-stu-id="d1005-219">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-220"> ( 「Pred 失敗」 ) </span><span class="sxs-lookup"><span data-stu-id="d1005-220">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-221"> ( 「開始」 ) </span><span class="sxs-lookup"><span data-stu-id="d1005-221">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-222"> ( 「正在停止」 ) </span><span class="sxs-lookup"><span data-stu-id="d1005-222">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="d1005-223"> ( "Service" ) </span><span class="sxs-lookup"><span data-stu-id="d1005-223">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d1005-224">**TerminalName**</span><span class="sxs-lookup"><span data-stu-id="d1005-224">**TerminalName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1005-225">資料類型： **字串**</span><span class="sxs-lookup"><span data-stu-id="d1005-225">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d1005-226">存取類型：唯讀</span><span class="sxs-lookup"><span data-stu-id="d1005-226">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d1005-227">終端機的名稱。</span><span class="sxs-lookup"><span data-stu-id="d1005-227">The name of the terminal.</span></span>

<span data-ttu-id="d1005-228">這個屬性繼承自 [**Win32 \_ TerminalSetting**](win32-terminalsetting.md)。</span><span class="sxs-lookup"><span data-stu-id="d1005-228">This property is inherited from [**Win32\_TerminalSetting**](win32-terminalsetting.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d1005-229">備註</span><span class="sxs-lookup"><span data-stu-id="d1005-229">Remarks</span></span>

<span data-ttu-id="d1005-230">請注意，與主控台會話相關聯的 Winstations 無法存取此類別的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="d1005-230">Be aware that Winstations that are associated with the console session cannot access the methods and properties of this class.</span></span> <span data-ttu-id="d1005-231">如果嘗試將 "Console" 指定為 **TerminalName** 屬性的值，則此物件的方法會傳回 **\_ \_ 不 \_ 支援的 WBEM E**。</span><span class="sxs-lookup"><span data-stu-id="d1005-231">If an attempt is made to do so by specifying "Console" as the value of the **TerminalName** property, methods of this object return **WBEM\_E\_NOT\_SUPPORTED**.</span></span> <span data-ttu-id="d1005-232">如果視窗工作站嘗試呼叫此物件的方法來新增或修改 LocalSystem、LocalService 或 NetworkService 帳戶的安全性屬性，也會傳回此錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="d1005-232">This error code is also returned if a window station attempts to call methods of this object to add or modify the security properties of the LocalSystem, LocalService, or NetworkService accounts.</span></span>

<span data-ttu-id="d1005-233">若要連接到 \\ 根 \\ CIMV2 \\ microsoft-windows-terminalservices-gateway 命名空間，驗證層級必須包含封包隱私權。</span><span class="sxs-lookup"><span data-stu-id="d1005-233">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="d1005-234">針對 C/c + + 呼叫，這是 **RPC \_ C \_ 驗證 \_ level \_ PKT \_ 隱私權** 的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="d1005-234">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**.</span></span> <span data-ttu-id="d1005-235">針對 Visual Basic 和腳本呼叫，這是 **WbemAuthenticationLevelPktPrivacy** 或 "pktPrivacy" 的驗證層級，其值為6。</span><span class="sxs-lookup"><span data-stu-id="d1005-235">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="d1005-236">下列 Visual Basic Scripting Edition (VBScript) 範例示範如何連接到具有封包隱私權的遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="d1005-236">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="d1005-237">受控物件格式 (MOF) 檔包含 Windows Management Instrumentation (WMI) 類別的定義。</span><span class="sxs-lookup"><span data-stu-id="d1005-237">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d1005-238">MOF 檔案不會安裝為 Microsoft Windows 軟體開發套件 (SDK) 的一部分。</span><span class="sxs-lookup"><span data-stu-id="d1005-238">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d1005-239">當您使用伺服器管理員新增相關聯的角色時，它們會安裝在伺服器上。</span><span class="sxs-lookup"><span data-stu-id="d1005-239">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d1005-240">如需 MOF 檔案的詳細資訊，請參閱 [受控物件格式 (mof) ](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="d1005-240">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1005-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1005-241">Requirements</span></span>



| <span data-ttu-id="d1005-242">需求</span><span class="sxs-lookup"><span data-stu-id="d1005-242">Requirement</span></span> | <span data-ttu-id="d1005-243">值</span><span class="sxs-lookup"><span data-stu-id="d1005-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1005-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d1005-244">Minimum supported client</span></span><br/> | <span data-ttu-id="d1005-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d1005-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d1005-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d1005-246">Minimum supported server</span></span><br/> | <span data-ttu-id="d1005-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d1005-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d1005-248">命名空間</span><span class="sxs-lookup"><span data-stu-id="d1005-248">Namespace</span></span><br/>                | <span data-ttu-id="d1005-249">根 \\ CIMv2 \\ microsoft-windows-terminalservices-gateway</span><span class="sxs-lookup"><span data-stu-id="d1005-249">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="d1005-250">MOF</span><span class="sxs-lookup"><span data-stu-id="d1005-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1005-251"><dt>TSCfgWmi mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1005-251"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1005-252">DLL</span><span class="sxs-lookup"><span data-stu-id="d1005-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1005-253"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1005-253"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1005-254">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1005-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1005-255">**Win32 \_ TerminalSetting**</span><span class="sxs-lookup"><span data-stu-id="d1005-255">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> </dl>

 

