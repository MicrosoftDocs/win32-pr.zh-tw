---
title: 'IVMNetworkAdapter 介面 (VPCCOMInterfaces .h) '
description: 作為虛擬網路介面卡的介面。
ms.assetid: df050706-09be-47d1-9ae1-1eb0e1836d64
keywords:
- IVMNetworkAdapter 介面 Virtual PC
- IVMNetworkAdapter 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74a0ccf722715896743129b6666609bd8a88df3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384749"
---
# <a name="ivmnetworkadapter-interface"></a>IVMNetworkAdapter 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

作為虛擬網路介面卡的介面 (NIC) 。 它是用來設定虛擬機器的網路連線方式。 您可以使用 [**IVMVirtualMachine：： AddNetworkAdapter**](ivmvirtualmachine-addnetworkadapter.md) 和 [**IVMVirtualMachine：： RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md)來新增和移除網路介面卡。 您也可以從 [**IVMVirtualMachine：： NetworkAdapters**](ivmvirtualmachine-networkadapters.md)或 [**IVMVirtualNetwork：： NetworkAdapters**](ivmvirtualnetwork-networkadapters.md)屬性傳回的 [**IVMNetworkAdapterCollection**](ivmnetworkadaptercollection.md)集合中取出 **IVMNetworkAdapter** 物件。

## <a name="members"></a>成員

**IVMNetworkAdapter** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMNetworkAdapter** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMNetworkAdapter** 介面具有這些方法。



| 方法                                                                         | 描述                                                                 |
|:-------------------------------------------------------------------------------|:----------------------------------------------------------------------------|
| [**\_ID**](ivmnetworkadapter--id.md)                                          | 抓取此網路介面的內部識別碼。<br/>     |
| [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md)     | 將網路介面附加至指定的虛擬網路。<br/> |
| [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md) | 從虛擬網路卸離網路介面。<br/>         |



 

### <a name="properties"></a>屬性

**IVMNetworkAdapter** 介面具有這些屬性。



| 屬性                                                                                  | 存取類型           | Description                                                                 |
|:------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------|
| [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md)<br/>                   | 讀取/寫入<br/> | 網路介面的 Ethernet (MAC) 位址。<br/>             |
| [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md)<br/> | 讀取/寫入<br/> | 指出是否動態產生乙太網路位址。<br/> |
| [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md)<br/>                     | 唯讀<br/>  | 與此網路介面相關聯的虛擬機器。<br/>      |
| [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md)<br/>                     | 唯讀<br/>  | 網路介面所連接的虛擬網路。<br/>  |



 

## <a name="remarks"></a>備註

網路介面的預設乙太網路位址是 "00-00-00-00-00-00"，大部分的作業系統都會將其視為不正確乙太網路位址。 如果 [**IsEthernetAddressDynamic**](ivmnetworkadapter-isethernetaddressdynamic.md) 設定為 **FALSE**，則必須使用有效的乙太網路位址來初始化 [**EthernetAddress**](ivmnetworkadapter-ethernetaddress.md) 。

下列程式說明如何使用 **IVMNetworkAdapter** 介面。

**將虛擬 NIC 連結至主機 NIC**

-   虛擬 (來賓) Nic 不會直接連接至主機 NIC。 相反地，虛擬 NIC 會連接到連接至主機 NIC 的虛擬網路。 如需設定虛擬網路的詳細資訊，請參閱 [**IVMVirtualNetwork**](ivmvirtualnetwork.md)。 若要將虛擬 NIC 連結至虛擬網路，請使用 [**AttachToVirtualNetwork**](ivmnetworkadapter-attachtovirtualnetwork.md) 方法。

**中斷虛擬 NIC 與虛擬網路的連線**

-   [**DetachFromVirtualNetwork**](ivmnetworkadapter-detachfromvirtualnetwork.md)方法會將虛擬 NIC 從虛擬網路卸離。 呼叫這個函數之後， [**VirtualNetwork**](ivmnetworkadapter-virtualnetwork.md) 屬性會傳回不正確虛擬網路識別碼。

**如果您有虛擬 NIC 物件，則從虛擬機器移除虛擬 NIC**

1.  使用 [**VirtualMachine**](ivmnetworkadapter-virtualmachine.md) 屬性，取得與虛擬 NIC 相關聯的虛擬機器。
2.  使用目前的物件做為 [**IVMVirtualMachine：： RemoveNetworkAdapter**](ivmvirtualmachine-removenetworkadapter.md) 方法的參數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



 

