---
description: IAMTimeline 介面提供操作時間軸的方法，也就是 Microsoft DirectShow 編輯服務 (DES) 中的中央物件。
ms.assetid: 6750efa0-946c-4ad3-b0df-de55872b94c3
title: 'IAMTimeline 介面 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: fc4374a198232625b87448004b667ccd8ce0183b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995046"
---
# <a name="iamtimeline-interface"></a>IAMTimeline 介面

> [!Note]  
> \[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

 

`IAMTimeline`介面提供操作時間軸的方法，也就是 Microsoft [DirectShow 編輯服務](directshow-editing-services.md) (DES) 中的中央物件。 時間軸是經過時間排序的元素集合，例如影片剪輯、音訊剪輯、效果和剪輯之間的轉換。 轉譯引擎會使用時間軸來建立篩選圖形，應用程式可從中產生轉譯的輸出。

`IAMTimeline` 執行三項基本服務。 其

-   在時間軸中建立物件。
-   作為這些物件的容器。
-   設定和抓取時間軸的一般參數。

若要建立時程表物件，請使用類別識別碼 CLSID AMTimeline 來呼叫 **CoCreateInstance** \_ 。

## <a name="members"></a>成員

**IAMTimeline** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMTimeline** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMTimeline** 介面具有這些方法。



| 方法                                                             | 描述                                                                                                                       |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**AddGroup**](iamtimeline-addgroup.md)                           | 將群組加入至時間軸。<br/>                                                                                          |
| [**ClearAllGroups**](iamtimeline-clearallgroups.md)               | 從時間軸移除所有群組，以及這些群組中包含的所有物件。<br/>                                |
| [**CreateEmptyNode**](iamtimeline-createemptynode.md)             | 建立新的時間軸物件。<br/>                                                                                         |
| [**EffectsEnabled**](iamtimeline-effectsenabled.md)               | 判斷是否已啟用效果。<br/>                                                                                |
| [**EnableEffects**](iamtimeline-enableeffects.md)                 | 啟用或停用時間軸中的所有效果。<br/>                                                                       |
| [**EnableTransitions**](iamtimeline-enabletransitions.md)         | 啟用或停用時間軸中的所有轉換。<br/>                                                                   |
| [**GetCountOfType**](iamtimeline-getcountoftype.md)               | 抓取指定的群組及其所有子系中所包含之指定類型的物件數目。<br/> |
| [**GetDefaultEffect**](iamtimeline-getdefaulteffect.md)           | 捕獲預設效果。<br/>                                                                                          |
| [**GetDefaultEffectB**](iamtimeline-getdefaulteffectb.md)         | 以 **BSTR** 值形式抓取預設效果。<br/>                                                                      |
| [**GetDefaultFPS**](iamtimeline-getdefaultfps.md)                 | 抓取預設輸出畫面播放速率（以每秒畫面格速率為單位）。<br/>                                                         |
| [**GetDefaultTransition**](iamtimeline-getdefaulttransition.md)   | 捕獲預設轉換。<br/>                                                                                      |
| [**GetDefaultTransitionB**](iamtimeline-getdefaulttransitionb.md) | 以 **BSTR** 值形式抓取預設轉換。<br/>                                                                  |
| [**GetDirtyRange**](iamtimeline-getdirtyrange.md)                 | 不支援。<br/>                                                                                                         |
| [**GetDuration**](iamtimeline-getduration.md)                     | 抓取時間軸的持續時間。<br/>                                                                                       |
| [**GetDuration2**](iamtimeline-getduration2.md)                   | 以 **雙精度浮點數** 的形式抓取時間軸持續時間。<br/>                                                                       |
| [**GetGroup**](iamtimeline-getgroup.md)                           | 抓取指定的群組。<br/>                                                                                           |
| [**GetGroupCount**](iamtimeline-getgroupcount.md)                 | 抓取時間軸中包含的群組數目。<br/>                                                     |
| [**GetInsertMode**](iamtimeline-getinsertmode.md)                 | 不支援。<br/>                                                                                                         |
| [**IsDirty**](iamtimeline-isdirty.md)                             | 不支援。<br/>                                                                                                         |
| [**RemGroupFromList**](iamtimeline-remgroupfromlist.md)           | 不支援。<br/>                                                                                                         |
| [**SetDefaultEffect**](iamtimeline-setdefaulteffect.md)           | 設定預設效果。<br/>                                                                                               |
| [**SetDefaultEffectB**](iamtimeline-setdefaulteffectb.md)         | 將預設效果設定為 **BSTR** 值。<br/>                                                                           |
| [**SetDefaultFPS**](iamtimeline-setdefaultfps.md)                 | 設定預設輸出畫面播放速率（以每秒畫面格速率為單位）。<br/>                                                              |
| [**SetDefaultTransition**](iamtimeline-setdefaulttransition.md)   | 設定預設轉換。<br/>                                                                                           |
| [**SetDefaultTransitionB**](iamtimeline-setdefaulttransitionb.md) | 將預設轉換設定為 BSTR 值。<br/>                                                                           |
| [**SetInsertMode**](iamtimeline-setinsertmode.md)                 | 未實作。<br/>                                                                                                       |
| [**SetInterestRange**](iamtimeline-setinterestrange.md)           | 未實作。<br/>                                                                                                       |
| [**TransitionsEnabled**](iamtimeline-transitionsenabled.md)       | 決定是否啟用轉換。<br/>                                                                            |
| [**ValidateSourceNames**](iamtimeline-validatesourcenames.md)     | 驗證時間軸中的來源名稱。<br/>                                                                                |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭檔 Qedit 與版本7以後的 Direct3D 標頭不相容。

 

> [!Note]  
> 若要取得 Qedit，請下載 [適用于 Windows Vista 和 .NET Framework 3.0 的 Microsoft Windows SDK 更新](https://msdn.microsoft.com/windowsvista/bb980924.aspx)。 在 Windows 7 和 .NET Framework 3.5 Service Pack 1 的 Microsoft Windows SDK 中無法使用 Qedit。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Qedit。h</dt> </dl>      |
| 程式庫<br/> | <dl> <dt>Strmiids .lib</dt> </dl> |



 

 
