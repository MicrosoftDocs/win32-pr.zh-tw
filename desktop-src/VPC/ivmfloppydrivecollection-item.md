---
title: 'IVMFloppyDriveCollection 專案屬性 (VPCCOMInterfaces .h) '
description: 對應至指定之索引的軟碟物件。
ms.assetid: 068a1f1c-ae84-4689-b68a-ce25b68fc06b
keywords:
- 專案屬性 Virtual PC
- 專案屬性 Virtual PC，IVMFloppyDriveCollection 介面
- IVMFloppyDriveCollection 介面 Virtual PC，Item 屬性
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection.Item
- IVMFloppyDriveCollection.get_Item
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315eaea13699d78a75457f39c6c915b30fa2fa9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106062"
---
# <a name="ivmfloppydrivecollectionitem-property"></a>IVMFloppyDriveCollection：： Item 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取對應至指定之索引的磁片物件。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Item(
  [in]          long           index,
  [out, retval] IVMFloppyDrive **floppyDrive
);
```



## <a name="property-value"></a>屬性值

[**IVMFloppyDrive**](ivmfloppydrive.md)物件。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                                      |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | *FloppyDrive* 參數為 **Null**。<br/>                                           |
| <dl> <dt>會 \_E \_ BADINDEX</dt> <dt>0x8002000B</dt> </dl>  | 要求專案的索引未對應到此集合中的專案。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 未知的設定。<br/>                                                      |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDriveCollection 定義為8ba70a25-f698-4ee5-85ce-3cc93a925516<br/>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> <dt>

[**IVMFloppyDriveCollection**](ivmfloppydrivecollection.md)
</dt> </dl>

 

