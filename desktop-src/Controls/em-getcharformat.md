---
title: 'EM_GETCHARFORMAT 訊息 (Richedit .h) '
description: 判斷 rich edit 控制項中的字元格式。
ms.assetid: 210b8719-5ed7-49f2-bd93-8a4e1efab1e8
keywords:
- EM_GETCHARFORMAT message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd71db4d3a13f2acfe33c2843b0d9aad46c6f9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025180"
---
# <a name="em_getcharformat-message"></a>EM \_ GETCHARFORMAT 訊息

判斷 rich edit 控制項中的字元格式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定要從其中抓取格式的文字範圍。 它可以是下列值之一。



| 值                                                                                                                                                         | 意義                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF \_ 預設值**</dt> </dl>       | 預設的字元格式。<br/>             |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SCF \_ 選取專案**</dt> </dl> | 目前選取範圍的字元格式。<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)結構，此結構會接收第一個字元的屬性。 **DwMask** 成員會指定整個選取範圍中的屬性是一致的。 例如，如果整個選取範圍是斜體或不是斜體，則 \_ 會設定 CFM 斜體; 如果選取範圍部分為斜體，則 \_ 不會設定 CFM 斜體。

Microsoft Rich Edit 2.0 和更新版本：此參數可以是 [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) 結構的指標，也就是 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) 結構的延伸。 傳送 **EM \_ GETCHARFORMAT** 訊息之前，請先設定結構的 **cbSize** 成員來指出結構的版本。

</dd> </dl>

## <a name="return-value"></a>傳回值

此訊息會傳回 [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)結構之 **dwMask** 成員的值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**參考**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





