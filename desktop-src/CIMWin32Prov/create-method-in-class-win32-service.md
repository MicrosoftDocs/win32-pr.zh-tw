---
description: Win32_Service 類別的建立方法 (CIMWin32 WMI 提供者) -建立新的系統服務。
ms.assetid: 164e9065-bb0d-4c93-a9fe-c86db1ea7cb7
ms.tgt_platform: multiple
title: 'Win32_Service 類別的建立方法 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3baa83179ac6c5040aa85a5fcf2af0d932a4c8e9cdc2d10742c5c8aaa66abb5f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003798"
---
# <a name="create-method-of-the-win32_service-class-cimwin32-wmi-providers"></a>Win32_Service 類別的建立方法 (CIMWin32 WMI 提供者) 

**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立新的系統服務。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Create(
  [in] string  Name,
  [in] string  DisplayName,
  [in] string  PathName,
  [in] uint8   ServiceType,
  [in] uint8   ErrorControl,
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

*名稱* \[在\]
</dt> <dd>

要安裝至 **Create** 方法的服務名稱。 字串長度上限為256個字元。 服務控制管理員資料庫會保留字元的大小寫，但服務名稱比較一律不區分大小寫。 正斜線 (/) 和雙反斜線 (\\) 是不正確服務名稱字元。

</dd> <dt>

*DisplayName* \[在\]
</dt> <dd>

服務的顯示名稱。 這個字串的最大長度為 256 個字元。 服務控制管理員中的名稱會保留大小寫。 *DisplayName* 比較一律不區分大小寫。

條件約束：接受與 *Name* 參數相同的值。

範例： "Atdisk"。

</dd> <dt>

*路徑名稱* \[在\]
</dt> <dd>

可執行檔的完整路徑，該檔案可執行服務。

範例：「 \\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys」。

</dd> <dt>

*ServiceType* \[在\]
</dt> <dd>

提供給呼叫它們的進程的服務類型。

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

**建立** 方法無法啟動時的錯誤嚴重性。 值指出如果發生失敗，啟動程式所採取的動作。 系統會記錄所有錯誤。

<dt>

0
</dt> <dd>

不通知使用者。

</dd> <dt>

1
</dt> <dd>

通知使用者。

</dd> <dt>

2
</dt> <dd>

使用上次的正確組態重新啟動系統。

</dd> <dt>

3
</dt> <dd>

系統嘗試以良好的設定開始。

</dd> </dl> </dd> <dt>

*StartMode* \[在\]
</dt> <dd>

Windows 基礎服務的啟動模式。

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

已停用
</dt> <dd>

無法再啟動的服務。

</dd> </dl> </dd> <dt>

*DesktopInteract* \[在\]
</dt> <dd>

若 **為 true**，則服務可以在桌面上建立 windows 或與其通訊。

</dd> <dt>

*StartName* \[在\]
</dt> <dd>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱的格式可以是 DomainName \\ 使用者名稱或使用者主體名稱 (UPN) 格式 (Username@DomainName) 。 服務進程會在執行時使用這兩種形式的其中一種來記錄。 如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。 如果指定 **Null** ，則服務會以 LocalSystem 帳戶的身分登入。 若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) ，) 系統用來載入設備磁碟機的輸入和輸出 (i/o。 如果指定了 **Null** ，驅動程式就會以服務名稱為基礎，以預設物件名稱（由 i/o 系統建立）來執行。 範例： DWDOM \\ Admin。

</dd> <dt>

*StartPassword* \[在\]
</dt> <dd>

*StartName* 參數所指定之帳戶名稱的密碼。 如果您不變更密碼，請指定 **Null** 。 如果此服務沒有密碼，請指定空字串。

</dd> <dt>

*LoadOrderGroup* \[在\]
</dt> <dd>

與新服務相關聯的組名。 載入順序群組包含于登錄中，並決定將服務載入作業系統的順序。 如果指標為 **Null** 或指向空字串，則服務不屬於群組。 群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。 [載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。 登錄的載入順序群組清單位於：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[在\]
</dt> <dd>

必須在此服務之前啟動的載入順序群組陣列。 陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。 在 Visual Basic 或腳本中，您可以傳遞 vbArray。 如果指標為 **Null** 或指向空字串，則服務沒有相依性。 組名必須以 Winsvc 中定義的 **SC \_ 群組 \_ 識別碼** 作為前置詞， (在 .h 檔案中定義) 字元，以與服務名稱區別，因為服務和服務群組會共用相同的命名空間。 群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。

</dd> <dt>

*ServiceDependencies* \[在\]
</dt> <dd>

陣列，包含在此服務啟動之前必須啟動之服務的名稱。 陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。 在 Visual Basic 或腳本中，您可以傳遞 vbArray。 如果指標為 **Null**，或指向空字串，則服務沒有相依性。 服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**0**
</dt> <dd>

要求已被接受。

</dd> <dt>

**1**
</dt> <dd>

不支援此要求。

</dd> <dt>

**2**
</dt> <dd>

使用者沒有必要的存取權。

</dd> <dt>

**3**
</dt> <dd>

無法停止此服務，因為與它相依的其他服務正在執行中。

</dd> <dt>

**4**
</dt> <dd>

要求的控制碼無效，或是服務不接受此控制碼。

</dd> <dt>

**5**
</dt> <dd>

因為 [**Win32 \_ BaseService**](win32-baseservice.md)) 類別的服務 (**state** 屬性的狀態等於0、1或2，所以無法將要求的控制項程式碼傳送至服務。

</dd> <dt>

**6**
</dt> <dd>

尚未啟動服務。

</dd> <dt>

**7**
</dt> <dd>

服務並未及時回應啟動要求。

</dd> <dt>

**8**
</dt> <dd>

啟動服務時發生未知的錯誤。

</dd> <dt>

**9**
</dt> <dd>

找不到服務可執行檔的目錄路徑。

</dd> <dt>

**10**
</dt> <dd>

服務已在執行中。

</dd> <dt>

**11**
</dt> <dd>

要加入新服務的資料庫已被鎖定。

</dd> <dt>

**12**
</dt> <dd>

這項服務所依賴的相依性已從系統中移除。

</dd> <dt>

**13**
</dt> <dd>

服務在相依的服務中找不到所需的服務。

</dd> <dt>

**14**
</dt> <dd>

已經從系統中停用服務。

</dd> <dt>

**15**
</dt> <dd>

此服務未通過驗證，無法在系統上執行。

</dd> <dt>

**16**
</dt> <dd>

這項服務正在從系統中移除。

</dd> <dt>

**17**
</dt> <dd>

服務沒有執行執行緒。

</dd> <dt>

**達**
</dt> <dd>

服務會在啟動時有迴圈相依性。

</dd> <dt>

**診斷**
</dt> <dd>

服務正在相同名稱下執行。

</dd> <dt>

**20**
</dt> <dd>

服務名稱包含不正確字元。

</dd> <dt>

**21**
</dt> <dd>

傳遞給服務的參數無效。

</dd> <dt>

**22**
</dt> <dd>

用來執行此服務的帳戶無效，或缺少執行服務的許可權。

</dd> <dt>

**23**
</dt> <dd>

服務存在於系統可使用之服務的資料庫中。

</dd> <dt>

**24**
</dt> <dd>

服務目前在系統中暫停。

</dd> </dl>

## <a name="remarks"></a>備註

服務通常會以下列兩種方式之一進行安裝：作為作業系統安裝的一部分，或使用服務開發人員所提供的安裝程式。 不過，某些服務（特別是在內部建立的服務）可能沒有安裝程式。 在這些情況下，您可以使用 **Create** 方法以程式設計方式安裝服務。

無論名稱為何，Create 方法都不會實際建立服務;它只會安裝現有的服務。 若要使用此命令，您必須將服務可執行檔案複製到電腦，然後使用 [ **建立** ] 來安裝服務。

**Create** 方法類似于 [**變更**](change-method-in-class-win32-service.md)方法。 在這兩種情況下，服務的屬性都會作為參數傳遞給方法。 如同與 **變更** 方法搭配使用的參數，傳遞這些參數的順序很重要。

*LoadOrderGroup* 參數代表定義執行相依性的系統服務群組。 服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。 這些相依服務需要有前面的服務才能正確運作。

## <a name="examples"></a>範例

下列 VBScript 會安裝名為 DbService 的服務。


```VB
Const OWN_PROCESS = 16
Const NOT_INTERACTIVE = True
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set objService = objWMIService.Get("Win32_BaseService")
errReturn = objService.Create ("DbService", "Personnel Database", _
"c:\windows\system32\db.exe", OWN_PROCESS ,2 ,"Automatic" , _
 NOT_INTERACTIVE ,".\LocalSystem" ,"")
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
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

 

