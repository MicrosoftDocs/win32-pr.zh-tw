---
title: 'IVMDVDDriveCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器中的 CD 和 DVD 光碟機集合。 若要取得 IVMDVDDriveCollection 物件，請使用 IVMVirtualMachine DVDROMDrives 屬性。
ms.assetid: 3069f530-9bc7-4f55-bf5a-82d1244d0cc5
keywords:
- IVMDVDDriveCollection 介面 Virtual PC
- IVMDVDDriveCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMDVDDriveCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77225134a88ff2c66be3f53f5d3d44c9f8353d8f44077fb0862f0c943c5aec3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056856"
---
# <a name="ivmdvddrivecollection-interface"></a>IVMDVDDriveCollection 介面

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器中的 CD 和 DVD 光碟機集合。 若要取得 **IVMDVDDriveCollection** 物件，請使用 [**IVMVirtualMachine：:D vdromdrives**](ivmvirtualmachine-dvdromdrives.md) 屬性。

## <a name="members"></a>成員

**IVMDVDDriveCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMDVDDriveCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMDVDDriveCollection** 介面具有這些屬性。



| 屬性                                                       | 存取類型          | 描述                                                                    |
|:---------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------|
| [**\_NewEnum**](ivmdvddrivecollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                                   |
| [**計數**](ivmdvddrivecollection-count.md)<br/>        | 唯讀<br/> | 此集合中的 CD 和 DVD 光碟機數目。<br/>                 |
| [**項目**](ivmdvddrivecollection-item.md)<br/>          | 唯讀<br/> | 對應到指定之索引的 CD 或 DVD 光碟機物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDriveCollection 定義為 bc86e297-e55f-4742-9614-ad11d3131f68<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> <dt>

[**IVMVirtualMachine：:D VDROMDrives**](ivmvirtualmachine-dvdromdrives.md)
</dt> </dl>

 

