---
title: 'IVMVirtualMachine StartCommunicationChannel 方法 (VPCCOMInterfaces .h) '
description: 設定主機與客體作業系統之間的通道。
ms.assetid: e4b04aa8-8400-4aa4-ad54-71ef57dec82a
keywords:
- StartCommunicationChannel 方法 Virtual PC
- StartCommunicationChannel 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，StartCommunicationChannel 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.StartCommunicationChannel
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ac6ab73b6a955b6810eaea280dc25732e2a6721
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466380"
---
# <a name="ivmvirtualmachinestartcommunicationchannel-method"></a>IVMVirtualMachine：： StartCommunicationChannel 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

設定主機與客體作業系統之間的通道。

## <a name="syntax"></a>語法


```C++
HRESULT StartCommunicationChannel(
  [in] VMEndpointType inHostEndpointType,
  [in] BSTR           inHostEndPointName,
  [in] VMEndpointType inGuestEndpointType,
  [in] BSTR           inGuestEndpointName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*inHostEndpointType* \[在\]
</dt> <dd>

此參數必須是 **vmEndpoint \_ NamedPipe** (0) 。

</dd> <dt>

*inHostEndPointName* \[在\]
</dt> <dd>

唯一的管道名稱。 這個字串的格式必須如下： " \\ \\ 。 \\pipe \\ *pipename*」。 名稱的 *pipename* 部分可以包含反斜線以外的任何字元，包括數位和特殊字元。 整個管道名稱字串的長度最多可達256個字元。 管道名稱不區分大小寫。

</dd> <dt>

*inGuestEndpointType* \[在\]
</dt> <dd>

此參數必須是 **vmEndpoint \_ TCPIP** (1) 。

</dd> <dt>

*inGuestEndpointName* \[在\]
</dt> <dd>

來賓中 TCP 伺服器正在接聽的埠號碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                                  | Description                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                                                        | 作業成功。<br/>                                                                                                                    |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                                       | *InHostEndpointType* 參數不是 **vmEndpoint \_ NamedPipe** (0) 或 *inGuestEndpointType* 參數不是 **vmEndpoint \_ TCPIP** (1) 。<br/> |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                          | *InHostEndPointName* 或 *InGuestEndpointName* 參數為 **Null** 或不是有效的值。<br/>                                                    |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>                                  | 已發生未預期的錯誤。<br/>                                                                                                                |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 不正確 \_ 控制碼)**</dt> <dt>0x80070006</dt> </dl>        | 控制碼無效。<br/>                                                                                                                           |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt> </dl>            | 沒有足夠的記憶體可完成此要求。<br/>                                                                                   |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 未 \_ 就緒)**</dt> <dt>0x80070015</dt> </dl>             | 它用來提供網路服務的基礎系統目前正在初始化。<br/>                                                        |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt> </dl>        | 管道名稱已在使用中。<br/>                                                                                                                 |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 管道 \_ 忙碌)**</dt> <dt>0x800700e7</dt> </dl>             | 有一或多個通道正在執行，而且很快就會推出。<br/>                                                                          |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (已 \_ 達到錯誤的最大 \_ 會話 \_)**</dt> <dt>0x80070161</dt> </dl> | 可用的通訊通道數目上限已在使用中。 目前無法啟動另一個通道。<br/>                              |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 修訂 \_ 不相符)**</dt> <dt>0x8007051a</dt> </dl>     | 主機和來賓子系統的版本不相符。 如需詳細資訊，請參閱 Windows 事件記錄檔。<br/>                             |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>                             | VM 未執行。<br/>                                                                                                                           |



 

## <a name="remarks"></a>備註

目前的執行僅支援在客體作業系統上的主機和 TCP/IP 介面上具名管道介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> <dt>

[**VMEndpointType**](vmendpointtype.md)
</dt> </dl>

 

