---
title: 'IVMNetworkAdapter IsEthernetAddressDynamic 屬性 (VPCCOMInterfaces .h) '
description: 判斷是否動態產生乙太網路位址。
ms.assetid: 7bd87868-f1d1-48e5-9e1b-04d2126f9dad
keywords:
- IsEthernetAddressDynamic 屬性 Virtual PC
- IsEthernetAddressDynamic 屬性 Virtual PC，IVMNetworkAdapter 介面
- IVMNetworkAdapter 介面 Virtual PC，IsEthernetAddressDynamic 屬性
topic_type:
- apiref
api_name:
- IVMNetworkAdapter.IsEthernetAddressDynamic
- IVMNetworkAdapter.get_IsEthernetAddressDynamic
- IVMNetworkAdapter.put_IsEthernetAddressDynamic
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b16074243094d410e8d39538b024120daa1871e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024536"
---
# <a name="ivmnetworkadapterisethernetaddressdynamic-property"></a>IVMNetworkAdapter：： IsEthernetAddressDynamic 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷是否動態產生乙太網路位址。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IsEthernetAddressDynamic(
  [in]          VARIANT_BOOL isDynamic
);

HRESULT get_IsEthernetAddressDynamic(
  [out, retval] VARIANT_BOOL *isDynamic
);
```



## <a name="property-value"></a>屬性值

\_如果應動態產生乙太網路位址，則設定為 variant TRUE， \_ 如果乙太網路位址為靜態，則為 variant FALSE。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                    | 意義                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                                                                                                             |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>                                                                                                                                |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl> | 找不到虛擬機器。 如果在建立 [**IVMNetworkAdapter**](ivmnetworkadapter.md) 物件之後移除電腦，就可能發生這種情況。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                                                                                                                         |



## <a name="remarks"></a>備註

針對大部分的虛擬網路介面，這個屬性應該設定為 **TRUE** (預設) 。 如果來賓中的軟體需要靜態乙太網路位址，則應該將此屬性設定為 **FALSE**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMNetworkAdapter 定義為 e32e4165-22b8-4dc0-8d57-850171ae207a<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMNetworkAdapter**](ivmnetworkadapter.md)
</dt> </dl>

 

