---
title: 'IVMMouse GetButton 方法 (VPCCOMInterfaces .h) '
description: 抓取指定滑鼠按鍵的目前狀態。
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- GetButton 方法 Virtual PC
- GetButton 方法 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，GetButton 方法
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af37a303c90fb9c60020f19f22767ec508c53fdc54bcefa533dabc780c38f16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007158"
---
# <a name="ivmmousegetbutton-method"></a>IVMMouse：： GetButton 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取所指定滑鼠按鍵的目前狀態 (向上或向下) 。

## <a name="syntax"></a>語法


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*buttonIndex* \[在\]
</dt> <dd>

正在要求其狀態的按鈕索引。 如需值的清單，請參閱 [**VMMouseButton**](vmmousebutton.md)。

</dd> <dt>

*isDown* \[退出，retval\]
</dt> <dd>

指定之按鈕的狀態。 如果此按鈕目前在虛擬機器中是關閉的，**則為 TRUE** ，否則為 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                        | 描述                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                              | 作業成功。<br/>                                                        |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>                | *IsDown* 參數為 **Null**。<br/>                                                  |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | *ButtonIndex* 參數無效。<br/>                                            |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>   | 此滑鼠裝置所連接的虛擬機器目前不在執行中。<br/> |
| <dl> <dt>**VM \_E \_ 滑鼠 \_ 非 \_**</dt>使用中 <dt>0xA0040800</dt> </dl> | 滑鼠裝置尚未開機。<br/>                                            |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>        | 已發生未預期的錯誤。<br/>                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

