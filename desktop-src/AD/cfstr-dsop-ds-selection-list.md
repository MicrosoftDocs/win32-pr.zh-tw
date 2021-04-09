---
title: 'CFSTR_DSOP_DS_SELECTION_LIST (Objsel) '
description: CFSTR \_ DSOP \_ ds \_ 選擇 \_ 清單剪貼簿格式會提供包含 DS \_ 選擇 \_ 清單結構的 HGLOBAL。 DS \_ 選擇 \_ 清單結構包含在目錄物件選擇器對話方塊中選取之專案的相關資料。
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934215"
---
# <a name="cfstr_dsop_ds_selection_list"></a>CFSTR \_ DSOP \_ DS \_ 選擇 \_ 清單

<dl> <dt>

<span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR \_ DSOP \_ DS \_ 選擇 \_ 清單**
</dt> <dd> <dl> <dt>

"CFSTR \_ DSOP \_ DS \_ SELECTION \_ LIST"
</dt> <dt>



**CFSTR \_ DSOP \_ DS \_ 挑選清單剪貼 \_ 簿** 格式是由呼叫 [**IDsObjectPicker：： InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)所取得的 [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject)所提供。 **CFSTR \_ DSOP \_ ds \_ 挑選清單剪貼 \_ 簿** 格式會提供包含 [**DS \_ 選擇 \_ 清單**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)結構的 **HGLOBAL** 。 **DS \_ 選擇 \_ 清單** 結構包含在 [目錄物件選擇器](directory-object-picker.md)對話方塊中選取之專案的相關資料。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Objsel。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DS \_ 選擇 \_ 清單**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[目錄物件選擇器](directory-object-picker.md)
</dt> </dl>

 

