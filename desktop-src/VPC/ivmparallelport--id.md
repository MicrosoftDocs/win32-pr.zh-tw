---
title: 'IVMParallelPort _ID 方法 (VPCCOMInterfaces .h) '
description: 抓取平行埠的內部識別碼。
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID 方法 Virtual PC
- _ID 方法 Virtual PC，IVMParallelPort 介面
- IVMParallelPort 介面 Virtual PC，_ID 方法
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267061204ea92dd8f5cae37fc5cb279e7dc2b010
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995575"
---
# <a name="ivmparallelport_id-method"></a>IVMParallelPort：： \_ ID 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取平行埠的內部識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*portID* \[擴展\]
</dt> <dd>

平行埠識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | Description                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                            |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>                               |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                        |
| <dl> <dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt> </dl> | 此虛擬機器的設定無效。<br/> |



 

## <a name="remarks"></a>備註

指令碼語言無法使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMParallelPort 定義為097beecb-0a02-474f-abd6-298b22293fc6<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

