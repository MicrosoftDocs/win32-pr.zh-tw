---
title: 'IVMHardDiskConnectionCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 抓取對應至指定之索引的硬碟連線物件。
ms.assetid: 24e158fb-b026-4619-9d0d-a59cd782894f
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMHardDiskConnectionCollection 介面
- IVMHardDiskConnectionCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMHardDiskConnectionCollection.Item
- IVMHardDiskConnectionCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5558e70cfcf18f67c14e52160737b851fa9ea2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968531"
---
# <a name="ivmharddiskconnectioncollectionitem-property"></a>IVMHardDiskConnectionCollection：： Item 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取對應至指定之索引的硬碟連線物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Item(
  [in]          long                  index,
  [out, retval] IVMHardDiskConnection **hardDiskConnection
);
```



## <a name="property-value"></a>屬性值

[**IVMHardDiskConnection**](ivmharddiskconnection.md)物件。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。 <br/>                                                      |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | *HardDiskConnection* 參數為 **Null**。 <br/>                                    |
| <dl> <dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | 要求專案的索引未對應到此集合中的專案。 <br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>                                                       |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                                   |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                         |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                          |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                               |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                      |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl>      |
| IID<br/>                      | IID \_ IVMHardDiskconnectionCollection 定義為 b9f2caf4-0aeb-4085-b105-ceddb90dbf62<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMHardDiskConnection**](ivmharddiskconnection.md)
</dt> <dt>

[**IVMHardDiskConnectionCollection**](ivmharddiskconnectioncollection.md)
</dt> </dl>

 

