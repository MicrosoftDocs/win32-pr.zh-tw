---
title: 'IVMHardDiskConnectionCollection Count 屬性 (VPCCOMInterfaces .h) '
description: 抓取此集合中的硬碟連接數目。
ms.assetid: 913c1bb7-0237-4f11-9873-7b42a94004f8
keywords:
- Count 屬性 Virtual PC
- Count 屬性 Virtual PC，IVMHardDiskConnectionCollection 介面
- IVMHardDiskConnectionCollection 介面 Virtual PC、Count 屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Count
- IVMHardDiskConnectionCollection.get_Count
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fccb00cf2388db8a971f5da2f726030b3f793ac878f4a59df2646195eb41ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974320"
---
# <a name="ivmharddiskconnectioncollectioncount-property"></a>IVMHardDiskConnectionCollection：： Count 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取此集合中的硬碟連接數目。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Count(
  [out, retval] long *count
);
```



## <a name="property-value"></a>屬性值

硬碟連接的數目。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>     |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                          |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                               |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                      |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection 定義為 b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

