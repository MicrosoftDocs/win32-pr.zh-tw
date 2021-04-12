---
title: 'IVMGuestOS 登出方法 (VPCCOMInterfaces .h) '
description: 登出客體作業系統中的所有使用者。
ms.assetid: 224aa7cb-0892-4e8a-84bd-78dd5cb724df
keywords:
- 登出方法虛擬電腦
- 登出方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，登出方法
topic_type:
- apiref
api_name:
- IVMGuestOS.Logoff
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20c67e917cc9ff93d162bc340185f426fe9eee3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025455"
---
# <a name="ivmguestoslogoff-method"></a>IVMGuestOS：：登出方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

登出客體作業系統中的所有使用者。

## <a name="syntax"></a>語法


```C++
HRESULT Logoff(
  [out, retval] IVMTask **outLogoffTask
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*outLogoffTask* \[退出，retval\]
</dt> <dd>

[**IVMTask**](ivmtask.md)物件，用來追蹤登出順序的完成進度。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                          | Description                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                | 作業成功。<br/>                                                |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                          | 已發生未預期的錯誤。<br/>                                            |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                  | 參數為 **Null**。<br/>                                                   |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt> </dl> | 呼叫端必須具有此 VM 的「執行」存取權限。<br/>                 |
| <dl> <dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt> </dl>                           | 作業未及時完成。<br/>                           |
| <dl> <dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt> </dl>       | 此虛擬機器未安裝整合元件功能。<br/> |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                     | 虛擬機器 (VM) 必須針對此操作執行。<br/>                 |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                          | 未知的設定。<br/>                                                |



 

## <a name="remarks"></a>備註

`HRESULT_FROM_WIN32(ERROR_NO_SUCH_LOGON_SESSION)` (的 0x80070520) 會透過傳回之 [**IVMTask**](ivmtask.md)物件的 [**Error**](ivmtask-error.md)屬性傳回，而客體作業系統中沒有任何登入會話。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

