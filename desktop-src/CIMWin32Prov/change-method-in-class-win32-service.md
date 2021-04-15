---
description: 修改 Win32 \_ 服務。
ms.assetid: b32753c5-8fcf-44ee-a95f-e4f6076e0f28
ms.tgt_platform: multiple
title: 'Win32_Service 類別的 Change 方法 (Mbnapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 321b27239114fc86861c0360d507db6c8c520a9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510642"
---
# <a name="change-method-of-the-win32_service-class-mbnapih"></a>Win32_Service 類別的 Change 方法 (Mbnapi) 

**變更** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ 服務**](win32-service.md)。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Change(
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint32  ServiceType,
  [in] uint32  ErrorControl,
  [in] string  StartMode,
  [in] boolean DesktopInteract,
  [in] string  StartName,
  [in] string  StartPassword,
  [in] string  LoadOrderGroup,
  [in] string  LoadOrderGroupDependencies[],
  [in] string  ServiceDependencies[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DisplayName* \[在\]
</dt> <dd>

服務的顯示名稱。 這個字串的最大長度為 256 個字元。 服務控制管理員中的名稱會保留大小寫。 *DisplayName* 比較一律不區分大小寫。

條件約束：接受與 **Name** 屬性相同的值。

範例： "Atdisk"。

</dd> <dt>

*路徑名稱* \[在\]
</dt> <dd>

執行服務之可執行檔的完整路徑，例如「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。

</dd> <dt>

*ServiceType* \[在\]
</dt> <dd>

提供給呼叫它們之進程的服務類型。

<dt>

1 (0x1) 
</dt> <dd>

核心驅動程式

</dd> <dt>

2 (0x2) 
</dt> <dd>

檔案系統驅動程式

</dd> <dt>

4 (0x4) 
</dt> <dd>

配接器

</dd> <dt>

8 (0x8) 
</dt> <dd>

辨識器驅動程式

</dd> <dt>

16 (0x10) 
</dt> <dd>

自有進程

</dd> <dt>

32 (0x20) 
</dt> <dd>

共用進程

</dd> <dt>

256 (0x100)
</dt> <dd>

互動式進程

</dd> </dl> </dd> <dt>

*ErrorControl* \[在\]
</dt> <dd>

當此服務在啟動期間無法啟動時的錯誤嚴重性。 值指出如果發生失敗，啟動程式所採取的動作。 系統會記錄所有錯誤。

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** (0) 


</dt> <dd>

不通知使用者。

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (1) 


</dt> <dd>

一般。 通知使用者。

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** (2) 


</dt> <dd>

系統會重新開機，並使用上一個良好的設定。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (3) 


</dt> <dd>

系統嘗試以正確的組態重新啟動。

</dd> </dl> </dd> <dt>

*StartMode* \[在\]
</dt> <dd>

Windows 基底服務的啟動模式。 如需詳細資訊，請參閱＜備註＞一節。

<dt>

Boot
</dt> <dd>

作業系統載入器啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

系統
</dt> <dd>

由作業系統初始化程式啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

自動
</dt> <dd>

服務控制管理員在系統啟動期間自動啟動的服務。

</dd> <dt>

手動
</dt> <dd>

當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。

</dd> <dt>

Disabled
</dt> <dd>

無法再啟動的服務。

</dd> </dl> </dd> <dt>

*DesktopInteract* \[在\]
</dt> <dd>

若 **為 True**，則服務可以建立或與桌面上的視窗進行通訊。

</dd> <dt>

*StartName* \[在\]
</dt> <dd>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱可能採用 DomainName 使用者名稱或的形式 \\ 。 \\使用者。 服務進程會在執行時使用這兩種形式的其中一種來記錄。 如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。 如果指定 **Null** ，此服務將會以 LocalSystem 帳戶的身分登入。 若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。 如果指定了 **Null** ，驅動程式就會根據服務名稱（例如 "DWDOM Admin"），以 i/o 系統建立的預設物件名稱執行 \\ 。

您也可以使用 (UPN) 格式的使用者主體名稱來指定 **StartName**，例如 *Username@DomainName* 。

</dd> <dt>

*StartPassword* \[在\]
</dt> <dd>

*StartName* 參數所指定之帳戶名稱的密碼。 如果您不變更密碼，請指定 **Null** 。 如果此服務沒有密碼，請指定空字串。

> [!Note]  
> 將服務從本機系統變更為網路，或從網路變更為本機系統時， *StartPassword* 必須是空字串 ( "" ) 而非 **Null**。

 

</dd> <dt>

*LoadOrderGroup* \[在\]
</dt> <dd>

與其相關聯的組名。 載入順序群組包含在系統登錄中，並決定將服務載入作業系統的順序。 如果指標為 **Null**，或指向空字串，則服務不屬於群組。 如需詳細資訊，請參閱＜備註＞一節。

群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。 [載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。 系統登錄中的載入順序群組清單位於：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[在\]
</dt> <dd>

必須在此服務啟動之前啟動的載入順序群組清單。 陣列是雙重以 **null** 終止的。 如果指標為 **Null**，或指向空字串，則服務沒有相依性。 組名的前面必須加上 **SC \_ 群組 \_ 識別碼** (定義于 Winsvc .h 檔案) 字元中，以區別它們與服務名稱，因為服務和服務群組共用相同的命名空間。 群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。

</dd> <dt>

*ServiceDependencies* \[在\]
</dt> <dd>

包含必須在此服務啟動之前啟動之服務名稱的清單。 陣列是雙重以 **Null** 終止的。 如果指標為 **Null**，或指向空字串，則服務沒有相依性。 服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

「成功」
</dt> <dd>

0

要求已被接受。

</dd> <dt>

**不支援**
</dt> <dd>

1

不支援此要求。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

使用者沒有必要的存取權。

</dd> <dt>

**相依服務正在執行**
</dt> <dd>

3

無法停止此服務，因為與它相依的其他服務正在執行中。

</dd> <dt>

**不正確服務控制**
</dt> <dd>

4

要求的控制碼無效，或是服務不接受此控制碼。

</dd> <dt>

**服務無法接受控制權**
</dt> <dd>

5

因為服務的狀態 ([**Win32 \_ BaseService**](win32-baseservice.md)，所以無法將要求的控制項程式碼傳送至服務。**State** 屬性) 等於0、1或2。

</dd> <dt>

**服務非使用中**
</dt> <dd>

6

尚未啟動服務。

</dd> <dt>

**服務要求超時**
</dt> <dd>

7

服務並未及時回應啟動要求。

</dd> <dt>

**未知的失敗**
</dt> <dd>

8

啟動服務時發生未知的錯誤。

</dd> <dt>

**找不到路徑**
</dt> <dd>

9

找不到服務可執行檔的目錄路徑。

</dd> <dt>

**服務已在執行**
</dt> <dd>

10

服務已在執行中。

</dd> <dt>

**服務資料庫已鎖定**
</dt> <dd>

11

要加入新服務的資料庫已被鎖定。

</dd> <dt>

**服務相依性已刪除**
</dt> <dd>

12

這項服務所依賴的相依性已從系統中移除。

</dd> <dt>

**服務相依性失敗**
</dt> <dd>

13

服務在相依的服務中找不到所需的服務。

</dd> <dt>

**服務已停用**
</dt> <dd>

14

已經從系統中停用服務。

</dd> <dt>

**服務登入失敗**
</dt> <dd>

15

此服務未通過驗證，無法在系統上執行。

</dd> <dt>

**已標示為要刪除的服務**
</dt> <dd>

16

這項服務正在從系統中移除。

</dd> <dt>

**服務無線程**
</dt> <dd>

17

服務沒有執行執行緒。

</dd> <dt>

**狀態迴圈相依性**
</dt> <dd>

18

服務會在啟動時有迴圈相依性。

</dd> <dt>

**狀態重複名稱**
</dt> <dd>

19

服務正在相同名稱下執行。

</dd> <dt>

**狀態不正確名稱**
</dt> <dd>

20

服務名稱包含不正確字元。

</dd> <dt>

**狀態不正確參數**
</dt> <dd>

21

傳遞給服務的參數無效。

</dd> <dt>

**狀態不正確服務帳戶**
</dt> <dd>

22

用來執行此服務的帳戶無效，或缺少執行服務的許可權。

</dd> <dt>

**狀態服務存在**
</dt> <dd>

23

服務存在於系統可使用之服務的資料庫中。

</dd> <dt>

**服務已暫停**
</dt> <dd>

24

服務目前在系統中暫停。

</dd> <dt>

**其他**
</dt> <dd>

25 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

當電腦啟動時，所有自動啟動的服務也會啟動。 有時候，其中一項服務可能無法與電腦一併啟動。 當服務在系統啟動期間失敗時，電腦會根據服務錯誤控制程式代碼的值採取動作。

大部分的服務都是使用一般的錯誤控制程式代碼安裝。 有些例外狀況（使用忽略錯誤碼來安裝）包括：

-   檔案複寫服務
-   智慧卡
-   次要登入
-   WMI

若為使用忽略錯誤碼所安裝的服務，則不會向使用者提供服務失敗的通知。 如果您偏好無法啟動服務的螢幕通知，您可以使用 WMI 來變更錯誤控制程式代碼。 錯誤控制代碼僅適用于電腦啟動;如果您在執行電腦之後停止然後嘗試重新開機服務，則不會使用錯誤控制代碼。

有時，您可能需要變更指定服務執行時所使用的帳戶。 例如，您可以在系統管理帳戶下執行服務。 因為這可能會產生安全性弱點，您可能會將服務切換為具有較少許可權的帳戶。 或者，您可能在即將刪除的帳戶下執行服務，或者您可能想要確保在所有伺服器上，某些服務會在特定帳戶下執行。 您可以使用 [**Win32 \_ 服務**](win32-service.md)類別的 **Change** 方法，將服務設定為在指定的使用者帳戶下執行。 選取帳戶時，請記住下列事項：

-   作為服務帳戶使用的帳戶必須具有以服務方式登入的許可權。 您可以使用群組原則來授與此許可權。
-   作為服務帳戶使用的帳戶不應該是本機、網域或企業系統管理員群組的成員。
-   服務的每個實例都應該在唯一的使用者帳戶下執行。 這可提供額外的安全性，並可讓您進行個別服務實例的審核。
-   如果服務是互動式的，則服務必須在 LocalSystem 帳戶下執行。

    LocalSystem 是必要的，因為一次只有一個視窗工作站 (WinSta0) 可以是可見和互動式的。 如果服務是以 LocalSystem 以外的帳戶執行，則會在 0x03e7 $ \\ Default 視窗工作站中執行，這是不可見的視窗。 在此視窗工作站中執行的服務無法接收輸入或顯示輸出。

當您將帳戶指派給服務時，SCM 需要該帳戶的正確密碼，才能進行指派。 如果您提供不正確的密碼，SCM 會拒絕該帳戶。 如果您使用 LocalSystem、LocalService 或 NetworkService 帳戶設定服務帳戶，則不需要提供帳戶密碼，因為這些帳戶沒有密碼。

SCM 會將帳戶密碼儲存在服務資料庫中。 不過，在指派密碼之後，SCM 無法確保儲存在服務資料庫中的密碼和指派給使用者帳戶的密碼 Active Directory 繼續相符。 因此，可能會發生類似下列的情況：

-   您可以設定在特定使用者帳戶下執行服務。
-   服務會使用目前的帳戶密碼在該帳戶下啟動。
-   您可以變更使用者帳戶的密碼。
-   服務會繼續執行。 但是，如果服務停止，您就無法將它重新開機，因為 SCM 會繼續使用舊的、不正確密碼。 變更 Active Directory 中的密碼並不會變更儲存在服務資料庫中的密碼。

如果您在一般使用者帳戶下執行服務，則每次使用者帳戶密碼變更時，都必須更新這些服務密碼。 如果您不確定哪些服務是在該帳戶下執行，或是哪些電腦的服務是在該帳戶下執行，這可能特別耗時。 幸運的是，您可以使用 WMI 來檢查所有電腦上的服務帳戶，如有必要，也可以變更服務帳戶密碼。

[**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)參數代表定義執行相依性的一組系統服務。 服務必須依「載入順序」群組所指定的順序起始，因為服務會彼此相依。 這些相依服務需要有前面的服務才能正確運作。

若要將服務從網路服務變更為本機系統， *StartName* 和 *StartPassword* 參數應該具有下列值：


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



若要將服務從本機系統服務變更為網路， *StartName* 和 *StartPassword* 參數應該具有下列值：


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
```



## <a name="examples"></a>範例

下列 VBScript 會將服務的服務帳戶從指定的使用者帳戶，變更為 LocalSystem。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objService in colServices
 errServiceChange = objService.Change( , , , , , , ".\LocalSystem" , "")
Next
```



下列 VBScript 會變更在 Netsvc 下執行之所有腳本的服務帳戶密碼。


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\Root\CIMv2")
Set colServiceList = objWMIService.ExecQuery("SELECT * FROM Win32_Service WHERE StartName = '.\\NetSvc'")
For Each objservice in colServiceList
 errReturn = objService.Change( , , , , , , , "password")
Next
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| 標頭<br/>                   | <dl> <dt>Mbnapi。h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[作業系統類別](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[**Win32 \_ 服務**](win32-service.md)
</dt> <dt>

[WMI 工作：服務](/windows/desktop/WmiSdk/wmi-tasks--services)
</dt> </dl>

 

