---
title: 多執行緒 Direct2D 應用程式
description: 描述建立多執行緒 Direct2D 應用程式的最佳做法。
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5710435f263e7b0f735581e03416f1d01733711429ad95b3ed25e473aca6d936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636390"
---
# <a name="multithreaded-direct2d-apps"></a>多執行緒 Direct2D 應用程式

如果您開發 [Direct2D](./direct2d-portal.md) 應用程式，您可能需要從一個以上的執行緒存取 Direct2D 資源。 在其他情況下，您可能會想要使用多執行緒處理，以取得更佳的效能或更佳的回應性 (例如使用一個執行緒進行螢幕顯示，以及使用個別的執行緒來進行離線轉譯) 。

本主題說明在幾乎不需要[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)轉譯的情況下開發多執行緒[Direct2D](./direct2d-portal.md)應用程式的最佳做法。 並行問題所造成的軟體瑕疵可能很難追蹤，而且在規劃多執行緒原則和遵循此處所述的最佳作法方面很有説明。

> [!Note]  
> 如果您從兩個不同的單一執行緒 Direct2D factory 存取所建立的兩個 [Direct2D](./direct2d-portal.md) 資源，則只要基礎 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 裝置和裝置內容也不同，就不會造成存取衝突。 談到本文中的「存取 Direct2D 資源」時，除非另有說明，否則它實際上是指「存取從相同 Direct2D 裝置建立的 Direct2D 資源」。

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>開發只呼叫 Direct2D Api 的 Thread-Safe 應用程式

您可以建立多執行緒 [Direct2D](./direct2d-portal.md) factory 實例。 您可以從多個執行緒使用和共用多執行緒處理站和其所有資源，但 (透過 Direct2D 呼叫對這些資源的存取) 由 Direct2D 序列化，因此不會發生存取衝突。 如果您的應用程式只呼叫 Direct2D Api，則 Direct2D 會自動以較小的額外負荷在細微層級中完成這類保護。 在這裡建立多執行緒處理站的程式碼。

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

此處的影像顯示 [Direct2D](./direct2d-portal.md) 如何序列化兩個使用 Direct2D API 進行呼叫的執行緒。

