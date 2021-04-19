---
description: 專屬全螢幕模式的概念會保留在 Direct3D 9 中，但會在 IDirect3D9：： CreateDevice 和 IDirect3DDevice9：： Reset 方法呼叫中完全保持隱含。
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: '使用多個監視器系統 (Direct3D 9) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184a11f06d2296100a0b546e29770f44977b4de3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972927"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>使用多個監視器系統 (Direct3D 9) 

專屬全螢幕模式的概念會保留在 Direct3D 9 中，但會在 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) 和 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 方法呼叫中完全保持隱含。 每次成功重設或以全螢幕操作建立裝置時，建立裝置的 Direct3D 物件都會標示為擁有該系統上的所有介面卡。 此狀態稱為獨佔模式，而在此階段，Direct3D 物件會擁有獨佔模式。 獨佔模式表示任何其他 Direct3D9 物件所建立的裝置都不能假設全螢幕操作，也不會配置視訊記憶體。 此外，當 Direct3D9 物件採用獨佔模式時，全螢幕裝置以外的所有裝置都會進入遺失狀態。 如需如何處理遺失裝置的詳細資訊，請參閱 [ (Direct3D 9) 的裝置遺失 ](lost-devices.md)。

除了獨佔模式之外，Direct3D9 物件也會收到裝置所要使用之焦點視窗的通知。 當該 Direct3D9 物件所擁有的最後全螢幕裝置重設為視窗模式或損毀時，就會釋放獨佔模式。

當 Direct3D9 物件擁有獨佔模式時，裝置可以分為兩個類別。 裝置的第一個類別是由建立裝置已全螢幕的相同 Direct3D9 物件所建立的類別，與已經全螢幕的裝置具有相同的焦點視窗，並且代表任何全螢幕裝置的不同介面卡。 此類別中的裝置對於其重設或建立的能力沒有任何限制，且不會置於遺失狀態。 此類別中的裝置甚至可以放入全螢幕模式。

不在此類別中的裝置，也就是由不同 Direct3D9 物件建立的裝置，或具有不同焦點視窗的裝置，或具有裝置已滿全螢幕的某些介面卡，無法重設並保持在遺失狀態，直到獨佔模式遺失為止。

實際的含意是，多個監視器應用程式可以將數個裝置放在全螢幕模式中，但只有當這些裝置適用于不同的介面卡時，才會由相同的 Direct3D9 物件建立，且全都共用相同的焦點視窗。

當您使用相同的 [**IDirect3D9**](/windows/desktop/api) 物件和焦點視窗來建立新裝置時，您的原始裝置將會遺失其表面。 您必須在第一個裝置上呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ，才能讓您的應用程式使用它。 例如，若要建立兩個裝置，請執行下列動作：

1.  建立裝置1
2.  建立裝置2
3.  重設裝置1

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計秘訣](programming-tips.md)
</dt> </dl>

 

 
