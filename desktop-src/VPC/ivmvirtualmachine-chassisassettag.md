---
title: 'IVMVirtualMachine ChassisAssetTag 屬性 (VPCCOMInterfaces .h) '
description: 底座資產標記。
ms.assetid: 469816a8-3078-4960-a5e1-79d65b5fc8fc
keywords:
- ChassisAssetTag 屬性 Virtual PC
- ChassisAssetTag 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，ChassisAssetTag 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.ChassisAssetTag
- IVMVirtualMachine.get_ChassisAssetTag
- IVMVirtualMachine.put_ChassisAssetTag
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7357546d330f21b55a24babaaad532aca3baca121c221c9f1be6493a6a78fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998688"
---
# <a name="ivmvirtualmachinechassisassettag-property"></a>IVMVirtualMachine：： ChassisAssetTag 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定底座資產標記。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ChassisAssetTag(
  [in]          BSTR chassisAssetTag
);

HRESULT get_ChassisAssetTag(
  [out, retval] BSTR *chassisAssetTag
);
```



## <a name="property-value"></a>屬性值

指定底座資產標記。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                               | 意義                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                                               |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                    | 參數為 **Null**。<br/>                                                  |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | 參數大於32個字元、空字串或無效。<br/> |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>            | 未知的設定。<br/>                                               |
| <dl> <dt>VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的</dt> <dt>0xA004020B</dt> </dl> | 虛擬機器處於執行中或已儲存狀態。<br/>                         |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                                           |



## <a name="remarks"></a>備註

在虛擬機器第一次啟動之後，此屬性才會包含有效的資訊。 如果在初始啟動之前讀取了空字串，則會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

