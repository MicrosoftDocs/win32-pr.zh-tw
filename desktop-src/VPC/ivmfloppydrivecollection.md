---
title: 'IVMFloppyDriveCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內的一組磁片磁碟機。
ms.assetid: ba05fa84-81c3-4e70-98f5-404a9bc517ad
keywords:
- IVMFloppyDriveCollection 介面 Virtual PC
- IVMFloppyDriveCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMFloppyDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 664937a08bf7576c35b94a162fb5b6f4a7400f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385238"
---
# <a name="ivmfloppydrivecollection-interface"></a>IVMFloppyDriveCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內的一組磁片磁碟機。 若要取得 **IVMFloppyDriveCollection** 物件，請使用 [**IVMVirtualMachine：： FloppyDrives**](ivmvirtualmachine-floppydrives.md) 屬性。

## <a name="members"></a>成員

**IVMFloppyDriveCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMFloppyDriveCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMFloppyDriveCollection** 介面具有這些屬性。



| 屬性                                                          | 存取類型          | Description                                                                 |
|:------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------|
| [**\_NewEnum**](ivmfloppydrivecollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                |
| [**計數**](ivmfloppydrivecollection-count.md)<br/>        | 唯讀<br/> | 此集合中的磁片磁碟機數目。<br/>                  |
| [**項目**](ivmfloppydrivecollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的磁片磁碟機物件。<br/> |



 

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

[**IVMVirtualMachine::FloppyDrives**](ivmvirtualmachine-floppydrives.md)
</dt> </dl>

 

