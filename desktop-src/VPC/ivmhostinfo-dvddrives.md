---
title: 'IVMHostInfo DVDDrives 屬性 (VPCCOMInterfaces .h) '
description: 抓取與主機 CD 和 DVD 裝置相關聯的磁碟機號。
ms.assetid: 17f01d00-2c02-48f0-bfe9-0326a40fdf55
keywords:
- DVDDrives 屬性 Virtual PC
- DVDDrives 屬性 Virtual PC，IVMHostInfo 介面
- IVMHostInfo 介面 Virtual PC，DVDDrives 屬性
topic_type:
- apiref
api_name:
- IVMHostInfo.DVDDrives
- IVMHostInfo.get_DVDDrives
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cfe0cf1a6b3a106af3bf1e7ec553b1822fd8ec51027a46b07a794771addc383
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056832"
---
# <a name="ivmhostinfodvddrives-property"></a>IVMHostInfo：:D VDDrives 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取與主機 CD 和 DVD 裝置相關聯的磁碟機號。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_DVDDrives(
  [out, retval] VARIANT *DVDDrives
);
```



## <a name="property-value"></a>屬性值

磁碟機號的陣列。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo 定義為5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHostInfo**](ivmhostinfo.md)
</dt> </dl>

 

