---
title: 'IVMNetworkAdapter AttachToVirtualNetwork 方法 (VPCCOMInterfaces .h) '
description: 將網路介面附加至指定的虛擬網路。
ms.assetid: c743e930-c22e-4f32-b691-f7adc2485fed
keywords:
- AttachToVirtualNetwork 方法 Virtual PC
- AttachToVirtualNetwork 方法 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，AttachToVirtualNetwork 方法
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.AttachToVirtualNetwork
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01e7d0d9822e73ef6081a35f19ef628fd10051b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465621"
---
# <a name="ivmnetworkadapterattachtovirtualnetwork-method"></a>IVMNetworkAdapter：： AttachToVirtualNetwork 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將網路介面附加至指定的虛擬網路。

## <a name="syntax"></a>語法


```C++
HRESULT AttachToVirtualNetwork(
  [in] IVMVirtualNetwork *virtualNetwork
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*virtualNetwork* \[在\]
</dt> <dd>

將連接此虛擬 NIC 的虛擬網路。 請參閱 [**IVMVirtualNetwork**](ivmvirtualnetwork.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                                          | Description                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                                                                                       | 作業成功。<br/>                           |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                                  | 參數為 **Null**。<br/>                              |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>                               | 參數不包含有效的虛擬網路。<br/> |
| <dl> <dt>**HRESULT \_從 \_ WIN32 (\_ \_ 拒絕存取錯誤)**</dt> <dt>0x80070005</dt> </dl> | 已拒絕存取要求的虛擬網路。<br/>     |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl>                          | 虛擬機器無效或已不存在。<br/>     |
| <dl> <dt>**VM \_ E \_ 不正確 \_ 虛擬 \_ 網路 \_ 識別碼**</dt> </dl>                                                                        | 參數不是現有的虛擬網路。<br/>       |
| <dl> <dt>**出現 \_ E \_ 例外狀況**</dt> </dl>                                                                                          | 已發生未預期的錯誤。<br/>                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

