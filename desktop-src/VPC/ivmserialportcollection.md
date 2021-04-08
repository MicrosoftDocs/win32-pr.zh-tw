---
title: 'IVMSerialPortCollection 介面 (VPCCOMInterfaces .h) '
description: 定義虛擬機器內序列埠的集合。 若要取得 IVMSerialPortCollection 物件，請使用 IVMVirtualMachine Serialport 屬性。
ms.assetid: c0ee9799-f3f7-477e-b33b-52f424752aad
keywords:
- IVMSerialPortCollection 介面 Virtual PC
- IVMSerialPortCollection 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMSerialPortCollection
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d2ec37789423b5f9446d667da69eca346a2286
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685967"
---
# <a name="ivmserialportcollection-interface"></a>IVMSerialPortCollection 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

定義虛擬機器內序列埠的集合。 若要取得 **IVMSerialPortCollection** 物件，請使用 [**IVMVirtualMachine：： serialport**](ivmvirtualmachine-serialports.md) 屬性。

## <a name="members"></a>成員

**IVMSerialPortCollection** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMSerialPortCollection** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IVMSerialPortCollection** 介面具有這些屬性。



| 屬性                                                         | 存取類型          | Description                                                                |
|:-----------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------|
| [**\_NewEnum**](ivmserialportcollection--newenum.md)<br/> | 唯讀<br/> | 集合的列舉值。<br/>                               |
| [**計數**](ivmserialportcollection-count.md)<br/>        | 唯讀<br/> | 此集合中的序列埠數目。<br/>                  |
| [**項目**](ivmserialportcollection-item.md)<br/>          | 唯讀<br/> | 對應至指定之索引的序列通訊埠物件。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPortCollection 定義為 dd3c6175-1f04-4341-9f85-104074880289<br/>    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> <dt>

[**IVMVirtualMachine：： Serialport**](ivmvirtualmachine-serialports.md)
</dt> </dl>

 

