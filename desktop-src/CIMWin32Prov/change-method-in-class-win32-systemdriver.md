---
description: 修改 Win32 \_ >systemdriver 服務。
ms.assetid: 61ee3297-2a66-466e-bdba-74d683f3ea70
ms.tgt_platform: multiple
title: 'Win32_SystemDriver 類別的 Change 方法 (Mbnapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Change
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 96ff327e84d3a5b6c66011506c162810f0fcc91d0cafe4053266aa8928f6e5a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925108"
---
# <a name="change-method-of-the-win32_systemdriver-class"></a>Win32 >systemdriver 類別的 Change 方法 \_

**變更** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ >systemdriver**](win32-systemdriver.md)服務。 [**Win32 \_ LoadOrderGroup**](win32-loadordergroup.md)參數代表定義執行相依性的系統服務群組。 服務必須依照載入順序群組所指定的順序起始，因為服務彼此相依。 這些相依服務需要有前面的服務才能正確運作。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Change(
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

*DisplayName* \[在\]
</dt> <dd>

服務的顯示名稱。 這個字串的最大長度為 256 個字元。 服務控制管理員中的名稱會保留大小寫。 *DisplayName* 比較一律不區分大小寫。

條件約束：接受與 *Name* 參數相同的值。

範例： "Atdisk"

</dd> <dt>

*路徑名稱* \[在\]
</dt> <dd>

可執行檔的完整路徑，此檔案可執行服務。

範例： *\\ SystemRoot \\ System32 \\ 驅動程式 \\afd.sys*

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

如果這項服務在啟動期間無法啟動時的錯誤嚴重性。 值指出如果發生失敗，啟動程式所採取的動作。 系統會記錄所有錯誤。

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

Windows 基底服務的啟動模式。

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機啟動**


</dt> <dd>

作業系統載入器啟動的設備磁碟機。

</dd> <dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機啟動**


</dt> <dd>

作業系統載入器啟動的設備磁碟機。

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**系統啟動**


</dt> <dd>

由作業系統初始化程式啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動**


</dt> <dd>

服務控制管理員在系統啟動期間自動啟動的服務。

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始**


</dt> <dd>

當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員會啟動服務。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**


</dt> <dd>

無法啟動的服務。

</dd> </dl> </dd> <dt>

*DesktopInteract* \[在\]
</dt> <dd>

值，如果 **為 True**，服務可以建立或與桌面上的視窗進行通訊。

</dd> <dt>

*StartName* \[在\]
</dt> <dd>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱可能採用 DomainName 使用者名稱或的形式 \\ 。 \\使用者。 當它執行時，會使用這兩種形式的其中一種來記錄服務進程。 如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。 如果指定了空字串，服務就會以 LocalSystem 帳戶的身分登入。 若是核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱，例如， \\ FileSystem \\ Rdr 或 \\ driver \\ Xns) ， (i/o) 系統用來載入設備磁碟機的輸入和輸出。 如果指定 **Null** ，驅動程式會以預設物件名稱執行，系統會根據服務名稱（例如，DWDOM Admin）來建立 i/o 系統 \\ 。

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

與其相關聯的組名。 載入順序群組包含在系統登錄中，並決定將服務載入作業系統的順序。 如果指標為 **Null**，或指向空字串，則服務不屬於群組。 群組之間的相依性應該列在 *LoadOrderGroupDependencies* 參數中。 [載入順序群組] 清單中的服務會先啟動，後面接著群組中不是 [載入順序群組] 清單中的服務，然後是不屬於群組的服務。 系統登錄中的載入順序群組清單位於：

**HKEY \_本機 \_ 電腦** \\ **系統** \\ **CurrentControlSet** \\ **控制項** \\ **ServiceGroupOrder**

</dd> <dt>

*LoadOrderGroupDependencies* \[在\]
</dt> <dd>

必須在此服務啟動之前啟動的載入順序群組清單。 陣列是雙重以 **null** 終止的。 如果指標為 **Null**，或指向空字串，則服務沒有相依性。 組名的前面必須加上 **SC \_ 群組 \_ 識別碼** (在 WinSvc .h 檔案中定義) 字元，以區別它們與服務名稱，因為服務和服務群組會共用相同的命名空間。 群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。

</dd> <dt>

*ServiceDependencies* \[在\]
</dt> <dd>

包含必須在此服務啟動之前啟動之服務名稱的清單。 陣列是雙重以 **null** 終止的。 如果指標為 **Null**，或指向空字串，則服務沒有相依性。 服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果已成功修改服務，則傳回零 (0) ，如果要求不受支援則為 1 (一個) ，以及表示錯誤的其他任何數位。

<dl> <dt>

**成功** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

正在執行 (3) 的 **相依服務**
</dt> <dt>

**不正確服務控制** (4) 
</dt> <dt>

**服務無法接受 Control** (5) 
</dt> <dt>

**服務非** 使用中 (6) 
</dt> <dt>

**服務要求超時** (7) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

 (9) **找不到路徑**
</dt> <dt>

**服務已** 在執行 (10) 
</dt> <dt>

**服務資料庫已鎖定** (11) 
</dt> <dt>

**服務相依性已刪除** (12) 
</dt> <dt>

**服務** 相依性失敗 (13) 
</dt> <dt>

**服務已停用** (14) 
</dt> <dt>

**服務登入失敗** (15) 
</dt> <dt>

已 **標示為要刪除的服務** (16) 
</dt> <dt>

**服務沒有線程** (17) 
</dt> <dt>

**狀態迴圈** 相依性 (18) 
</dt> <dt>

**狀態重複名稱** (19) 
</dt> <dt>

**狀態不正確名稱** (20) 
</dt> <dt>

**狀態不正確參數** (21) 
</dt> <dt>

**狀態不正確服務帳戶** (22) 
</dt> <dt>

**狀態服務存在** (23) 
</dt> <dt>

**服務已暫停** (24) 
</dt> <dt>

**其他** (25 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

若要將服務從網路服務變更為本機系統，請使用下列值作為 *StartName* 和 *StartPassword* 參數：


```C++
StartName = "LocalSystem"
StartPassword = "" // - empty string, not NULL
```



若要將服務從本機系統服務變更為 network service，請針對 *StartName* 和 *StartPassword* 參數使用下列值：


```C++
StartName = "NT AUTHORITY\NetworkService"
StartPassword = "" // - empty string, not NULL
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

[**Win32 \_ >systemdriver**](win32-systemdriver.md)
</dt> </dl>

 

