---
description: 建立由系統驅動程式管理的新服務。
ms.assetid: 212c88eb-f26d-4b07-b8fe-8508050c97fc
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a85b18a04672f63c4f1fd8fe4fa386ffb4e3094e817b53a20af9887a84748a3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080152"
---
# <a name="create-method-of-the-win32_systemdriver-class"></a>Win32 >systemdriver 類別的 Create 方法 \_

**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會建立由系統驅動程式管理的新服務。 *Win32 \_ LoadOrderGroup* 參數代表定義執行相依性的系統服務群組。 服務必須依「載入順序」群組所指定的順序起始，因為服務彼此相依。 這些相依服務需要有前面的服務才能正確運作。

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

**建立** 方法無法啟動時的錯誤嚴重性。 此值表示如果發生失敗，啟動程式所採取的動作。 系統會記錄所有錯誤。

<dt>

0
</dt> <dd>

拒絕

不通知使用者。

</dd> <dt>

1
</dt> <dd>

"Normal"

通知使用者。

</dd> <dt>

2
</dt> <dd>

嚴格

使用上次的正確組態重新啟動系統。

</dd> <dt>

3
</dt> <dd>

必需

系統嘗試以良好的設定開始。

</dd> </dl> </dd> <dt>

*StartMode* \[在\]
</dt> <dd>

Windows 基礎服務的啟動模式。

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**引導**


</dt> <dd>

作業系統載入器啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**系統**


</dt> <dd>

由作業系統初始化程式啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>

<span id="Automatic"></span><span id="automatic"></span><span id="AUTOMATIC"></span>**自動**


</dt> <dd>

服務控制管理員在系統啟動期間自動啟動的服務。

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**手動**


</dt> <dd>

當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員要啟動的服務。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**禁用**


</dt> <dd>

無法再啟動的服務。

</dd> </dl> </dd> <dt>

*DesktopInteract* \[在\]
</dt> <dd>

若 **為 true**，則服務可以建立或與桌面上的視窗進行通訊。

</dd> <dt>

*StartName* \[在\]
</dt> <dd>

用來執行服務的帳戶名稱。 根據服務類型而定，帳戶名稱的格式可以是 DomainName \\ 使用者名稱或使用者主體名稱 (UPN) 格式 (Username@DomainName) 。 服務進程會在執行時使用這兩種形式的其中一種來記錄。 如果帳戶屬於內建網域，則為。 \\您可以指定使用者名稱。 如果指定 **Null** ，則服務會以 LocalSystem 帳戶的身分登入。 若為核心或系統層級的驅動程式， *StartName* 會包含驅動程式物件名稱 (也就是 \\ 檔案系統 \\ Rdr 或 \\ 驅動程式 \\ Xns) 輸入和輸出 (i/o) 系統用來載入設備磁碟機。 如果指定了 **Null** ，驅動程式就會以服務名稱為基礎，以預設物件名稱（由 i/o 系統建立）來執行。

範例： DWDOM \\ 管理員

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

如果成功建立服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指定錯誤的任何其他數位。

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

[**Win32 \_ >systemdriver**](win32-systemdriver.md)
</dt> </dl>

 

