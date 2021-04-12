---
description: 將作業提交至作業系統，以在未來指定的時間和日期執行。
ms.assetid: 9d582fbb-24cb-401d-8b77-af7671a24e6d
ms.tgt_platform: multiple
title: Win32_ScheduledJob 類別的 Create 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ScheduledJob.Create
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9f1acae94ea29d2d57b2952c0b0adc267ad3066c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317916"
---
# <a name="create-method-of-the-win32_scheduledjob-class"></a>Win32 Register-scheduledjob 類別的 Create 方法 \_

**建立** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會將作業提交至作業系統，以在未來指定的時間和日期執行。 此方法需要在提交作業的電腦上啟動排程服務。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 Create(
  [in]           string   Command,
  [in]           datetime StartTime,
  [in, optional] boolean  RunRepeatedly,
  [in, optional] uint32   DaysOfWeek,
  [in, optional] uint32   DaysOfMonth,
  [in, optional] boolean  InteractWithDesktop,
  [out]          uint32   JobId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*命令* \[在\]
</dt> <dd>

排程服務用來叫用作業的命令、批次程式或二進位檔和命令列參數的名稱。

範例： "defrag/q/f"。

</dd> <dt>

*StartTime* \[在\]
</dt> <dd>

國際標準時間 (UTC) 時間來執行工作。 格式必須為： "YYYYMMDDHHMMSS.FFFFFF"。MMMMMM (+-) OOO "，其中" YYYYMMDD "必須以" "取代 \* \* \* \* \* \* \* \* 。 例如： " \* \* \* \* \* \* \* \* 143000.000000-420" 會指定 14.30 (2:30 P.M. ) PST，並有日光節約時間生效。

StartTime 屬性值的 " (+-) OOO" 區段是本地時間轉譯目前的偏差。 偏差是 UTC 時間與當地時間之間的差異。 若要計算時區的偏差，請將您時區提前或晚于格林威治標準時間的小時數乘以60的 (GMT)  (如果您的時區是在 GMT 之前，則以小時為單位，如果您的時區晚于 gmt) ，則為負數。 如果您的時區使用日光節約時間，請在您的計算中加入額外的60。 例如，太平洋標準時區是 GMT 後八小時，因此偏差等於-420 (-8 \* 60 + 60) 當日光節約時間正在使用中時，當日光節約時間未使用時，則為-480 (-8 \* 60) 。 您也可以藉由查詢 [**Win32 \_ 時區**](win32-timezone.md) 類別的偏差屬性來判斷偏差的值。

</dd> <dt>

*RunRepeatedly* \[在中，選擇性\]
</dt> <dd>

若 **為 True**，則排程工作會在特定天數重複執行。 預設值為 **False**。

</dd> <dt>

*DaysOfWeek* \[在中，選擇性\]
</dt> <dd>

排程執行工作的周間天數;只有在 *RunRepeatedly* 參數為 **True** 時才會使用。 若要排定一周中超過一天的作業，請在邏輯 OR 中聯結適當的值。 例如，若要針對星期二和星期五排程作業， *DaysOfWeek* 的值為2或16。

<dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>

**星期一** (1) 


</dt> <dd></dd> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>

**星期二** (2) 


</dt> <dd></dd> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>

**星期三** (4) 


</dt> <dd></dd> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>

**星期四** (8) 


</dt> <dd></dd> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>

**星期五** (16) 


</dt> <dd></dd> <dt>

<span id="Saturday"></span><span id="saturday"></span><span id="SATURDAY"></span>

**星期六** (32) 


</dt> <dd></dd> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>

**星期日** (64) 


</dt> <dd></dd> </dl> </dd> <dt>

*DaysOfMonth* \[在中，選擇性\]
</dt> <dd>

排程執行作業的當月天數;只有在 *RunRepeatedly* 參數為 **True** 時才會使用。

<dt>

<span id="1"></span>

<span id="1"></span>**1** (1) 


</dt> <dd>

每月第1天

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2** (2) 


</dt> <dd>

每月第2天

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3** (4) 


</dt> <dd>

每月第3天

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4** (8) 


</dt> <dd>

每月第4天

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5** (16) 


</dt> <dd>

每月第5天

</dd> <dt>

<span id="6"></span>

<span id="6"></span>**6** (32) 


</dt> <dd>

每月第6天

</dd> <dt>

<span id="7"></span>

<span id="7"></span>**7** (64) 


</dt> <dd>

月7日

</dd> <dt>

<span id="8"></span>

<span id="8"></span>**8** (128) 


</dt> <dd>

每月第8天

</dd> <dt>

<span id="9"></span>

<span id="9"></span>**9** (256) 


</dt> <dd>

每月第9天

</dd> <dt>

<span id="10"></span>

<span id="10"></span>**10** (512) 


</dt> <dd>

每月第10天

</dd> <dt>

<span id="11"></span>

<span id="11"></span>**11** (1024) 


</dt> <dd>

每月第11天

</dd> <dt>

<span id="12"></span>

<span id="12"></span>**12** (2048) 


</dt> <dd>

每月第12天

</dd> <dt>

<span id="13"></span>

<span id="13"></span>**13** (4096) 


</dt> <dd>

每月第13天

</dd> <dt>

<span id="14"></span>

<span id="14"></span>**14** (8192) 


</dt> <dd>

月14日

</dd> <dt>

<span id="15"></span>

<span id="15"></span>**15** (16384) 


</dt> <dd>

月15日

</dd> <dt>

<span id="16"></span>

<span id="16"></span>**16** (32768) 


</dt> <dd>

每月第16天

</dd> <dt>

<span id="17"></span>

<span id="17"></span>**17** (65536) 


</dt> <dd>

每月17日

</dd> <dt>

<span id="18"></span>

<span id="18"></span>**18** (131072) 


</dt> <dd>

每月18日

</dd> <dt>

<span id="19"></span>

<span id="19"></span>**19** (262144) 


</dt> <dd>

月19日

</dd> <dt>

<span id="20"></span>

<span id="20"></span>**20** (524288) 


</dt> <dd>

每月第20天

</dd> <dt>

<span id="21"></span>

<span id="21"></span>**21** (1048576) 


</dt> <dd>

每月21日

</dd> <dt>

<span id="22"></span>

<span id="22"></span>**22** (2097152) 


</dt> <dd>

每月第22天

</dd> <dt>

<span id="23"></span>

<span id="23"></span>**23** (4194304) 


</dt> <dd>

每月23日

</dd> <dt>

<span id="24"></span>

<span id="24"></span>**24** (8388608) 


</dt> <dd>

每月第24天

</dd> <dt>

<span id="25"></span>

<span id="25"></span>**25** (16777216) 


</dt> <dd>

每月25日

</dd> <dt>

<span id="26"></span>

<span id="26"></span>**26** (33554432) 


</dt> <dd>

每月26日

</dd> <dt>

<span id="27"></span>

<span id="27"></span>**27** (67108864) 


</dt> <dd>

每月第27天

</dd> <dt>

<span id="28"></span>

<span id="28"></span>**28** (134217728) 


</dt> <dd>

一個月的第28天

</dd> <dt>

<span id="29"></span>

<span id="29"></span>**29** (268435456) 


</dt> <dd>

每月第29天

</dd> <dt>

<span id="30"></span>

<span id="30"></span>**30** (536870912) 


</dt> <dd>

每月30日

</dd> <dt>

<span id="31"></span>

<span id="31"></span>**31** (1073741824) 


</dt> <dd>

月31日

</dd> </dl> </dd> <dt>

*InteractWithDesktop* \[在中，選擇性\]
</dt> <dd>

若 **為 True**，表示指定的工作應該是互動式的，這表示使用者可以在工作執行時將輸入提供給排程工作。 預設值為 **False**。

</dd> <dt>

*JobId* \[擴展\]
</dt> <dd>

作業的識別碼。 此參數是在電腦上排程之作業的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

在成功時傳回 0 (零) 的值，並傳回不同的數位來表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成**
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

使用者沒有必要的存取權。

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

**參數不正確**
</dt> <dd>

21

傳遞給服務的參數無效。

</dd> <dt>

**服務未啟動**
</dt> <dd>

22

執行此服務的帳戶無效，或缺少執行服務的許可權。

</dd> <dt>

**其他**
</dt> <dd>

23 4294967295

</dd> </dl>

## <a name="remarks"></a>備註

如果您的排程工作啟動了互動式程式，例如「記事本」，則 **InteractWithDeskto** 屬性必須設定為 **True** ，否則就看不到該程式的畫面。 即使此程式未出現在畫面上，仍會出現在 **工作管理員** 中。

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

[**Win32 \_ register-scheduledjob**](win32-scheduledjob.md)
</dt> </dl>

 

