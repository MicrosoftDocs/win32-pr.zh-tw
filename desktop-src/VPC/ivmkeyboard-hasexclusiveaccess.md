---
title: 'IVMKeyboard HasExclusiveAccess 屬性 (VPCCOMInterfaces .h) '
description: 指出此物件是否具有 VM 鍵盤裝置的獨佔控制。
ms.assetid: edba154e-e700-488c-9133-91649daecef1
keywords:
- HasExclusiveAccess 屬性 Virtual PC
- HasExclusiveAccess 屬性 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，HasExclusiveAccess 屬性
topic_type:
- apiref
api_name:
- IVMKeyboard.HasExclusiveAccess
- IVMKeyboard.get_HasExclusiveAccess
- IVMKeyboard.put_HasExclusiveAccess
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c01e13e331824a0d1b6834cbb27da7eb4b5420a3cd3dbec94cdbdd494c79c95b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136721"
---
# <a name="ivmkeyboardhasexclusiveaccess-property"></a>IVMKeyboard：： HasExclusiveAccess 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指出此物件是否有虛擬機器 (VM) 鍵盤裝置的獨佔控制。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HasExclusiveAccess(
  [in]          VARIANT_BOOL makeExclusive
);

HRESULT get_HasExclusiveAccess(
  [out, retval] VARIANT_BOOL *isExclusive
);
```



## <a name="property-value"></a>屬性值

如果已取得對 VM 鍵盤裝置的獨佔存取權，**則為 TRUE** ，否則為 **FALSE** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                   | 意義                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                      | 作業成功。<br/>                                                                                                                                                                                                        |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                        | *IsExclusive* 參數為 **Null**。<br/>                                                                                                                                                                                             |
| <dl> <dt>S \_FALSE</dt> <dt>1</dt> </dl>                                   | 已為此裝置設定要求的獨佔模式。 當您嘗試在取得獨佔模式時，或在先前未取得時嘗試釋放獨佔模式時，就會發生這種情況。<br/> |
| <dl> <dt>VM \_E \_ 設定 \_ 獨佔 \_ 模式 \_ 失敗</dt> <dt>0xA0040825</dt> </dl> | 無法依要求設定或發行獨佔模式。 這可能是因為 VM 已不再執行，或因為另一個進程已在 VM 的鍵盤裝置上取得獨佔模式。<br/>                                 |
| <dl> <dt>E \_INVALIDARG</dt> <dt>0x80000003</dt> </dl>                     | 指定的字串是空的，或包含不正確按鍵碼。<br/>                                                                                                                                                                      |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                | 已發生未預期的錯誤。<br/>                                                                                                                                                                                                    |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

