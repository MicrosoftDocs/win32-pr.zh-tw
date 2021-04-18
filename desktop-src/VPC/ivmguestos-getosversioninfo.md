---
title: 'IVMGuestOS GetOsVersionInfo 方法 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中執行之客體作業系統的版本資訊。
ms.assetid: 1f9d749f-6007-466d-9df9-71c6a72e8112
keywords:
- GetOsVersionInfo 方法 Virtual PC
- GetOsVersionInfo 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，GetOsVersionInfo 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.GetOsVersionInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ec0c0c2516a8ef16a3d9d9c6c4178abb31bd52f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965324"
---
# <a name="ivmguestosgetosversioninfo-method"></a>IVMGuestOS：： GetOsVersionInfo 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬機器中執行之客體作業系統 (VM) 的版本資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetOsVersionInfo(
  [out, retval] GUESTOSVERSIONINFOEX **guestOsVersionInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*guestOsVersionInfo* \[退出，retval\]
</dt> <dd>

[**GUESTOSVERSIONINFOEX**](guestosversioninfoex.md)結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                       | Description                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                             | 作業成功。<br/>                                  |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                               | 參數為 **Null**。<br/>                                     |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl> | 沒有足夠的記憶體可完成此要求。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                       | 已發生未預期的錯誤。<br/>                              |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                  | VM 未執行。<br/>                                         |
| <dl> <dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt> </dl>    | 此 VM 中未安裝整合元件。<br/>           |



 

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

 

