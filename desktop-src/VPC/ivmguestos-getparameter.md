---
title: 'IVMGuestOS GetParameter 方法 (VPCCOMInterfaces .h) '
description: 抓取客體作業系統內的具名引數。
ms.assetid: d4d5acbd-fa19-4eb2-af75-2c94e5f6f7f0
keywords:
- GetParameter 方法 Virtual PC
- GetParameter 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，GetParameter 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.GetParameter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d12bddec3fac5dc918f06d926fe5e5656b70d84d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387644"
---
# <a name="ivmguestosgetparameter-method"></a>IVMGuestOS：： GetParameter 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取客體作業系統內的具名引數。

## <a name="syntax"></a>語法


```C++
HRESULT GetParameter(
  [in]          BSTR inParameterName,
  [out, retval] BSTR *outParameterValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inParameterName* \[在\]
</dt> <dd>

參數名稱。 長度必須介於1到255個字元之間，且不能包含反斜線 (\\) 字元。

</dd> <dt>

*outParameterValue* \[退出，retval\]
</dt> <dd>

參數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                    | Description                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                     |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                         | 參數無效或未指定。<br/>                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                            | 參數為 **Null**。<br/>                                        |
| <dl> <dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt> </dl>                     | 作業未及時完成。<br/>                |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>               | 虛擬機器未執行。<br/>                               |
| <dl> <dt>**VM \_E \_ VM 已 \_ 暫停**</dt> <dt>0xA00400507</dt> </dl>                    | 虛擬機器已暫停。<br/>                                    |
| <dl> <dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt> </dl> | 此虛擬機器中未安裝整合元件。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                 |



 

## <a name="remarks"></a>備註

虛擬機器必須在執行中，而且當叫用此方法時，必須安裝整合元件。 只有以 Windows 為基礎的客體作業系統支援這個方法。

安裝整合元件後，系統會自動將下列金鑰新增至客體作業系統的登錄：

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 虛擬機器 \\ 來賓 \\ 參數**

當客體作業系統啟動時，會在 **參數** 索引鍵中填入下列登錄字串值：

-   **HostName**
-   **PhysicalHostName**
-   **PhysicalHostNameFullyQualified**
-   **VirtualMachineName**

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

 

