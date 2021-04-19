---
title: 'IVMDVDDrive BusNumber 屬性 (VPCCOMInterfaces .h) '
description: 抓取此裝置所連接的匯流排編號。
ms.assetid: 8edc94da-22bc-4141-a6c7-1b18cca754fc
keywords:
- BusNumber 屬性 Virtual PC
- BusNumber 屬性 Virtual PC，IVMDVDDrive 介面
- IVMDVDDrive 介面 Virtual PC，BusNumber 屬性
topic_type:
- apiref
api_name:
- IVMDVDDrive.BusNumber
- IVMDVDDrive.get_BusNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 056770b7eb11518645f3c28a6d45685795c7107a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106999817"
---
# <a name="ivmdvddrivebusnumber-property"></a>IVMDVDDrive：： BusNumber 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此裝置所連接的匯流排編號。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_BusNumber(
  [out, retval] long *vmBusNumber
);
```



## <a name="property-value"></a>屬性值

匯流排號碼。 例如，在 IDE 匯流排上，此值會代表主要或次要位置。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                       | 意義                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                          | 作業成功。<br/>                                          |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>            | 參數為 **Null**。<br/>                                             |
| <dl> <dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt> </dl> | 此 DVD 光碟機的匯流排位置未正確初始化。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>    | 已發生未預期的錯誤。<br/>                                      |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive 定義為 b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

