---
title: 'IVMMouse VerticalPosition 屬性 (VPCCOMInterfaces .h) '
description: 滑鼠的絕對 y 座標。
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- VerticalPosition 屬性 Virtual PC
- VerticalPosition 屬性 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，VerticalPosition 屬性
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935026"
---
# <a name="ivmmouseverticalposition-property"></a>IVMMouse：： VerticalPosition 屬性

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取滑鼠的絕對 y 座標。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>屬性值

指出滑鼠新位置的 y 座標。 使用絕對座標時，此值會指定滑鼠的新 y 座標。 使用相對座標時，此值會指定要在 y 方向移動滑鼠的圖元數。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                                                                                |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | 參數為 **Null**。<br/>                                                                                                                   |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | 此滑鼠裝置所連接的虛擬機器目前不在執行中。<br/>                                                         |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 您必須安裝整合元件才能取出滑鼠位置，或在使用絕對座標時設定滑鼠位置。<br/>       |
| <dl> <dt>VM \_E \_ 使用 \_ 相對 \_ 座標</dt> <dt>0xA0040802</dt> </dl>   | 滑鼠裝置目前設定為使用相對滑鼠座標。<br/>                                                                         |
| <dl> <dt>VM \_E \_ 滑鼠 \_ 非 \_ </dt>使用中 <dt>0xA0040800</dt> </dl>             | 如果滑鼠裝置未啟動，或虛擬機器中目前未啟用，則無法抓取絕對座標。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                                                                                            |



## <a name="remarks"></a>備註

使用相對座標時，無法抓取此屬性。

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

 

