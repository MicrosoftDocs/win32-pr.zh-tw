---
title: 'IVMSerialPort Type 屬性 (VPCCOMInterfaces .h) '
description: 捕獲序列埠的類型。
ms.assetid: 0ec9c9d7-9387-458e-befe-42d58c38df35
keywords:
- 類型虛擬電腦
- Type property Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，Type 屬性
topic_type:
- apiref
api_name:
- IVMSerialPort.Type
- IVMSerialPort.get_Type
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ab32ba6e205911fca85474c047e24b7ad7f1f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465537"
---
# <a name="ivmserialporttype-property"></a>IVMSerialPort：： Type 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

捕獲序列埠的類型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Type(
  [out, retval] VMSerialPortType *portType
);
```



## <a name="property-value"></a>屬性值

序列埠的類型。 如需值的清單，請參閱 [**VMSerialPortType**](vmserialporttype.md)。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                            |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 Null。<br/>                                   |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 此虛擬機器的設定無效。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

