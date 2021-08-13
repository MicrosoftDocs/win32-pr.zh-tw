---
description: SetPriority&\# 32;WMI 類別方法會嘗試變更進程的執行優先權。
ms.assetid: ef012e9e-ff65-4881-835e-ddab23af9333
ms.tgt_platform: multiple
title: Win32_Process 類別的 SetPriority 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process.SetPriority
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: decd5892d480e4f236ae9d7acdc1a25c018557166535c963eb35dc3f6f62ffa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675567"
---
# <a name="setpriority-method-of-the-win32_process-class"></a>Win32 進程類別的 SetPriority 方法 \_

**SetPriority** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會嘗試變更進程的執行優先權。

本主題使用受控物件格式 (MOF) 語法。 如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。

## <a name="syntax"></a>語法


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*優先順序* \[在\]
</dt> <dd>

進程的新優先順序類別。 請注意，這些值與 [**Win32 \_ 進程**](win32-process.md)的 **Priority** 屬性中明確陳述的值不同。

<dt>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>

<span id="Idle"></span><span id="idle"></span><span id="IDLE"></span>**閒置** (64) 


</dt> <dd>

針對只有當系統閒置時才會執行之執行緒的進程指定。 進程的執行緒會被在較高優先順序類別中執行之進程的執行緒佔用，例如螢幕保護裝置。 子進程會繼承閒置優先順序類別。

</dd> <dt>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>

<span id="Below_Normal"></span><span id="below_normal"></span><span id="BELOW_NORMAL"></span>**低於標準** (16384) 


</dt> <dd>

指出優先順序高於 **閒置 \_ 優先順序 \_ 類別**，但低於 **一般 \_ 優先順序 \_ 類別** 的進程。

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**一般** (32) 


</dt> <dd>

針對沒有特殊排程需求的進程指定。

</dd> <dt>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>

<span id="Above_Normal"></span><span id="above_normal"></span><span id="ABOVE_NORMAL"></span>**高於一般** (32768) 


</dt> <dd>

指出優先順序高於 **一般 \_ 優先順序 \_ 類別** 但優先順序高於 **高 \_ 優先順序 \_** 類別的進程。

</dd> <dt>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>

<span id="High_Priority"></span><span id="high_priority"></span><span id="HIGH_PRIORITY"></span>**高優先順序** (128) 


</dt> <dd>

針對執行必須立即執行之時間關鍵工作的進程指定。 該處理序的執行緒會優先於正常或閒置優先權類別處理序的執行緒。 其中一個範例是工作清單，當使用者呼叫時，無論作業系統上的負載為何，都必須快速回應。 使用高優先順序類別時請特別小心，因為高優先順序的類別應用程式幾乎可以使用所有可用的 CPU 時間。

</dd> <dt>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>

<span id="Realtime"></span><span id="realtime"></span><span id="REALTIME"></span>**即時** (256) 


</dt> <dd>

指定給具有最高優先順序的進程。 進程的執行緒會優先處理所有其他進程的執行緒，包括執行重要工作的作業系統進程。 例如，執行超過一小段時間間隔的即時程式可能導致磁碟快取無法排清或滑鼠沒有回應。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

傳回下列清單所列的其中一個值，或傳回不同的值來表示錯誤。 如需其他錯誤代碼，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。 如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。

<dl> <dt>

**成功完成** (0) 
</dt> <dt>

**拒絕存取** (2) 
</dt> <dt>

**許可權不足** (3) 
</dt> <dt>

**未知的失敗** (8) 
</dt> <dt>

 (9) **找不到路徑**
</dt> <dt>

**不正確參數** (21) 
</dt> <dt>

**其他** (22 4294967295) 
</dt> </dl>

## <a name="remarks"></a>備註

若要將優先權設定為即時，呼叫端必須具有 **SeIncreaseBasePriorityPrivilege** (**SE \_ INC \_ 基本 \_ 優先權 \_ 許可權**) 。 如果沒有此許可權，優先順序最高的優先順序可以設定為高優先順序。

## <a name="examples"></a>範例

[ [修改執行中進程的優先順序](https://Gallery.TechNet.Microsoft.Com/23615ee7-cccb-43c2-b994-6106ce2fc05e) ] VBScript 範例會將執行中的 Notepad.exe 實例的優先順序從一般變更為一般。

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

[**Win32 \_ 進程**](win32-process.md)
</dt> </dl>

 

