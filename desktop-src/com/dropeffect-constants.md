---
title: 'DROPEFFECT 常數 (Oleidl.idl) '
description: 表示拖放作業之效果的相關資訊。
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05c9a4fa961b0da2e654d4672392104b95e718bbb176167c7bb715c39f25cfc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736950"
---
# <a name="dropeffect-constants"></a>DROPEFFECT 常數

表示拖放作業之效果的相關資訊。 [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)函式和 [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)和 [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)中的許多方法都會使用此列舉的值。



| 常數/值                                                                                                                                                                                                                            | 描述                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_無**</dt> <dt>0</dt> </dl>                | 捨棄目標無法接受資料。<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_複製**</dt> <dt>1</dt> </dl>                | 將結果放置在複本中。 拖曳來源不會改變原始資料。<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_移動**</dt> <dt>2</dt> </dl>                | 拖曳來源應該移除資料。 <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_連結**</dt> <dt>4</dt> </dl>                | 拖曳來源應建立原始資料的連結。<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_滾動**</dt>的 <dt>0x80000000</dt> </dl> | 滾動即將開始，或目前在目標中發生。 除了其他值之外，還會使用這個值。<br/> |



## <a name="remarks"></a>備註

您的應用程式應該一律遮罩 **DROPEFFECT** 列舉中的值，以確保與未來的實施相容。 目前，只有 **DROPEFFECT** 值中的某些位置具有意義。 未來將會新增更多的位解釋。 拖曳來源和卸載目標應該在比較之前仔細地適當地遮罩這些值。 它們絕對不應該藉 \_ 由執行下列動作來比較 DROPEFFECT，例如 DROPEFFECT COPY：

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

相反地，應用程式應該一律遮罩值，或使用下列其中一種技術來搜尋值：

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

這可讓您定義新的捨棄效果，同時保留與現有程式碼的回溯相容性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Oleidl.idl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





