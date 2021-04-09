---
title: 'IVMAccountant DiskBytesRead 屬性 (VPCCOMInterfaces .h) '
description: 此虛擬機器的所有存放裝置控制器所讀取的總位元組數。
ms.assetid: cf2c1a58-2261-496d-b8e2-a0d5285c16ab
keywords:
- DiskBytesRead 屬性 Virtual PC
- DiskBytesRead 屬性 Virtual PC，IVMAccountant 介面
- IVMAccountant 介面 Virtual PC，DiskBytesRead 屬性
topic_type:
- apiref
api_name:
- IVMAccountant.DiskBytesRead
- IVMAccountant.get_DiskBytesRead
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2dec370a9669ee5f43ae67f8d47c153c342a53d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934471"
---
# <a name="ivmaccountantdiskbytesread-property"></a>IVMAccountant：:D iskBytesRead 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此虛擬機器的所有儲存控制器讀取的位元組總數。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DiskBytesRead(
  [out, retval] VARIANT *bytesRead
);
```



## <a name="property-value"></a>屬性值

位元組總數。 這項資料會以 **VT \_ DECIMAL** 類型的 **變數** 傳回。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>       |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>          |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                    | 虛擬機器未執行。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>   |



## <a name="remarks"></a>備註

請注意，當虛擬機器從儲存狀態開機、重設或還原時，磁片 i/o 統計資料會重設為零。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMAccountant 定義為6376c067-7f57-4d63-b754-06e2e4f51d73<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMAccountant**](ivmaccountant.md)
</dt> </dl>

 

