---
title: 'IVMGuestOS ProductType 屬性 (VPCCOMInterfaces .h) '
description: 抓取虛擬機器中執行之客體作業系統的產品類型。
ms.assetid: 426cd456-42a6-4bcd-a7a2-3aec258b02cb
keywords:
- ProductType 屬性 Virtual PC
- ProductType 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，ProductType 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.ProductType
- IVMGuestOS.get_ProductType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bc79ffd0717ac0949103a05d1bcdaa96da48d7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969162"
---
# <a name="ivmguestosproducttype-property"></a>IVMGuestOS：:P roductType 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬機器中執行之客體作業系統的產品類型。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_ProductType(
  [out, retval] BSTR *productType
);
```



## <a name="property-value"></a>屬性值

產品類型。 以下是支援的字串值。



| 值                                                                                  | 意義                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>"0x0000002"</dt> </dl> | 系統是網域控制站，而作業系統是 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。<br/>                                                                                                   |
| <dl> <dt>"0x0000003"</dt> </dl> | 作業系統是 Windows Server 2008 R2、Windows Server 2008、Windows Server 2003 R2、Windows Server 2003 或 Windows 2000 Server。<br/> 請注意，同時也是網域控制站的伺服器會回報為 **ver \_ nt \_ 域 \_ 控制器**，而不是 **\_ nt \_ server**。<br/> |
| <dl> <dt>"0x0000001"</dt> </dl> | 作業系統是 Windows 7、Windows Vista、Windows XP 或 Windows 2000 Professional。<br/>                                                                                                                                                                                       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMGuestOS**](ivmguestos.md)
</dt> </dl>

 

