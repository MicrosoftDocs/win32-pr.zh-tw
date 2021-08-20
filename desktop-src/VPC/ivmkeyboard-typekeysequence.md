---
title: 'IVMKeyboard TypeKeySequence 方法 (VPCCOMInterfaces .h) '
description: 模擬輸入的索引鍵清單（以逗號分隔）。
ms.assetid: ba4d4e43-cb2e-49ae-940d-2e81286d3473
keywords:
- TypeKeySequence 方法 Virtual PC
- TypeKeySequence 方法 Virtual PC，IVMKeyboard 介面
- IVMKeyboard 介面 Virtual PC，TypeKeySequence 方法
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeKeySequence
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565d31d04a31f72ea25b3477fb91d53d252f6173eec8bc2f40133db38eeb1619
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998858"
---
# <a name="ivmkeyboardtypekeysequence-method"></a>IVMKeyboard：： TypeKeySequence 方法

\[WindowsVirtual PC 不再適用于 Windows 8。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

模擬輸入的索引鍵清單（以逗號分隔）。

## <a name="syntax"></a>語法


```C++
HRESULT TypeKeySequence(
  [in] BSTR keySequence
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*keySequence* \[在\]
</dt> <dd>

要輸入的按鍵代碼（以逗號分隔）序列。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼/值                                                                                                                                                 | 描述                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0</dt> </dl>                       | 作業成功。<br/>                                   |
| <dl> <dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt> </dl>         | 參數為 **Null**。<br/>                                      |
| <dl> <dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | 指定的字串是空的，或包含不正確按鍵碼。<br/> |
| <dl> <dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt> </dl> | 已發生未預期的錯誤。<br/>                               |



 

## <a name="remarks"></a>備註

金鑰序列字串是一組以逗號分隔的索引鍵識別碼，用來模擬標準美國101按鍵的按鍵和發行順序。

如果索引鍵識別碼出現在字串中，但沒有先前的修飾詞，則會將按鍵按鍵的程式碼傳送到虛擬機器會話，緊接著其對應的金鑰發行程式碼。 金鑰修飾詞可以用來變更此行為。

例如，向下修飾詞會傳送下列金鑰識別碼的按鍵按鍵程式碼，而不會傳送金鑰發行程式碼。 當您在傳送其他索引鍵時，如果將 Ctrl、Alt 和 Shift 鍵保持在一起，則這非常有用。 若要釋放金鑰，必須連同先前的 UP 修飾詞一起包含在金鑰字串中。

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
</dt> <dt>

[主要序列](key-sequences.md)
</dt> </dl>

 

