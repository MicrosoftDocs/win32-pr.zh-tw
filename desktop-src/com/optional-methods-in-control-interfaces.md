---
title: 控制項介面中的選擇性方法
description: 控制項介面中的選擇性方法
ms.assetid: a26f7078-9286-4b21-b924-4b03d3849909
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e92303b9e4e6a5edd295d0895a9121eee70ea05ae2a8967a9346ea26b153e8b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859288"
---
# <a name="optional-methods-in-control-interfaces"></a>控制項介面中的選擇性方法

執行介面並不一定表示執行該介面的所有方法，並視需要執行任何動作，而不是傳回 E \_ >notimpl 或 S \_ OK。 下表識別介面的「支援」中所列介面的方法，這 [表示](what-support-for-an-interface-means.md) 控制項可以用這種方式執行的主題。 如果支援介面，則此處未列出的任何方法都必須完全執行。



| IOleControl                                                                                                   | 註解                                                                       |
|---------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**GetControlInfo**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-getcontrolinfo)、 [ **OnMnemonic**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onmnemonic)<br/> | 具有助憶鍵的控制項是必要的。<br/>                              |
| [**IOleControl：： OnAmbientPropertyChange**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-onambientpropertychange)<br/>                | 使用環境屬性之控制項的必要參數。<br/>                 |
| [**IOleControl::FreezeEvents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents)<br/>                                      | 查看 [事件凍結](event-freezing.md)<br/>                            |
| IOleObject                                                                                                    |                                                                                |
| [**SetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setmoniker)<br/>                                                        | 如果控制項未標記為 OLEMISC CANTLINKINSIDE，則為必要項 \_<br/> |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmoniker)<br/>                                                        | 如果控制項未標記為 OLEMISC CANTLINKINSIDE，則為必要項 \_<br/> |
| [**InitFromData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-initfromdata)<br/>                                                    | 選擇性<br/>                                                            |
| [**GetClipboardData**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getclipboarddata)<br/>                                            | 選擇性<br/>                                                            |
| [**SetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setextent)<br/>                                                          | 只對 >DVASPECT 內容為必要 \_<br/>                                |
| [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)<br/>                                                          | 只對 >DVASPECT 內容為必要 \_<br/>                                |
| [**SetColorScheme**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-setcolorscheme)<br/>                                                | 選擇性<br/>                                                            |
| [**DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)<br/>                                                                | 請參閱附注1<br/>                                                          |
| IOleInPlaceObject                                                                                             |                                                                                |
| [**CoNtextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | 選擇性<br/>                                                            |
| [**ReactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-reactivateandundo)<br/>                                   | 選擇性<br/>                                                            |
| IOleInPlaceActiveObject                                                                                       |                                                                                |
| [**CoNtextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>                                    | 選擇性<br/>                                                            |
| IViewObject2                                                                                                  |                                                                                |
| [**凍結**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-freeze)<br/>                                                               | 選擇性<br/>                                                            |
| [**解凍**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-unfreeze)<br/>                                                           | 選擇性<br/>                                                            |
| [**GetColorSet**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject-getcolorset)<br/>                                                     | 選擇性<br/>                                                            |
| IPersistStream、IPersistStreamInit、IPersistMemory                                                            |                                                                                |
| [**GetSizeMax**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststream-getsizemax)<br/>                                                    | 請參閱附註 2<br/>                                                          |



 

1.  具有屬性頁的控制項必須支援 OLEIVERB 屬性和 OLEIVERB 主要動詞的 [**IOleObject：:D overb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb) \_ \_ 。 可以是作用中的控制項必須支援 OLEIVERB \_ INPLACEACTI加值稅E 動詞的 DoVerb。 可以是 UI 作用中的控制項也必須支援 OLEIVERB \_ UIACTI加值稅E 動詞的 DoVerb。
2.  如果控制項支援 [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) 或 [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) ，而且可以傳回精確的值，則應該這麼做。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[控制項](controls.md)
</dt> </dl>

 

 





