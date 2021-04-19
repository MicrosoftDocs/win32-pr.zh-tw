---
description: 成功重設裝置時 (IDirect3DDevice9：： Reset) 或在全螢幕操作中建立 (IDirect3D9：： CreateDevice) ，建立裝置的 Direct3D 物件會標示為擁有該系統上的所有介面卡。
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: 'Multiple-Monitor 作業 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998428"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Multiple-Monitor 作業 (Direct3D 9) 

成功重設裝置時 ([**IDirect3DDevice9：： reset**](/windows/desktop/api)) 或在全螢幕操作中建立 ([**IDirect3D9：： CreateDevice**](/windows/desktop/api)) ，建立裝置的 Direct3D 物件會標示為擁有該系統上的所有介面卡。 此狀態稱為獨佔模式，且 Direct3D 物件擁有獨佔模式。 獨佔模式表示任何其他 Direct3D 物件所建立的裝置都不能假設全螢幕作業，也不會配置視訊記憶體。 此外，當 Direct3D 物件採用獨佔模式時，所有未進入全螢幕的裝置都會處於遺失狀態。 如需詳細資訊，請參閱 [ (Direct3D 9) 的遺失裝置 ](lost-devices.md)。

除了獨佔模式，Direct3D 物件也會收到裝置將使用之焦點視窗的通知。 當該 Direct3D 物件所擁有的最終全螢幕裝置重設為視窗模式或損毀時，就會釋放獨佔模式。

當 Direct3D 物件擁有獨佔模式時，裝置可以分為兩個類別。 裝置的第一個類別具有下列特性。

-   它們是由建立全螢幕裝置的相同 Direct3D 物件所建立。
-   它們與全螢幕裝置具有相同的焦點視窗。
-   它們代表與任何全螢幕裝置不同的介面卡。

此類別中的裝置對於其重設或建立的能力沒有任何限制，且未處於遺失狀態。 此類別中的裝置甚至可以放入全螢幕模式。

不屬於第一個類別目錄的裝置-由另一個 Direct3D 物件建立的裝置、使用不同的焦點視窗建立，以及針對裝置已全螢幕的介面卡建立的裝置，在獨佔模式遺失之前，無法重設並維持遺失狀態。 如此一來，多監視器應用程式就可以在全螢幕模式下放置數部裝置，但只有當這些裝置適用于不同的介面卡時，才會由相同的 Direct3D 物件建立，並共用相同的焦點視窗。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呈現場景](presenting-a-scene.md)
</dt> </dl>

 

 



