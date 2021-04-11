---
description: 描述與 PresentEx 呼叫相關的 swapchain 統計資料。
ms.assetid: aa100b83-6fbf-442d-9891-7fc034a5b1d5
title: D3DPRESENTSTATS 結構 (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENTSTATS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b49a589fa1702f61e5a5daef806a5b36d464d0ec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196310"
---
# <a name="d3dpresentstats-structure"></a>D3DPRESENTSTATS 結構

描述與 [**PresentEx**](/windows/win32/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) 呼叫相關的 swapchain 統計資料。

## <a name="syntax"></a>語法


```C++
typedef struct _D3DPRESENTSTATS {
  UINT          PresentCount;
  UINT          PresentRefreshCount;
  UINT          SyncRefreshCount;
  LARGE_INTEGER SyncQPCTime;
  LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```



## <a name="members"></a>成員

<dl> <dt>

**PresentCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

目前正在輸出至螢幕的顯示裝置所執行的成功目前呼叫計數。 此參數實際上是最後一個出現之呼叫的目前識別碼，不一定是目前所發出的 API 呼叫總數。

</dd> <dt>

**PresentRefreshCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

在螢幕上顯示最後一次出現的 vblank 計數，vblank 計數會隨著每個 vblank 間隔遞增一次。

</dd> <dt>

**SyncRefreshCount**
</dt> <dd>

類型： **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

排程器上次呼叫 QueryPerformanceCounter 來取樣電腦時間時的 vblank 計數。

</dd> <dt>

**SyncQPCTime**
</dt> <dd>

類型： **[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

排程器上次取樣的電腦時間，藉由呼叫 [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)取得。

</dd> <dt>

**SyncGPUTime**
</dt> <dd>

類型： **[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

不使用這個值。

</dd> </dl>

## <a name="remarks"></a>備註

當9Ex 應用程式 (D3DSWAPEFFECT FLIPEX) 採用翻轉模式時 \_ ，應用程式可以在任何時間點呼叫 GetPresentStatistics 來偵測框架卸載。 實際上，使用者可以執行下列動作。

1.  轉譯為背景緩衝區
2.  呼叫存在
3.  呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構
4.  將下一個畫面格轉譯為背景緩衝區
5.  呼叫存在
6.  重複步驟4和 5 1 或更多次
7.  呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構
8.  比較兩個預存 D3DPRESENTSTATS 結構的 PresentRefreshCount 值。 應用程式可以根據 PresentRefreshCount 增量和 PresentCount 指派的框架呈現的假設，來計算特定 PresentCount 參數的對應 PresentRefreshCount。 如果上一次取樣的 PresentRefreshCount 不符合 PresentCount (也就是，如果 PresentRefreshCount 已遞增但 PresentCount 沒有，則會卸載畫面格。 ) 

應用程式可以藉由取樣任何兩個 PresentCount 和 GetPresentStats (實例來判斷是否已卸載框架) 。 例如，以與監視器重新整理速率相同的速率呈現的媒體應用程式 (例如，監視器重新整理速率為60Hz，應用程式每隔1/60 秒會顯示一個框架，) 想要呈現框架 A、B、C、D、E，每個畫面格都對應到目前的識別碼 (PresentCount) 1、2、3、7、8。

應用程式程式碼看起來會像下列順序。

1.  將框架 A 轉譯為背景緩衝區
2.  呼叫存在，PresentCount = 1
3.  呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構
4.  分別轉譯接下來的4個框架 B、C、D、E
5.  呼叫目前的4次，分別為 PresentCounts = 2、3、7、8
6.  呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構
7.  比較兩個預存 D3DPRESENTSTATS 結構的 PresentRefreshCount 值。 如果差異為2，也就是兩個 GetPresentStats API 呼叫之間已超過 2 vblank 間隔，則最後一個呈現的畫面格應該是畫面格 C。由於應用程式會顯示一次 vblank 的間隔， (監視器) 的重新整理頻率、呈現框架 A 與顯示畫面格 C 之間所經過的時間，應該是 2 vblanks。
8.  比較兩個預存 D3DPRESENTSTATS 結構的 PresentCount 值。 如果第一個 PresentCount 是 1 (對應至框架 A) ，而第二個 (PresentCount 對應至框架 C) ，則未卸載任何框架。 如果第二個 PresentCount 是3（對應至框架 D），則應用程式會知道一個框架已卸載。

請注意，呼叫 GetPresentStatistics 之後，不論 FLIPEX 模式 PresentEx 呼叫的狀態為何，都會進行處理。

**Windows Vista：** 目前的呼叫將會排入佇列，然後再處理 GetPresentStats 呼叫。

當應用程式偵測到呈現特定畫面格之後，就可以略過這些框架，並修正簡報以重新同步處理 vblank。 若要這樣做，應用程式可以單純地轉譯最晚的畫面格，並使用佇列中下一個正確的框架開始轉譯。 但是，如果應用程式已經開始轉譯延遲的畫面格，就可以在名為 D3DPRESENT FORCEIMMEDIATE 的 D3D9Ex 中使用新的呈現參數 \_ 。 旗標會在目前的 API 呼叫的參數中傳遞，並向執行時間指出框架將在下一個 vblank 間隔內立即處理，實際上完全不會顯示在螢幕上。 以下是在上一個範例中的最後一個步驟之後的應用程式使用範例。

1.  將下一個畫面格轉譯為背景緩衝區
2.  從 PresentRefreshCount 探索下一個畫面格已延遲
3.  將目前間隔設定為 D3DPRESENT \_ FORCEIMMEDIATE
4.  在下一個畫面上呼叫

應用程式可以用相同的方式同步處理影片和音訊串流，因為 GetPresentStatistics 的行為不會在該情況下變更。

D3D9Ex Flip 模式提供畫面格統計資訊給視窗型應用程式和全螢幕9Ex 應用程式。

**Windows Vista：** 使用 DWM Api 來取出目前的統計資料。

當桌面視窗管理員關閉時，使用切換模式的視窗模式9Ex 應用程式將會收到有限精確度的現有統計資料資訊。

* * Windows Vista： * *

如果應用程式的速度不夠快，無法跟上監視器的重新整理率，可能是因為硬體太慢或系統資源不足，則可能會遇到圖形問題。 問題就是所謂的視覺化擁塞中斷。 如果監視設定為在 60 Hz 重新整理，且應用程式只能管理 30 fps，則一半的畫面格將會發生問題。

應用程式可以藉由追蹤 SynchRefreshCount 來偵測出問題。 例如，應用程式可能會執行下列一連串的動作。

1.  轉譯為背景緩衝區。
2.  呼叫存在。
3.  呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構。
4.  將下一個畫面格轉譯為背景緩衝區。
5.  呼叫存在。
6.  呼叫 GetPresentStats 並儲存產生的 D3DPRESENTSTATS 結構。
7.  比較兩個預存 D3DPRESENTSTATS 結構的 SyncRefreshCount 值。 如果差異大於一，則會略過框架。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
