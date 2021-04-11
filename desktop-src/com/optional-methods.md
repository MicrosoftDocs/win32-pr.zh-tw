---
title: 選擇性方法
description: 選擇性方法
ms.assetid: 8cdb5686-177c-48c9-8315-e5921520007c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 904aad26ecfba6396c9911b247443f9a956bca7f
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093340"
---
# <a name="optional-methods"></a>選擇性方法

OLE 元件可以執行介面，而不會在介面中執行每個方法的所有語義，而是在適當的情況下傳回 E \_ >notimpl 或 S \_ OK。 下表描述 ActiveX 控制項容器不需要執行的這些方法 (也就是控制項容器可以傳回 E \_ >notimpl) 。

下表說明選用的方法;請注意，方法必須仍然存在，但是可以直接傳回 E \_ >notimpl，而不是實作為實際的語法。 請注意，來自以下未列出之強制介面的任何方法都必須視為強制性，而且可能不會傳回 E \_ >notimpl。

## <a name="ioleclientsite"></a>IOleClientSite



| 方法                                                     | 註解                                                                                                 |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**SaveObject**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-saveobject)<br/> | 成功支援持續性所需。<br/>                                       |
| [**GetMoniker**](/windows/desktop/api/OleIdl/nf-oleidl-ioleclientsite-getmoniker)<br/> | 只有在容器支援連結至自己的表單或檔內的控制項時才需要。<br/> |



 

## <a name="ioleinplacesite"></a>IOleInPlaceSite



| 方法                                                                     | 註解                                                 |
|----------------------------------------------------------------------------|----------------------------------------------------------|
| [**CoNtextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/> | 選擇性<br/>                                      |
| [**捲動**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-scroll)<br/>                        | 可能會傳回 \_ FALSE，而不採取任何動作。<br/>           |
| [**DiscardUndoState**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-discardundostate)<br/>    | 可以傳回 \_ [確定]，但不採取任何動作。<br/>              |
| [**DeactivateAndUndo**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplacesite-deactivateandundo)<br/>  | 停用是強制性的;復原是選擇性的。 <br/> |



 

## <a name="iolecontrolsite"></a>>iolecontrolsite



| 方法                                                                          | 註解                                                                                                                                                            |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetExtendedControl**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-getextendedcontrol)<br/>     | 支援擴充控制項的容器所需。<br/>                                                                                                 |
| [**ShowPropertyFrame**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-showpropertyframe)<br/>       | 如果容器想要包含自己的屬性頁來處理擴充控制項屬性（除了控制項所提供的屬性），則為必要項。<br/> |
| [**TranslateAccelerator**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-translateaccelerator)<br/> | 可能會傳回 \_ FALSE，而不採取任何動作。<br/>                                                                                                                      |
| [**LockInPlaceActive**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrolsite-lockinplaceactive)<br/>       | 選擇性<br/>                                                                                                                                                 |



 

## <a name="idispatch-ambient-properties"></a>IDispatch (環境屬性) 



| 方法                      | 註解                                                                          |
|-----------------------------|-----------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | 支援非標準環境屬性之容器的必要元件。<br/> |
| GetTypeInfo<br/>      | 支援非標準環境屬性之容器的必要元件。<br/> |
| GetIDsOfNames<br/>    | 支援非標準環境屬性之容器的必要元件。<br/> |



 

## <a name="idispatch-event-sink"></a>IDispatch (事件接收) 



| 方法                      | 註解                                                                               |
|-----------------------------|----------------------------------------------------------------------------------------|
| GetTypeInfoCount<br/> | 控制項知道自己的型別資訊，因此不需要呼叫這個。<br/> |
| GetTypeInfo<br/>      | 控制項知道自己的型別資訊，因此不需要呼叫這個。<br/> |
| GetIDsOfNames<br/>    | 控制項知道自己的型別資訊，因此不需要呼叫這個。<br/> |



 

## <a name="ioleinplaceframe"></a>IOleInPlaceFrame



| 方法                                                                           | 註解                                                                |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| [**CoNtextSensitiveHelp**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-contextsensitivehelp)<br/>       |                                                                         |
| [**GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)<br/>                    | 具有工具列 UI (的容器的必要選項) <br/> |
| [**RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)<br/>  | 具有工具列 UI (的容器的必要選項) <br/> |
| [**SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)<br/>          | 具有工具列 UI (的容器的必要選項) <br/> |
| [**InsertMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-insertmenus)<br/>                   | 具有功能表 UI (的容器的必要選項) <br/>    |
| [**SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)<br/>                           | 具有功能表 UI (的容器的必要選項) <br/>    |
| [**RemoveMenus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-removemenus)<br/>                   | 具有功能表 UI (的容器的必要選項) <br/>    |
| [**SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)<br/>               | 只有具有狀態行的容器才需要<br/>        |
| [**EnableModeless**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-enablemodeless)<br/>             | 選擇性<br/>                                                     |
| [**TranslateAccelerator**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-translateaccelerator)<br/> | 選擇性<br/>                                                     |



 

## <a name="iolecontainer"></a>IOleContainer



| 方法                                                                    | 註解                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ParseDisplayName**](/windows/desktop/api/OleIdl/nf-oleidl-iparsedisplayname-parsedisplayname)<br/> | 只有在支援連結至控制項或容器中的其他內嵌時，才支援這項功能，因為這是針對標記系結的必要項。<br/>                                                                                                                  |
| [**LockContainer**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-lockcontainer)<br/>           | 適用于 ParseDisplayName<br/>                                                                                                                                                                                                                   |
| [**EnumObjects**](/windows/desktop/api/OleIdl/nf-oleidl-iolecontainer-enumobjects)<br/>               | 透過 [**IEnumUnknown**](/windows/win32/api/objidlbase/nn-objidlbase-ienumunknown)的列舉值傳回所有 ActiveX 控制項，但不一定都 (的所有物件，因為不保證所有物件都是 ActiveX 控制項;有些可能是一般的 Windows 控制項) 。<br/> |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[容器](containers.md)
</dt> </dl>

 

