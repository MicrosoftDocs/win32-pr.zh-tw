---
description: 如果沒有任何效能成本，應用程式可能會產生一些有趣的查詢。
ms.assetid: 81e1c5c5-03bc-4598-814e-14e56513e221
title: " (Direct3D 9) 的非同步通知"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8aee8acb791e2e1e2de7eb305cc19df4e7711e2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972772"
---
# <a name="asynchronous-notification-direct3d-9"></a> (Direct3D 9) 的非同步通知

如果沒有任何效能成本，應用程式可能會產生一些有趣的查詢。 在 Direct3D 7 和 Direct3D 8 中，同步查詢機制 GetInfo，適用于統計資料，但未加入任何效能關鍵查詢。 另外還有其他專案 (，像是本質上是非同步) 。 這是一個簡單的 API，可進行同步和非同步查詢。 GetInfo 將在 Direct3D 9 中淘汰。

使用 [**IDirect3DDevice9：： CreateQuery**](/windows/desktop/api)建立查詢。 這個方法會採用 D3DQUERYTYPE，它會定義要進行何種類型的查詢，並將指標傳回至 [**IDirect3DQuery9**](/windows/desktop/api) 物件。 如果查詢類型不受支援，則呼叫會傳回錯誤 D3DERR \_ NOTAVAILABLE。 使用查詢物件時，應用程式會使用 [**IDirect3DQuery9：： Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)將查詢提交至執行時間，並使用 [**IDirect3DQuery9：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)來輪詢查詢狀態。 如果有可用的查詢結果， \_ 則會傳回 s OK，否則會 \_ 傳回 FALSE。 應用程式預期會針對查詢結果傳遞適當大小的緩衝區。

應用程式有一個選項，可讓執行時間使用 D3DGETDATA \_ flush With [**IDirect3DQuery9：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)來強制將查詢排清至驅動程式。 它會造成清除，強制驅動程式查看查詢。 在此情況下， \_ 如果裝置遺失，則會傳回 D3DERR DEVICELOST。

當裝置遺失時，所有查詢都會遺失，應用程式必須重新建立。 如果裝置不支援查詢，且 pQueryID 為 **Null**，則查詢建立將會失敗，並出現 D3DERR \_ INVALIDCALL。

下表摘要說明每個查詢類型的重要資訊。



| QuertyType                    | 有效的問題旗標              | 有其的緩衝區              | 執行階段      | 查詢的隱含開頭 |
|-------------------------------|-------------------------------|-----------------------------|--------------|-----------------------------|
| D3DQUERYTYPE \_ VCACHE          | D3DISSUE \_ 結束                 | D3DDEVINFO \_ VCACHE          | 零售/Debug | CreateDevice                |
| D3DQUERYTYPE \_ ResourceManager | D3DISSUE \_ 結束                 | D3DDEVINFO \_ ResourceManager | 僅限 Debug   | 存在                     |
| D3DQUERYTYPE \_ VERTEXSTATS     | D3DISSUE \_ 結束                 | D3DDEVINFO \_ D3DVERTEXSTATS  | 僅限 Debug   | 存在                     |
| D3DQUERYTYPE \_ 事件           | D3DISSUE \_ 結束                 | BOOL                        | 零售/Debug | CreateDevice                |
| D3DQUERYTYPE \_ 遮蔽       | D3DISSUE \_ BEGIN，D3DISSUE \_ END | DWORD                       | 零售/Debug | N/A                         |



 

[**IDirect3DQuery9：： Issue**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-issue)的旗標欄位：


```
#define D3DISSUE_END (1 << 0) 
// Tells the runtime to issue the end of a query, changing its state to 
//   "non-signaled" 
```




```
 
#define D3DISSUE_BEGIN (1 << 1) // Tells the runtime to issue the 
// beginning of a query. 
```



[**IDirect3DQuery9：：**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)的旗標欄位：


```
 
#define D3DGETDATA_FLUSH (1 << 0) // Tells the runtime to flush 
// if the query is outstanding.
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[程式設計秘訣](programming-tips.md)
</dt> </dl>

 

 