![兩個序列化執行緒的圖表。](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>使用極短的 Direct3D 或 DXGI 呼叫來開發 Thread-Safe Direct2D 應用程式

[Direct2D](./direct2d-portal.md)應用程式通常也會進行某些[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)或 DXGI 呼叫。 例如，顯示執行緒會在 Direct2D 中繪製，然後使用 [**DXGI 交換鏈**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)呈現。

在此情況下，請確保執行緒安全性更複雜：某些 [Direct2D](./direct2d-portal.md) 呼叫會間接存取基礎 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 資源，而另一個呼叫 direct3d 或 DXGI 的執行緒可能會同時存取這些資源。 因為這些 Direct3D 或 DXGI 呼叫不 Direct2d 感知和控制，所以您需要建立多執行緒 Direct2D factory，但您必須執行 mor，以避免發生存取衝突。

此圖表顯示 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 資源存取衝突，因為執行緒 T0 透過 [Direct2D](./direct2d-portal.md) 呼叫間接存取資源，而 T2 直接透過 Direct3D 或 DXGI 呼叫存取相同的資源。

> [!Note]  
> [Direct2D](./direct2d-portal.md)提供的執行緒保護 (此映射中的藍色鎖定) 在此案例中並沒有説明。

 

![執行緒保護圖表。](images/multi-thread2.png)

為了避免此處的資源存取衝突，建議您明確取得 [Direct2D](./direct2d-portal.md) 用於內部存取同步處理的鎖定，並線上程需要進行可能會導致存取衝突的 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 DXGI 呼叫（如下所示）時套用該鎖定。 尤其是，您應該特別注意使用例外狀況的程式碼或以 HRESULT 傳回碼為基礎的早期系統。 基於這個理由，建議您使用 RAII (資源取得是初始化) 模式，以呼叫 [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) 和 [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) 方法。

> [!Note]  
> 請務必將呼叫與 [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) 和 [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) 方法配對，否則您的應用程式可能會鎖死。

 

此處的程式碼顯示如何鎖定和解除鎖定 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 DXGI 呼叫的時機。


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> 某些 [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 DXGI 呼叫 (特別 [**IDXGISwapChain：:P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) 重新傳送) 可能會在呼叫函式或方法的程式碼中取得鎖定及/或觸發回呼。 您應該注意這一點，並確保這類行為不會造成鎖死。 如需詳細資訊，請參閱 [ [DXGI 總覽](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) ] 主題。

 

![direct2d 和 direct3d 執行緒鎖定圖表。](images/multi-thread3.png)

當您使用 [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) 和 [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) 方法時，呼叫會受到自動 [Direct2D](./direct2d-portal.md) 和明確鎖定的保護，因此應用程式不會碰到存取衝突。

有其他方法可以解決此問題。 不過，我們建議您明確地使用[Direct2D](./direct2d-portal.md)鎖定來保護[Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)或 DXGI 呼叫，因為它通常會提供較佳的效能，因為它會以更細微的層級來保護平行存取，而且在 direct2d 涵蓋下的額外負荷較低。

## <a name="ensuring-atomicity-of-stateful-operations"></a>確保具狀態作業的不可部分完成性

雖然 [DirectX](/previous-versions//ee663301(v=vs.85)) 的安全線程功能可協助確保不會同時進行兩個個別的 api 呼叫，您也必須確定讓具狀態 API 呼叫的執行緒不會互相干擾。 範例如下。

1.  有兩行文字是您想要以執行緒0呈現的螢幕 () ，以及執行緒 1) 的非畫面 (：行 \# 1 是 "A"，而第 \# 2 行是 "B"，這兩個都是以實心黑色筆刷繪製。
2.  執行緒1會繪製第一行文字。
3.  執行緒0會對使用者輸入做出反應，並將兩個文字行分別更新為 "B" 和 "，以及將筆刷色彩變更為純紅色，以供自己的繪圖使用;
4.  執行緒1會繼續以紅色色彩筆刷繪製第二行文字（現在是 "of"）。
5.  最後，我們會在非畫面繪圖目標上取得兩行文字：以黑色顯示「A」，並以紅色顯示「大於」。

![開啟和關閉畫面執行緒的圖表。](images/multi-thread4.png)

在頂端的資料列中，執行緒0會使用目前的文字字串和目前的黑色筆刷來繪製。 執行緒1只會在上半部完成全螢幕繪製。

在中間的資料列中，執行緒0會回應使用者互動、更新文字字串和筆刷，然後重新整理畫面。 此時，執行緒1會遭到封鎖。 在底部的資料列中，執行緒1之後的最後一個離螢幕轉譯會繼續使用改變的筆刷和改變的文字字串來繪製下半部。

若要解決此問題，建議您針對每個執行緒都有個別的內容，以便：

-   您應建立裝置內容的複本，讓可變動的資源 (也就是在顯示或列印期間可能會有所不同的資源，例如文字內容或範例中的純色筆刷，在轉譯時不會變更) 不會變更。 在此範例中，您應該在繪製前維護這兩行文字和色彩筆刷的複本。 如此一來，您就能確保每個執行緒都有完整且一致的內容可供繪製和呈現。
-   您應該共用大量資源 (例如點陣圖和複雜效果圖形) ，這些會初始化一次，然後不會線上程之間修改來提高效能。
-   您可以共用輕量資源 (例如純色筆刷和文字格式) 這些會初始化一次，然後不會線上程之間修改

## <a name="summary"></a>總結

當您開發多執行緒 [Direct2D](./direct2d-portal.md) 應用程式時，您必須建立多執行緒 Direct2D factory，然後從該 factory 衍生所有 Direct2D 資源。 如果執行緒會進行 [direct3d](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) 或 dxgi 呼叫，您也必須明確取得，然後套用 Direct2D 鎖定來保護這些 DIRECT3D 或 dxgi 呼叫。 此外，您必須針對每個執行緒擁有可變動資源的複本，以確保內容完整性。
