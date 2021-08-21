---
title: 'IVMMouse UsingAbsoluteCoordinates 屬性 (VPCCOMInterfaces .h) '
description: 抓取滑鼠座標是否代表絕對或相對座標。
ms.assetid: 668278f8-28ae-4128-9653-4985bddbe184
keywords:
- UsingAbsoluteCoordinates 屬性 Virtual PC
- UsingAbsoluteCoordinates 屬性 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，UsingAbsoluteCoordinates 屬性
topic_type:
- apiref
api_name:
- IVMMouse.UsingAbsoluteCoordinates
- IVMMouse.get_UsingAbsoluteCoordinates
- IVMMouse.put_UsingAbsoluteCoordinates
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5695489179abdf6719d9375ac5fa3e2b57a60f3e495475745637aad4b12a3737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118844145"
---
# <a name="ivmmouseusingabsolutecoordinates-property"></a>IVMMouse：： UsingAbsoluteCoordinates 屬性

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

抓取滑鼠座標是否代表絕對或相對座標。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_UsingAbsoluteCoordinates(
  [in]          VARIANT_BOOL usingAbsoluteCoordinates
);

HRESULT get_UsingAbsoluteCoordinates(
  [out, retval] VARIANT_BOOL *usingAbsoluteCoordinates
);
```



## <a name="property-value"></a>屬性值

**變異 \_TRUE** 表示將滑鼠裝置設定為使用絕對座標， **VARIANT \_ FALSE** 表示使用相對座標。

## <a name="error-codes"></a>錯誤碼



| 名稱/值                                                                                                                                                                       | 意義                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_確定</dt> <dt>0</dt> </dl>                                          | 作業成功。<br/>                                                                              |
| <dl> <dt>E \_指標</dt><dt>且顯示 0x80004003</dt> </dl>                            | 參數為 **Null**。<br/>                                                                                 |
| <dl> <dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt> </dl>               | 此滑鼠裝置所連接的虛擬機器目前不在執行中。<br/>                       |
| <dl> <dt>VM \_E \_ 新增 \_ 功能 \_ 無法 \_ </dt> <dt>0xA0040505</dt> </dl> | 未安裝整合元件。 需要整合元件才能使用絕對座標。<br/> |
| <dl> <dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt> </dl>                    | 已發生未預期的錯誤。<br/>                                                                          |



## <a name="remarks"></a>備註

這個屬性只會在此物件的本機上，而新的 [**IVMMouse**](ivmmouse.md)物件會預設為 **VARIANT \_ FALSE** 。 請注意，您必須安裝整合元件，才能使用絕對座標。

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

 

