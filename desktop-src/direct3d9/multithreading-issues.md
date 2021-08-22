---
description: 全螢幕 Direct3D 應用程式會提供 windows 控制碼給 Direct3D 執行時間。
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: " (Direct3D 9) 的多執行緒問題"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd86b07850a1134d214d02c8b809c825f7cab2971ee87f93bd66aeae1dbd4b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119371928"
---
# <a name="multithreading-issues-direct3d-9"></a> (Direct3D 9) 的多執行緒問題

全螢幕 Direct3D 應用程式會提供 windows 控制碼給 Direct3D 執行時間。 視窗會與執行時間連結。 這表示，所有傳遞至應用程式視窗訊息程式的訊息，都是由 Direct3D 執行時間本身的訊息處理常式所檢查。

顯示模式變更會受到基礎作業系統內建的支援常式影響。 發生模式變更時，系統會將數個訊息廣播至所有應用程式。 在 Direct3D 應用程式中，訊息會在視窗程式執行緒上收到，這不一定是呼叫 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) 或 [**IDirect3D9：： CreateDevice**](/windows/desktop/api) (的相同執行緒，也不一定是 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)的最終發行版本，而這可能會導致顯示模式變更) 。 Direct3D 執行時間會在內部維護數個重要區段。 因為 **IDirect3DDevice9：： Reset** 或 **IDirect3D9：： CreateDevice** 所造成的模式切換中至少會保留其中一個重要區段，所以當應用程式收到模式變更相關的視窗訊息時，仍會保留這些重要區段。

這種設計對多執行緒應用程式有一些影響。 尤其是，應用程式必須務必將其視窗訊息處理執行緒從其 Direct3D 執行緒中緊密隔離。 在某個執行緒上造成模式變更的應用程式，但在其視窗程式中的不同執行緒上進行 Direct3D 呼叫，會有鎖死的風險。

基於這些理由，Direct3D 的設計目的是要讓 [**IDirect3DDevice9：： Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)、 [**IDirect3D9：： CreateDevice**](/windows/desktop/api)、 [**IDirect3DDevice9：： TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)或最終發行的 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 只能從處理視窗訊息的相同執行緒呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計提示](programming-tips.md)
</dt> </dl>

 

 
