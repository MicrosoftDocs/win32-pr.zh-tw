---
description: 這個介面是用來控制動畫功能，連接動畫集與正在進行動畫的轉換框架。
ms.assetid: a485e4d2-82e1-45db-8496-dd743904c34d
title: 'ID3DXAnimationController 介面 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9ed587be50ba41d4544152985285b20ab63bd745
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982889"
---
# <a name="id3dxanimationcontroller-interface"></a>ID3DXAnimationController 介面

這個介面是用來控制動畫功能，連接動畫集與正在進行動畫的轉換框架。 介面具有混合多個動畫的方法，並可在一段時間內修改混合參數，以啟用平滑轉換和其他效果。

## <a name="members"></a>成員

**ID3DXAnimationController** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **ID3DXAnimationController** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ID3DXAnimationController** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                                             |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvanceTime**](id3dxanimationcontroller--advancetime.md)                             | 將網格繪製到動畫，並以指定的數量前進全域動畫時間。<br/>                                                              |
| [**CloneAnimationController**](id3dxanimationcontroller--cloneanimationcontroller.md)   | 複製或複製動畫控制器。<br/>                                                                                                  |
| [**GetAnimationSet**](id3dxanimationcontroller--getanimationset.md)                     | 取得動畫集。<br/>                                                                                                                       |
| [**GetAnimationSetByName**](id3dxanimationcontroller--getanimationsetbyname.md)         | 取得動畫集合，並指定其名稱。<br/>                                                                                                       |
| [**GetCurrentPriorityBlend**](id3dxanimationcontroller--getcurrentpriorityblend.md)     | 傳回目前正在執行之優先順序 blend 事件的事件控制碼。<br/>                                                                 |
| [**GetCurrentTrackEvent**](id3dxanimationcontroller--getcurrenttrackevent.md)           | 傳回目前在指定動畫播放軌上執行的事件的事件控制碼。<br/>                                                     |
| [**GetEventDesc**](id3dxanimationcontroller--geteventdesc.md)                           | 取得指定動畫事件的描述。<br/>                                                                                           |
| [**GetMaxNumAnimationOutputs**](id3dxanimationcontroller--getmaxnumanimationoutputs.md) | 取得動畫控制器可支援的動畫輸出數目上限。<br/>                                                            |
| [**GetMaxNumAnimationSets**](id3dxanimationcontroller--getmaxnumanimationsets.md)       | 取得動畫控制器可支援的動畫集合數目上限。<br/>                                                              |
| [**GetMaxNumEvents**](id3dxanimationcontroller--getmaxnumevents.md)                     | 取得動畫控制器可支援的事件數目上限。<br/>                                                                      |
| [**GetMaxNumTracks**](id3dxanimationcontroller--getmaxnumtracks.md)                     | 取得動畫控制器中的曲目數目上限。<br/>                                                                               |
| [**GetNumAnimationSets**](id3dxanimationcontroller--getnumanimationsets.md)             | 傳回目前在動畫控制器中註冊的動畫集合數目。<br/>                                                       |
| [**GetPriorityBlend**](id3dxanimationcontroller--getpriorityblend.md)                   | 取得動畫控制器所使用的目前優先權混合權數。<br/>                                                                  |
| [**GetTime**](id3dxanimationcontroller--gettime.md)                                     | 取得全域動畫時間。<br/>                                                                                                              |
| [**GetTrackAnimationSet**](id3dxanimationcontroller--gettrackanimationset.md)           | 取得指定之播放軌的動畫集。<br/>                                                                                                  |
| [**GetTrackDesc**](id3dxanimationcontroller--gettrackdesc.md)                           | 取得追蹤描述。<br/>                                                                                                                  |
| [**GetUpcomingPriorityBlend**](id3dxanimationcontroller--getupcomingpriorityblend.md)   | 傳回已排定在指定事件之後發生之下一個優先權 blend 事件的事件控制碼。<br/>                                         |
| [**GetUpcomingTrackEvent**](id3dxanimationcontroller--getupcomingtrackevent.md)         | 傳回在動畫播放軌上指定的事件之後，排定要發生之下一個事件的事件控制碼。<br/>                                  |
| [**KeyPriorityBlend**](id3dxanimationcontroller--keypriorityblend.md)                   | 設定指定動畫播放軌的混合事件索引鍵。<br/>                                                                                  |
| [**KeyTrackEnable**](id3dxanimationcontroller--keytrackenable.md)                       | 設定可啟用或停用動畫播放軌的事件索引鍵。<br/>                                                                               |
| [**KeyTrackPosition**](id3dxanimationcontroller--keytrackposition.md)                   | 設定事件索引鍵，以變更動畫播放軌的當地時間。<br/>                                                                         |
| [**KeyTrackSpeed**](id3dxanimationcontroller--keytrackspeed.md)                         | 設定可變更動畫播放軌播放速率的事件索引鍵。<br/>                                                                       |
| [**KeyTrackWeight**](id3dxanimationcontroller--keytrackweight.md)                       | 設定可變更動畫播放軌權數的事件索引鍵。將多個追蹤結合在一起時，權數會用來做為乘數。<br/> |
| [**RegisterAnimationOutput**](id3dxanimationcontroller--registeranimationoutput.md)     | 將動畫輸出新增至動畫控制器，並註冊用於調整、旋轉和轉譯 (SRT) 轉換的指標。<br/>          |
| [**RegisterAnimationSet**](id3dxanimationcontroller--registeranimationset.md)           | 將動畫集加入至動畫控制器。<br/>                                                                                           |
| [**ResetTime**](id3dxanimationcontroller--resettime.md)                                 | 將全域動畫的時間重設為零。 任何暫止的事件將會保留其原始排程，但在新的時間範圍內。<br/>                 |
| [**SetPriorityBlend**](id3dxanimationcontroller--setpriorityblend.md)                   | 設定動畫控制器所使用的優先順序混合權數。<br/>                                                                          |
| [**SetTrackAnimationSet**](id3dxanimationcontroller--settrackanimationset.md)           | 將動畫集套用至指定的曲目。<br/>                                                                                            |
| [**SetTrackDesc**](id3dxanimationcontroller--settrackdesc.md)                           | 設定追蹤描述。<br/>                                                                                                                  |
| [**SetTrackEnable**](id3dxanimationcontroller--settrackenable.md)                       | 啟用或停用動畫控制器中的軌跡。<br/>                                                                                     |
| [**SetTrackPosition**](id3dxanimationcontroller--settrackposition.md)                   | 將軌跡設定為指定的本機動畫時間。<br/>                                                                                        |
| [**SetTrackPriority**](id3dxanimationcontroller--settrackpriority.md)                   | 設定指定動畫播放軌的優先順序混合加權。<br/>                                                                         |
| [**SetTrackSpeed**](id3dxanimationcontroller--settrackspeed.md)                         | 設定追蹤速度。 追蹤速度類似于用來加速播放播放軌或減緩播放速度的乘數。<br/>            |
| [**SetTrackWeight**](id3dxanimationcontroller--settrackweight.md)                       | 設定軌跡加權。 權數用來決定如何將多個追蹤混合在一起。<br/>                                                |
| [**UnkeyAllPriorityBlends**](id3dxanimationcontroller--unkeyallpriorityblends.md)       | 從動畫控制器中移除所有排程的優先順序 blend 事件。<br/>                                                                   |
| [**UnkeyAllTrackEvents**](id3dxanimationcontroller--unkeyalltrackevents.md)             | 從指定的動畫播放軌移除所有事件。<br/>                                                                                         |
| [**UnkeyEvent**](id3dxanimationcontroller--unkeyevent.md)                               | 從動畫播放軌移除指定的事件，以防止事件的執行。<br/>                                                    |
| [**UnregisterAnimationSet**](id3dxanimationcontroller--unregisteranimationset.md)       | 從動畫控制器移除動畫集。<br/>                                                                                      |
| [**ValidateEvent**](id3dxanimationcontroller--validateevent.md)                         | 檢查指定的事件控制碼是否有效，以及動畫事件是否尚未完成。<br/>                                              |



 

## <a name="remarks"></a>備註

使用 [**D3DXCreateAnimationController**](d3dxcreateanimationcontroller.md)建立動畫控制器物件。

LPD3DXANIMATIONCONTROLLER 型別定義為 **ID3DXAnimationController** 介面的指標。


```
typedef interface ID3DXAnimationController ID3DXAnimationController;
typedef interface ID3DXAnimationController *LPD3DXANIMATIONCONTROLLER;
```



D3DXEVENTHANDLE 型別定義為動畫控制器事件的事件控制碼。


```
typedef DWORD D3DXEVENTHANDLE;
```



LPD3DXEVENTHANDLE 型別定義為動畫控制器事件的事件控制碼指標。


```
typedef D3DXEVENTHANDLE *LPD3DXEVENTHANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D3dx9anim。h</dt> </dl> |
| 程式庫<br/> | <dl> <dt>D3dx9 .lib</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[D3DX 介面](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
