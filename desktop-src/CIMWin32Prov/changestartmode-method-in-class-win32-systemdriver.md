---
description: 修改 Win32 >systemdriver 服務的啟動模式 \_ 。
ms.assetid: 34f4e0ac-d8a0-4be7-8c84-0252e50db441
ms.tgt_platform: multiple
title: Win32_SystemDriver 類別的 ChangeStartMode 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriver.ChangeStartMode
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2e2067ae7da8a6f112671237ebc7f77dd26644c5e0b2fa0b77a443c160468581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959127"
---
# <a name="changestartmode-method-of-the-win32_systemdriver-class"></a>Win32 >systemdriver 類別的 ChangeStartMode 方法 \_

**ChangeStartMode** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會修改 [**Win32 \_ >systemdriver**](win32-systemdriver.md)服務的啟動模式。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 ChangeStartMode(
  [in] string StartMode = Auto Start
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*StartMode* \[在\]
</dt> <dd>

Windows 基礎服務的啟動模式。

<dt>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>

<span id="Boot_Start"></span><span id="boot_start"></span><span id="BOOT_START"></span>**開機開始 ( 「開機」** ) 


</dt> <dd>

作業系統載入器啟動的設備磁碟機。 這個值只適用於驅動程式服務。

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**System** ( "system" ) 


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

當進程呼叫 [**StartService**](startservice-method-in-class-win32-systemdriver.md) 方法時，服務控制管理員要啟動的服務。

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**停用** ( [已停用] ) 


</dt> <dd>

無法再啟動的服務。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

如果成功修改服務，則傳回 0 (零) 的值; 如果不支援要求，則傳回 1 (一個) ，以及指出錯誤的其他任何數位。

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

 

