---
title: 'IVMVirtualMachine BaseBoardSerialNumber 屬性 (VPCCOMInterfaces .h) '
description: 基本板序號。
ms.assetid: 374ad471-e0de-4e55-bab6-f7ddf3e5797f
keywords:
- BaseBoardSerialNumber 屬性 Virtual PC
- BaseBoardSerialNumber 屬性 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，BaseBoardSerialNumber 屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.BaseBoardSerialNumber
- IVMVirtualMachine.get_BaseBoardSerialNumber
- IVMVirtualMachine.put_BaseBoardSerialNumber
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2aaf205874eb7b8aaaead44a4d1a4b2775be4e01e076f1cc716058f8f9e45a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119653078"
---
# <a name="ivmvirtualmachinebaseboardserialnumber-property"></a>IVMVirtualMachine：： BaseBoardSerialNumber 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取並設定基本板序號。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BaseBoardSerialNumber(
  [in]          BSTR baseBoardSerialNumber
);

HRESULT get_BaseBoardSerialNumber(
  [out, retval] BSTR *baseBoardSerialNumber
);
```



## <a name="property-value"></a>屬性值

指定基本電路板序號。

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

 

