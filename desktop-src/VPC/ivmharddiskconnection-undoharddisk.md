---
title: 'IVMHardDiskConnection UndoHardDisk 屬性 (VPCCOMInterfaces .h) '
description: 抓取與此連接之復原磁片映射對應的硬碟物件。
ms.assetid: 0daec200-0bda-44cf-b97d-b9a179cb63f8
keywords:
- UndoHardDisk 屬性 Virtual PC
- UndoHardDisk 屬性 Virtual PC，IVMHardDiskConnection 介面
- IVMHardDiskConnection 介面 Virtual PC，UndoHardDisk 屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnection.UndoHardDisk
- IVMHardDiskConnection.get_UndoHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0fcbd6535c0cf91e1b42549047c131c1804215c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093768"
---
# <a name="ivmharddiskconnectionundoharddisk-property"></a>IVMHardDiskConnection：： UndoHardDisk 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取與此連接之復原磁片映射對應的硬碟物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_UndoHardDisk(
  [out, retval] IVMHardDisk **undoHardDisk
);
```



## <a name="property-value"></a>屬性值

描述與此連接相關聯之復原硬碟的 [**IVMHardDisk**](ivmharddisk.md) 物件。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                               | 意義                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                                  | 作業成功。<br/>                                                                                                    |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                            | 已發生未預期的錯誤。<br/>                                                                                                |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                                    | 參數為 **Null** 或無效。<br/>                                                                                          |
| <dl> <dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt> </dl> | 找不到此連接的復原磁片。<br/>                                                                                 |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>                            | 目前的虛擬機器設定無效。<br/>                                                                          |
| <dl> <dt>VM \_E \_ 磁片磁碟機 \_ 無效</dt>的 <dt>0xA0040502</dt> </dl>                         | 此連線的匯流排位置未正確地初始化，或此位置的裝置不是有效的硬碟。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDiskconnection 定義為 aefa36a5-463a-46ae-9e6c-a1fb4e12e671<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> </dl>

 

