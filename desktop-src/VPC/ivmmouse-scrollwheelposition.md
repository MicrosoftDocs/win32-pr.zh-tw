---
title: 'IVMMouse ScrollWheelPosition 屬性 (VPCCOMInterfaces .h) '
description: 調整滑鼠 (相對) 的 z 座標。
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- ScrollWheelPosition 屬性 Virtual PC
- ScrollWheelPosition 屬性 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，ScrollWheelPosition 屬性
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686404"
---
# <a name="ivmmousescrollwheelposition-property"></a>IVMMouse：： ScrollWheelPosition 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

調整滑鼠 (相對) 的 z 座標。

此屬性是唯寫的。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>屬性值

Z 座標，指出滑鼠沿著 Z 軸移動的圖元數。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                     | 意義                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                        | 作業成功。<br/>                                                                |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>             | 此滑鼠裝置所連接的虛擬機器目前不在執行中。<br/>         |
| <dl> <dt>VM \_E \_ 滑鼠 \_ 非 \_ </dt>使用中 <dt>0xA0040800</dt> </dl>           | 滑鼠裝置尚未開機，或目前未在虛擬機器中啟用。<br/> |
| <dl> <dt>VM \_E \_ 使用 \_ 絕對 \_ 座標</dt> <dt>0xA0040801</dt> </dl> | 當滑鼠裝置使用絕對座標時，無法設定捲軸位置。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                  | 已發生未預期的錯誤。<br/>                                                            |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse 定義為 ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

