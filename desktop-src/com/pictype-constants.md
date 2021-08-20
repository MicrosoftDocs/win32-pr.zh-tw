---
title: 'PICTYPE 常數 (OleCtl) '
description: 描述圖片取得類型所傳回的圖片物件類型，以及 \_ 描述傳遞給 OleCreatePictureIndirect 之 PICTDESC 結構的 picType 成員中的圖片類型。
ms.assetid: 79f10687-f0eb-4b5e-a1a9-9186dbd0b51f
topic_type:
- apiref
api_name:
- PICTYPE_UNINITIALIZED
- PICTYPE_NONE
- PICTYPE_BITMAP
- PICTYPE_METAFILE
- PICTYPE_ICON
- PICTYPE_ENHMETAFILE
api_location:
- OleCtl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa6ac7be72ba34616a1ae8d596efbad3af761760c8f5e5c2bfa5dc8362593748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567648"
---
# <a name="pictype-constants"></a>PICTYPE 常數

描述 [**圖片：： get \_ 類型**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)所傳回的圖片物件類型，以及描述傳遞給 [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)之 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)結構的 **picType** 成員中的圖片類型。



| 常數/值                                                                                                                                                                                                                                  | 描述                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PICTYPE_UNINITIALIZED"></span><span id="pictype_uninitialized"></span><dl> <dt>**PICTYPE \_未初始化**</dt><dt>的 (-1)</dt> </dl> | 圖片物件目前未初始化。 此值僅適用于 [**圖片：： get \_ 類型**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type) 的傳回值，而且不能與 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構有效。<br/>  |
| <span id="PICTYPE_NONE"></span><span id="pictype_none"></span><dl> <dt>**PICTYPE \_無**</dt> <dt>0</dt> </dl>                               | 建立新的圖片物件時不會有初始化的狀態。 只有在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中，這個值才有效。<br/>                                                                        |
| <span id="PICTYPE_BITMAP"></span><span id="pictype_bitmap"></span><dl> <dt>**PICTYPE \_點陣圖**</dt> <dt>1</dt> </dl>                         | 圖片類型是點陣圖。 當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **bmp** 欄位包含相關的初始化參數。<br/>             |
| <span id="PICTYPE_METAFILE"></span><span id="pictype_metafile"></span><dl> <dt>**PICTYPE \_中繼檔**</dt> <dt>2</dt> </dl>                   | 圖片類型為中繼檔。 當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **wmf** 欄位包含相關的初始化參數。<br/>           |
| <span id="PICTYPE_ICON"></span><span id="pictype_icon"></span><dl> <dt>**PICTYPE \_圖示**</dt> <dt>3</dt> </dl>                               | 圖片類型是圖示。 當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **圖示** 欄位包含相關的初始化參數。<br/>             |
| <span id="PICTYPE_ENHMETAFILE"></span><span id="pictype_enhmetafile"></span><dl> <dt>**PICTYPE \_ENHMETAFILE**</dt> <dt>4</dt> </dl>          | 圖片類型是增強的中繼檔。 當此值發生在 [**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc) 結構中時，表示該結構的 **emf** 欄位包含相關的初始化參數。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>OleCtl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**圖片：： get \_ 類型**](/windows/desktop/api/OCIdl/nf-ocidl-ipicture-get_type)
</dt> <dt>

[**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)
</dt> <dt>

[**PICTDESC**](/windows/win32/api/olectl/ns-olectl-pictdesc)
</dt> </dl>

 

 





