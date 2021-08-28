---
title: 'IVMHardDiskConnection 硬碟屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至此連接的硬碟物件。
ms.assetid: dbe369d8-ec05-4039-9494-fc196262f697
keywords:
- 硬碟屬性虛擬電腦
- 硬碟屬性虛擬 PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，硬碟屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.HardDisk
- IVMHardDiskConnection.get_HardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e03eafb17aab0b27d8d47e142c4ba540933e6d09452d2ef705cf7e54c550829
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844820"
---
# <a name="ivmharddiskconnectionharddisk-property"></a>IVMHardDiskConnection：：硬碟屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取對應至此連接的硬碟物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_HardDisk(
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="property-value"></a>屬性值

[**IVMHardDisk**](ivmharddisk.md)物件，描述與此連接相關聯的硬碟。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                       | 意義                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                          | 作業成功。<br/>                                                                                                    |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>            | 參數為 **Null** 或無效。<br/>                                                                                          |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>    | 目前的虛擬機器設定無效。<br/>                                                                          |
| <dl> <dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt> </dl> | 此連線的匯流排位置未正確地初始化，或此位置的裝置不是有效的硬碟。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>    | 已發生未預期的錯誤。<br/>                                                                                                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

