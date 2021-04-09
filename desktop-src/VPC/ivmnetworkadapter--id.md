---
title: 'IVMNetworkAdapter _ID 方法 (VPCCOMInterfaces .h) '
description: 抓取此網路介面的內部識別碼。
ms.assetid: 3e71c2cd-1a75-44d9-9a6d-04e6344dfec3
keywords:
- _ID 方法 Virtual PC
- _ID 方法 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，_ID 方法
topic_type:
- apiref
api_name:
- IVMNetworkAdapter._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b9df514d24f9826b58964b4c51c9a76a9ba982e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934501"
---
# <a name="ivmnetworkadapter_id-method"></a>IVMNetworkAdapter：： \_ ID 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此網路介面的內部識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT _ID(
  [out] long *identifier
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*識別碼* \[擴展\]
</dt> <dd>

內部識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | Description                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>           |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl> | 找不到虛擬機器。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 作業發生未知的錯誤。<br/>  |



 

## <a name="remarks"></a>備註

指令碼語言無法使用這個方法。

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

 

