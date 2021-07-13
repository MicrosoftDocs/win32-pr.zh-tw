---
description: 實行 IInkDesktopHost 介面。
ms.assetid: 7a577536-405b-400d-89bc-c3b3894b448d
title: InkDesktopHost 類別
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDesktopHost
api_type:
- COM
api_location:
- InkPresenterDesktop.idl
ms.openlocfilehash: 74eebdbdfdbe3a4018d63b1f2161687152ebb5cc
ms.sourcegitcommit: 1f917afc149b5cc449a4a25a87de311e4842734b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113689221"
---
# <a name="inkdesktophost-class"></a>InkDesktopHost 類別

實行 [**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost) 介面。

[**IInkDesktopHost**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkdesktophost)物件可讓您透過建立應用程式執行緒來進行筆跡輸入、處理和轉譯，以裝載 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop)物件，並將它插入應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md)視覺化樹狀結構中。

## <a name="members"></a>成員

**InkDesktopHost** 類別繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **InkDesktopHost** 也有下列類型的成員：

- [方法](#methods)

### <a name="methods"></a>方法

**InkDesktopHost** 類別有這些方法。

| 方法 | 描述 |
|---|---|
| [**CreateAndInitializeInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createandinitializeinkpresenter) | 在應用程式執行緒上建立 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件，並將它連接至應用程式的 [DirectComposition](../directcomp/directcomposition-portal.md) 視覺化樹狀結構，並設定物件的大小。<br/> |
| [**CreateInkPresenter**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-createinkpresenter) | 在應用程式執行緒上建立 [**IInkPresenterDesktop**](/windows/win32/api/inkpresenterdesktop/nn-inkpresenterdesktop-iinkpresenterdesktop) 物件。<br/> |
| [**QueueWorkItem**](/windows/win32/api/inkpresenterdesktop/nf-inkpresenterdesktop-iinkdesktophost-queueworkitem) | 將筆墨作業加入到工作佇列中，以便在 **InkDesktopHost** 執行緒上執行。<br/> |

## <a name="creationaccess-functions"></a>建立 \\ 存取函數

使用類別識別碼<strong>InkDesktopHost</strong>呼叫[<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ，以取得物件的參考。

``` C++
CoCreateInstance(__uuidof(InkDesktopHost), 
  nullptr, 
  CLSCTX_INPROC_SERVER, 
  IID_PPV_ARGS(&_spInkHost));
```

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|---|---|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/> |
| 標頭<br/>                   | <dl> <dt>InkPresenterDesktop。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>InkPresenterDesktop .idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkDesktopHost 定義為4ce7d875-a981-4140-a1ff-ad93258e8d59<br/> |

## <a name="related-topics"></a>相關主題

[筆跡展示者類別](ink-presenter-classes.md)、[畫筆和手寫筆互動](/windows/uwp/design/input/pen-and-stylus-interactions)、[筆墨分析範例](/samples/microsoft/windows-universal-samples/inkanalysis/)、[簡單筆墨範例](/samples/microsoft/windows-universal-samples/simpleink/)、[複雜](/samples/microsoft/windows-universal-samples/complexink/)的筆墨範例
