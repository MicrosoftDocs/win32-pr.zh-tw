---
title: 'IVMSerialPort Configure 方法 (VPCCOMInterfaces .h) '
description: 設定序列埠。
ms.assetid: fee2e373-8e7c-4f1d-84d0-f0f187a41e9f
keywords:
- 設定方法 Virtual PC
- 設定方法 Virtual PC，IVMSerialPort 介面
- IVMSerialPort 介面 Virtual PC，Configure 方法
topic_type:
- apiref
api_name:
- IVMSerialPort.Configure
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e67d84239f7b672b5b8c47346d1dde73de6a35c1e99a3ba231b8425fe8b7d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136621"
---
# <a name="ivmserialportconfigure-method"></a>IVMSerialPort：： Configure 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

設定序列埠。

## <a name="syntax"></a>語法


```C++
HRESULT Configure(
  [in] VMSerialPortType portType,
  [in] BSTR             portName,
  [in] VARIANT_BOOL     vmConnectImmediately
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*portType* \[在\]
</dt> <dd>

序列埠的類型。 如需值的清單，請參閱 [**VMSerialPortType**](vmserialporttype.md)。

</dd> <dt>

*portName* \[在\]
</dt> <dd>

序列埠的名稱。 例如，"COM1" 代表 **vmSerialPort \_ HostPort**，"C： \\SerialPort.txt" 代表 **vmSerialPort \_ TextFile**，" \\ \\ *servername* \\ pipe \\ *pipename*" 代表 **vmSerialPort \_ NamedPipe**。

</dd> <dt>

*vmConnectImmediately* \[在\]
</dt> <dd>

如果啟動虛擬機器時應立即開啟主機序列埠，則 **為 TRUE** ，否則為 **FALSE** 。 如果 *portType* 不是 **vmSerialPort \_ HostPort**，則會忽略。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                            | 描述                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                          |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                 | *PortType* 參數無效。<br/>                                                                                 |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                      |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                    | *PortName* 參數為 **Null**。<br/>                                                                                  |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>      | 沒有足夠的記憶體可完成此要求。<br/>                                                         |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt> </dl> | *PortName* 參數所指定的路徑太長。 路徑必須小於 **最大 \_ 路徑** (260) 個字元。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt> </dl>    | *PortName* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。<br/>                                    |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt> </dl>    | *PortName* 參數會指定空的或相對路徑。 需要絕對路徑。<br/>                            |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                            | 此虛擬機器的設定無效。<br/>                                                               |
| <dl> <dt>**VM \_E \_ PREF 不 \_ 合法的 \_ 值**</dt> <dt>0xA0040301</dt> </dl>                   | 指定的埠已在使用中。<br/>                                                                                  |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort 定義為 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

