---
description: 建立新的服務。
ms.assetid: e000b896-3b49-4650-b706-548592cfe721
ms.tgt_platform: multiple
title: Win32_BaseService 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 827a82bf76fe78b86f97efa3aa01e0ae1106cd81430952b5d5b2849b5b3dd492
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547428"
---
# <a name="create-method-of-the-win32_baseservice-class"></a>Win32 BaseService 類別的 Create 方法 \_

**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立新的服務。 *LoadOrderGroup* 參數代表定義執行相依性的系統服務群組。 服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。 這些相依服務需要有前面的服務才能正確運作。

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

提供給呼叫它們的進程的服務類型。 此值為點陣圖。

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>**核心驅動程式** (1) 


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>**檔案系統驅動程式** (2) 


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>**介面卡** (4) 


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>辨識 **器驅動程式** (8) 


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span> (16) 的 **進程**


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>**共用進程** (32) 


</dt> <dd></dd> <dt>

256
</dt> <dd>

互動式進程

</dd> <dt>




</dt> <dd></dd> </dl> </dd> <dt>

*ErrorControl* \[在\]
</dt> <dd>

**建立** 方法無法啟動時的錯誤嚴重性。 值指出如果發生失敗，啟動程式所採取的動作。 系統會記錄所有錯誤。

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**忽略** (0) 


</dt> <dd>

不通知使用者。

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (1) 


</dt> <dd>

通知使用者。

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**嚴重** (2) 


</dt> <dd>

使用上次的正確組態重新啟動系統。

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**重大** (3) 


</dt> <dd>

系統嘗試以良好的設定開始。

</dd> </dl> </dd> <dt>

*StartMode* \[在\]
</dt> <dd>

Windows 基礎服務的啟動模式。

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) 


</dt> <dd>

作業系統載入器啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>

<span id="System_Start"></span><span id="system_start"></span><span id="SYSTEM_START"></span>**系統啟動** ( "system" ) 


</dt> <dd>

由作業系統初始化程式啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>

<span id="Auto_Start"></span><span id="auto_start"></span><span id="AUTO_START"></span>**自動啟動 ( 「自動」** ) 


</dt> <dd>

要由服務控制管理員在系統啟動期間自動啟動的服務。

</dd> <dt>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>

<span id="Demand_Start"></span><span id="demand_start"></span><span id="DEMAND_START"></span>**需求開始 ( 「手動」** ) 


</dt> <dd>

當進程呼叫 [**StartService**](startservice-method-in-class-win32-service.md) 方法時，服務控制管理員要啟動的服務。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) 


</dt> <dd>

無法再啟動的服務。

</dd> </dl> </dd> <dt>

*DesktopInteract* \[在\]
</dt> <dd>

若 **為 true**，則服務可以在桌面上建立 windows 或與其通訊。

</dd> <dt>

*StartName* \[在\]
</dt> <dd>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱的格式可能是 "DomainName \\ Username"。 服務進程會在執行時使用這兩種形式的其中一種來記錄。 如果帳戶屬於內建網域，則為」。 \\您可以指定使用者名稱」。 如果指定 **Null** ，則服務會以 LocalSystem 帳戶的身分登入。 若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。 如果指定了 **Null** ，驅動程式就會以服務名稱為基礎，以預設物件名稱（由 i/o 系統建立）來執行。 範例： DWDOM \\ Admin。

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

必須在此服務之前啟動的載入順序群組陣列。 陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。 在 Visual Basic 或腳本中，您可以傳遞 vbArray。 如果指標為 **Null** 或指向空字串，則服務沒有相依性。 組名必須以 \_ Winsvc 中定義的 SC 群組識別碼作為前置詞 \_ ， (在 .h 檔案中定義) 字元，以與服務名稱區別，因為服務和服務群組會共用相同的命名空間。 群組的相依性表示，如果在嘗試啟動群組的所有成員之後，此服務至少有一個成員在執行中，就可以執行此服務。

</dd> <dt>

*ServiceDependencies* \[在\]
</dt> <dd>

陣列，包含在此服務啟動之前必須啟動之服務的名稱。 陣列中的每個專案都是以 **null** 分隔，而且清單會以兩個 **null** 值終止。 在 Visual Basic 或腳本中，您可以傳遞 vbArray。 如果指標為 **Null**，或指向空字串，則服務沒有相依性。 服務的相依性表示，只有在其相依的服務正在執行時，才能執行此服務。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或任何其他值以表示錯誤。

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

互動式進程。

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

已經從系統中移除這個服務所依賴的相依性。

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

服務沒有執行緒。

</dd> <dt>

**狀態迴圈相依性**
</dt> <dd>

18

啟動服務時有循環的相依性。

</dd> <dt>

**狀態重複名稱**
</dt> <dd>

19

有一個服務在相同名稱下執行。

</dd> <dt>

**狀態不正確名稱**
</dt> <dd>

20

服務名稱中有不正確字元。

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

[**Win32 \_ BaseService**](win32-baseservice.md)
</dt> </dl>

 

