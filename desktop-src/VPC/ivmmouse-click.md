---
title: 'IVMMouse Click method (VPCCOMInterfaces. h) '
description: 模擬滑鼠按鍵的點擊。
ms.assetid: f16e36d6-34ca-4d65-95e4-1a6660d0abd0
keywords:
- 按一下 [方法虛擬電腦]
- 按一下 [方法 Virtual PC，IVMMouse 介面]
- IVMMouse 介面 Virtual PC，按一下 [方法]
topic_type:
- apiref
api_name:
- IVMMouse.Click
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d1d1aaf538ac6b30a27df904729f2ad3187ebde29cb915c3d7ef35d1e9cf57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974247"
---
# <a name="ivmmouseclick-method"></a>IVMMouse：： Click 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

模擬滑鼠按鍵的點擊。

## <a name="syntax"></a>語法


```C++
HRESULT Click(
  [in] VMMouseButton buttonIndex
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*buttonIndex* \[在\]
</dt> <dd>

要按一下之按鈕的索引。 如需值的清單，請參閱 [**VMMouseButton**](vmmousebutton.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                        | 描述                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                              | 作業成功。<br/>                                                                                                          |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | 參數為 **Null**。<br/>                                                                                                             |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>   | 此滑鼠裝置所連接的虛擬機器目前不在執行中。<br/>                                                   |
| <dl> <dt>**VM \_E \_ 滑鼠 \_ 非 \_**</dt>使用中 <dt>0xA0040800</dt> </dl> | 無法完成作業，因為滑鼠裝置未啟動，或虛擬機器中目前未處於作用中狀態。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>        | 已發生未預期的錯誤。<br/>                                                                                                      |



 

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

 

