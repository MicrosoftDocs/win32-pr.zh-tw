---
title: 'IVMKeyboard 介面 (VPCCOMInterfaces .h) '
description: 控制虛擬機器內的鍵盤裝置。 您可以使用 IVMVirtualMachine 鍵盤屬性來抓取虛擬機器的 IVMKeyboard。
ms.assetid: a64a23b6-3937-40c6-af9d-fb341c04fbf7
keywords:
- IVMKeyboard 介面 Virtual PC
- IVMKeyboard 介面 Virtual PC，說明
topic_type:
- apiref
api_name:
- IVMKeyboard
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce2ddddd00de509278760a22fe3ab464f27c1c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106973302"
---
# <a name="ivmkeyboard-interface"></a>IVMKeyboard 介面

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

控制虛擬機器內的鍵盤裝置。 您可以使用 [**IVMVirtualMachine：：鍵盤**](ivmvirtualmachine-keyboard.md)屬性來抓取虛擬機器的 **IVMKeyboard** 。

## <a name="members"></a>成員

**IVMKeyboard** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 **IVMKeyboard** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IVMKeyboard** 介面具有這些方法。



| 方法                                                       | 描述                                                                   |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**IsPressed**](ivmkeyboard-ispressed.md)                   | 判斷指定的索引鍵是否已關閉。<br/>                      |
| [**PressAndReleaseKey**](ivmkeyboard-pressandreleasekey.md) | 模擬按下的按鍵，然後釋放。<br/>              |
| [**PressKey**](ivmkeyboard-presskey.md)                     | 模擬按下的按鍵。<br/>                                |
| [**ReleaseKey**](ivmkeyboard-releasekey.md)                 | 模擬要釋放的金鑰。<br/>                                    |
| [**TypeAsciiText**](ivmkeyboard-typeasciitext.md)           | 模擬輸入至來賓的一連串 ASCII 按鍵。<br/>       |
| [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)       | 模擬在來賓中輸入的索引鍵清單（以逗號分隔）。<br/> |



 

### <a name="properties"></a>屬性

**IVMKeyboard** 介面具有這些屬性。



| 屬性                                                                | 存取類型           | Description                                                                                                |
|:------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------|
| [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md)<br/> | 讀取/寫入<br/> | 指出此物件是否對虛擬機器的鍵盤裝置具有獨佔控制。<br/> |



 

## <a name="remarks"></a>備註

您可以透過數種方式將金鑰輸入至虛擬機器。 若要輸入標準的 ASCII 字元序列，請使用 [**TypeAsciiText**](ivmkeyboard-typeasciitext.md) 方法。 如果需要更大的彈性， **IVMKeyboard** 有數種設計用來與下列清單中的主要代碼搭配使用的方法。 [**TypeKeySequence**](ivmkeyboard-typekeysequence.md)方法可以接受以逗號分隔的按鍵碼字串，此字串將依序按下並依序在虛擬機器中放開。 除了這些按鍵碼以外，關鍵字可以用來強制只按下或只釋放按鍵。 UP 和 DOWN 關鍵字只適用于緊接在關鍵字後面的按鍵程式碼。

若要避免多個腳本、應用程式或使用者同時嘗試存取相同的鍵盤裝置，請將 [**HasExclusiveAccess**](ivmkeyboard-hasexclusiveaccess.md) 屬性設定為 **TRUE**。 如果有一個進程取得獨佔存取權，則在釋出獨佔存取權之前，會忽略其他程式傳送輸入到鍵盤裝置的任何嘗試。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard 定義為00695f2e-c5ad-4d6e-b1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Windows Virtual PC 介面](virtual-pc-interfaces.md)
</dt> <dt>

[主要序列](key-sequences.md)
</dt> </dl>

 

