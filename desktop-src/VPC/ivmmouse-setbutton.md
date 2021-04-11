---
title: 'IVMMouse SetButton 方法 (VPCCOMInterfaces .h) '
description: 將目前狀態 () 指定的滑鼠按鍵。
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- SetButton 方法 Virtual PC
- SetButton 方法 Virtual PC，IVMMouse 介面
- IVMMouse 介面 Virtual PC，SetButton 方法
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105677"
---
# <a name="ivmmousesetbutton-method"></a>IVMMouse：： SetButton 方法

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

將目前狀態 () 指定的滑鼠按鍵。

## <a name="syntax"></a>語法


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*buttonIndex* \[在\]
</dt> <dd>

按鈕索引。 如需值的清單，請參閱 [**VMMouseButton**](vmmousebutton.md)。

</dd> <dt>

*向下* \[在\]
</dt> <dd>

新的按鈕狀態。 如果按鈕狀態設為 down，則使用 **TRUE** ，如果要設定為向上則使用 **FALSE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                        | Description                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                              | 作業成功。<br/>                                                                                                          |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | *ButtonIndex* 參數無效。<br/>                                                                                              |
| <dl> <dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt> </dl>   | 此滑鼠裝置所連接的虛擬機器目前不在執行中。<br/>                                                   |
| <dl> <dt>**VM \_E \_ 滑鼠 \_ 非 \_**</dt>使用中 <dt>0xA0040800</dt> </dl> | 無法完成作業，因為滑鼠裝置未啟動，或虛擬機器中目前未處於作用中狀態。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl>        | 已發生未預期的錯誤。<br/>                                                                                                      |



 

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

 

