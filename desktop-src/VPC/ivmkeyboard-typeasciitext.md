---
title: 'IVMKeyboard TypeAsciiText 方法 (VPCCOMInterfaces .h) '
description: 模擬輸入至來賓的一連串 ASCII 按鍵。
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- TypeAsciiText 方法 Virtual PC
- TypeAsciiText 方法 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，TypeAsciiText 方法
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05e1c2afce1fa21aa1017a2ac7975ddcf49d850e2dbbc3cfb12e69798600554
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118345262"
---
# <a name="ivmkeyboardtypeasciitext-method"></a>IVMKeyboard：： TypeAsciiText 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

模擬輸入至來賓的一連串 ASCII 按鍵。

## <a name="syntax"></a>語法


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*文字* \[在\]
</dt> <dd>

要在虛擬機器內輸入的 ASCII 文字字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | Description                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>     |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>        |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | 指定的字串是空的。<br/>    |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/> |



 

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

 

