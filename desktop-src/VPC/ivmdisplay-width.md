---
title: 'IVMDisplay Width 屬性 (VPCCOMInterfaces .h) '
description: VM 的顯示寬度（以圖元為單位）。
ms.assetid: a0062d75-dbb3-41ff-8112-87c1a31b088e
keywords:
- Width 屬性 Virtual PC
- Width 屬性 Virtual PC，IVMDisplay 介面
- IVMDisplay 介面 Virtual PC，Width 屬性
topic_type:
- apiref
api_name:
- IVMDisplay.Width
- IVMDisplay.get_Width
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db106804f81f52b669b90920699761061d97fb3412dd58b761f7da1701ec53b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654218"
---
# <a name="ivmdisplaywidth-property"></a>IVMDisplay：： Width 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取虛擬機器 (VM) 顯示的寬度（以圖元為單位）。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_Width(
  [out, retval] long *displayPixelWidth
);
```



## <a name="property-value"></a>屬性值

寬度（以圖元為單位）。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                         | 意義                                                                  |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                            | 作業成功。<br/>                                 |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>              | 參數為 **Null**。<br/>                                    |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl> | 虛擬機器必須正在執行，才能進行這種操作。<br/>       |
| <dl> <dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt> </dl>      | 虛擬機器無效或目前未執行。<br/> |
| <dl> <dt>VM \_E \_ NO \_ DISPLAY</dt> <dt>0xA0040850</dt> </dl>      | 找不到虛擬機器的有效顯示。<br/>     |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>      | 已發生未預期的錯誤。<br/>                             |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay 定義為960895e9-f743-4498-96aa-261f867e7fc5<br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMDisplay**](ivmdisplay.md)
</dt> </dl>

 

