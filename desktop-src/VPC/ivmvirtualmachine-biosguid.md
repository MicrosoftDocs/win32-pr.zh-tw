---
title: 'IVMVirtualMachine BIOSGUID 屬性 (VPCCOMInterfaces .h) '
description: BIOS GUID。
ms.assetid: d866838d-31e9-41f1-be57-43e778b9db95
keywords:
- BIOSGUID 屬性 Virtual PC
- BIOSGUID 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，BIOSGUID 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BIOSGUID
- IVMVirtualMachine.get_BIOSGUID
- IVMVirtualMachine.put_BIOSGUID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10263e32ab71c2a5b9533b3dde6547f774d6b302
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843511"
---
# <a name="ivmvirtualmachinebiosguid-property"></a>IVMVirtualMachine：： BIOSGUID 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定 BIOS GUID。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BIOSGUID(
  [in]          BSTR biosGUID
);

HRESULT get_BIOSGUID(
  [out, retval] BSTR *biosGUID
);
```



## <a name="property-value"></a>屬性值

指定 BIOS GUID。 在十六進位數位前後加上左和右大括弧。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                               | 意義                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                  | 作業成功。<br/>                       |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                    | 參數為 **Null**。<br/>                          |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                 | 參數無效或為空字串。<br/>   |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>            | 未知的設定。<br/>                       |
| <dl> <dt>VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的</dt> <dt>0xA004020B</dt> </dl> | 虛擬機器處於執行中或已儲存狀態。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>            | 已發生未預期的錯誤。<br/>                   |



## <a name="remarks"></a>備註

在虛擬機器第一次啟動之後，此屬性才會包含有效的資訊。 如果在初始啟動之前讀取了空字串，則會傳回空字串。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

