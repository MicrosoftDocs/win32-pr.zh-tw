---
description: '下表描述可以引發 InkOverlay 物件事件的執行緒。EventThreadsCursorButtonDownFires 筆跡 threadCursorButtonUpFires 筆墨 threadCursorDownFires 的筆墨 threadCursorInRangeFires on 筆墨 threadCursorOutOfRangeFires 上的筆墨 ThreadDoubleClick (Automation only) 。只會在應用程式的使用者介面上引發 (UI) threadDoubleClick (受控程式庫) 。在應用程式 ui 上，于應用程式 ui threadMouseUpFires 上的應用程式 ui 上，于應用程式 ui 上的應用程式 ui 上，于應用程式 ui 上的應用程式 ui 上，于應用程式 ui 上的應用程式 ui 上引發：在應用程式 ui threadMouseWheelFires 上的應用程式 ui threadNewInAirPacketsFires 上，在應用程式 ui threadNewPacketsFires 的筆墨線程或在更新 InkOverlay 物件選取專案的執行緒上，于筆墨 threadSelectionMovedFires 筆墨上的筆墨 threadSelectionMovingFires 上筆跡的筆墨 threadSelectionResizedFires 上筆墨 threadSelectionResizingFires 的筆墨 threadStrokeFires 上筆墨 threadStrokesDeletedFires 的筆墨 threadStrokesDeletingFires 上筆墨 threadSystemGestureFires 的筆墨 '
ms.assetid: 5d679e66-6ea1-491e-86a8-974c4ec61b96
title: InkOverlay 物件事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6122709f043fa94f4c1b3d04fcd1c51bb3cd8982
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971557"
---
# <a name="inkoverlay-object-events"></a>InkOverlay 物件事件

下表描述可以引發 [**InkOverlay**](inkoverlay-class.md) 物件事件的執行緒。



| 事件                                                                             | 執行緒                                                                                                                                                                   |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CursorButtonDown**](inkoverlay-cursorbuttondown.md)                           | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**CursorButtonUp**](inkoverlay-cursorbuttonup.md)                               | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**CursorDown**](inkoverlay-cursordown.md)                                       | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**CursorInRange**](inkoverlay-cursorinrange.md)                                 | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**CursorOutOfRange**](inkoverlay-cursoroutofrange.md)                           | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**DoubleClick**](inkoverlay-doubleclick.md) (Automation) 。                  | 在應用程式的使用者介面上引發 (UI) 執行緒<br/>                                                                                                          |
| 僅) [**DoubleClick**](/previous-versions/ms567634(v=vs.100)) (受控程式庫。 | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**手勢**](inkoverlay-gesture.md)                                             | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**MouseDown**](inkoverlay-mousedown.md)                                         | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**MouseMove**](inkoverlay-mousemove.md)                                         | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**MouseUp**](inkoverlay-mouseup.md)                                             | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**滑鼠滾輪**](inkoverlay-mousewheel.md)                                       | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**NewInAirPackets**](inkoverlay-newinairpackets.md)                             | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**NewPackets**](inkoverlay-newpackets.md)                                       | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**畫**](inkoverlay-painted.md)                                             | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**繪畫**](inkoverlay-painting.md)                                           | 在應用程式的 UI 執行緒上引發<br/>                                                                                                                           |
| [**SelectionChanged**](inkoverlay-selectionchanged.md)                           | 在筆跡執行緒上引發，或在更新 [**InkOverlay**](inkoverlay-class.md) 物件的 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性的執行緒上引發<br/> |
| [**SelectionChanging**](inkoverlay-selectionchanging.md)                         | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**SelectionMoved**](inkoverlay-selectionmoved.md)                               | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**SelectionMoving**](inkoverlay-selectionmoving.md)                             | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**SelectionResized**](inkoverlay-selectionresized.md)                           | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**SelectionResizing**](inkoverlay-selectionresizing.md)                         | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**中風**](inkoverlay-stroke.md)                                               | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**StrokesDeleted**](inkoverlay-strokesdeleted.md)                               | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**StrokesDeleting**](inkoverlay-strokesdeleting.md)                             | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**SystemGesture**](inkoverlay-systemgesture.md)                                 | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**TabletAdded**](inkoverlay-tabletadded.md)                                     | 在筆跡執行緒上引發<br/>                                                                                                                                        |
| [**TabletRemoved**](inkoverlay-tabletremoved.md)                                 | 在筆跡執行緒上引發<br/>                                                                                                                                        |



 

 

