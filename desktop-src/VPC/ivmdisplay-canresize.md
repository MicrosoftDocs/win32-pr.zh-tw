---
title: 'IVMDisplay Graphicswindow.canresize 屬性 (VPCCOMInterfaces .h) '
description: 判斷來賓是否允許解析變更。
ms.assetid: 97f2aad9-aa27-4db2-ac5d-fa9645f0e674
keywords:
- Graphicswindow.canresize 屬性 Virtual PC
- Graphicswindow.canresize 屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，Graphicswindow.canresize 屬性
topic_type:
- apiref
api_name:
- IVMDisplay.CanResize
- IVMDisplay.get_CanResize
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca865189b1fd155e0edf85bac9a36d94ffe5d656
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686412"
---
# <a name="ivmdisplaycanresize-property"></a>IVMDisplay：： Graphicswindow.canresize 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

判斷來賓是否允許解析變更。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CanResize(
  [out, retval] VARIANT_BOOL *canResize
);
```



## <a name="property-value"></a>屬性值

**變異 \_** 如果來賓允許解析變更，則為 TRUE，否則為 **VARIANT \_ FALSE** 。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                                                                              |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | 參數為 **Null**。<br/>                                                                                                                 |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>                    | 未知的設定。<br/>                                                                                                              |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | 虛擬機器必須正在執行，才能進行這種操作。<br/>                                                                                    |
| <dl> <dt>VM \_E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt> </dl>                    | 找不到虛擬機器的影片裝置。<br/>                                                                                   |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 無法使用 [整合元件] 功能;可能是未安裝整合元件，或已停用此功能。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                                                                                          |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

