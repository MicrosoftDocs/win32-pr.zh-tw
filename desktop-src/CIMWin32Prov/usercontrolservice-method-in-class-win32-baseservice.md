---
description: 嘗試將使用者定義的控制項程式碼傳送至服務。
ms.assetid: d181dbf8-e1ad-47b2-9e64-4aabc77e64bd
ms.tgt_platform: multiple
title: Win32_BaseService 類別的 UserControlService 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService.UserControlService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 55647524c8ba561716441976fe6654b933e1900b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847531"
---
# <a name="usercontrolservice-method-of-the-win32_baseservice-class"></a>Win32 BaseService 類別的 UserControlService 方法 \_

[WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試將使用者定義的控制項程式碼傳送至服務。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 UserControlService(
  [in] uint8 ControlCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ControlCode* \[在\]
</dt> <dd>

值，指定服務的控制項命令。 例如，控制命令是「暫停」或「繼續」命令。 值可以是預先定義的程式碼，或是服務定義的值和動作。 以下是預先定義的控制項代碼：

<dt>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>

<span id="SERVICE_CONTROL_CONTINUE"></span><span id="service_control_continue"></span>**服務 \_ 控制 \_ 繼續**


</dt> <dd>

通知暫停的服務繼續。

</dd> <dt>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>

<span id="SERVICE_CONTROL_INTERROGATE"></span><span id="service_control_interrogate"></span>**服務 \_ 控制 \_ 詢問**


</dt> <dd>

通知服務向服務控制管理員報告目前的狀態資訊。

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>

<span id="SERVICE_CONTROL_NETBINDADD"></span><span id="service_control_netbindadd"></span>**服務 \_ 控制 \_ NETBINDADD**


</dt> <dd>

通知網路服務有系結的新元件。

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>

<span id="SERVICE_CONTROL_NETBINDDISABLE"></span><span id="service_control_netbinddisable"></span>**服務 \_ 控制 \_ NETBINDDISABLE**


</dt> <dd>

通知網路服務，其中一個系結已停用。

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>

<span id="SERVICE_CONTROL_NETBINDENABLE"></span><span id="service_control_netbindenable"></span>**服務 \_ 控制 \_ NETBINDENABLE**


</dt> <dd>

通知網路服務已停用已停用的系結。

</dd> <dt>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>

<span id="SERVICE_CONTROL_NETBINDREMOVE"></span><span id="service_control_netbindremove"></span>**服務 \_ 控制 \_ NETBINDREMOVE**


</dt> <dd>

通知網路服務已移除系結的元件。

</dd> <dt>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>

<span id="SERVICE_CONTROL_PARAMCHANGE"></span><span id="service_control_paramchange"></span>**服務 \_ 控制 \_ PARAMCHANGE**


</dt> <dd>

通知服務其啟動參數已變更。

</dd> <dt>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>

<span id="SERVICE_CONTROL_PAUSE"></span><span id="service_control_pause"></span>**服務 \_ 控制 \_ 暫停**


</dt> <dd>

通知服務暫停。

</dd> <dt>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>

<span id="SERVICE_CONTROL_STOP"></span><span id="service_control_stop"></span>**服務 \_ 控制 \_ 停止**


</dt> <dd>

通知服務停止。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。

<dl> <dt>

「成功」
</dt> <dd>

0

已接受要求。

</dd> <dt>

**不支援**
</dt> <dd>

1

不支援此要求。

</dd> <dt>

**拒絕存取**
</dt> <dd>

2

使用者沒有必要的存取權限。

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

該服務已啟動。

</dd> <dt>

**服務要求超時**
</dt> <dd>

7

服務不會快速回應啟動要求。

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

這項服務所依賴的相依性會從系統中移除。

</dd> <dt>

**服務相依性失敗**
</dt> <dd>

13

服務在相依的服務中找不到所需的服務。

</dd> <dt>

**服務已停用**
</dt> <dd>

14

系統會停用服務。

</dd> <dt>

**服務登入失敗**
</dt> <dd>

15

此服務未通過驗證，無法在系統上執行。

</dd> <dt>

**已標示為要刪除的服務**
</dt> <dd>

16

正在從系統中移除此服務。

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

執行此服務的帳戶無效，或沒有執行此服務的許可權。

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

 

