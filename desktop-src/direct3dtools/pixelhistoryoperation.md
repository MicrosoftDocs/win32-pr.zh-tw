---
description: 代表圖元歷程記錄的相關資訊。
MS-HAID: vspixengine.PixelHistoryOperation
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: PixelHistoryOperation 結構
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59DC72FC-3865-48D3-9F92-9BE93DCA093B
api_name:
- PixelHistoryOperation
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c02a6725f588aaa4c7d72c48d03d921503d4e6a6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973136"
---
# <a name="span-idvspixenginepixelhistoryoperationspanpixelhistoryoperation-structure"></a><span id="vspixengine.pixelhistoryoperation"></span>PixelHistoryOperation 結構

代表圖元歷程記錄的相關資訊。

## <a name="syntax"></a>語法


```C++
} PixelHistoryOperation;
```

## <a name="members"></a>成員

**開齋節**  
與這項作業相關聯之圖形事件的識別碼。

**五 氯 酚**  
與此作業相關聯的已壓縮呼叫。

**renderTargetPtr**  
原本與此作業) 的已捕捉應用程式內 (的呈現目標。

**iPrim**  
與 jumpbox 他的作業相關聯的實際基本類型索引。

**numPrims**  
與這項作業相關聯之基本專案的總數。

**numVertsPerPrim**  
每個基本的頂點數目。

**iInstance**  
轉譯實例時，與這項作業相關聯之實際實例的實例編號。

**iInstanceCount**  
轉譯實例時，與這項作業相關聯的實例總數。

**bAssemblerStageGeneratesInstanceID**  
如果輸入組合語言產生實例識別碼，則為 true;否則為 false。

**flags**  
PIXELHISTORYFLAGS 值的組合。 如需詳細資訊，請參閱 PIXELHISTORYFLAGS 列舉。

**pVSFile**  
圖元著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

**pGSFile**  
幾何著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

**pPSFile**  
圖元著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

**pHSFile**  
輪廓著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

**pDSFile**  
網域著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

**pCSFile**  
計算著色器位元組資料流程的 FILEPTR。 這會傳回，以便進行 debug。

**VertexShaderFile**  
COM 字串，其中包含頂點著色器原始程式檔的 filepath。

**PixelShaderFile**  
COM 字串，其中包含圖元著色器原始程式檔的 filepath。

**GeometryShaderFile**  
COM 字串，其中包含幾何著色器原始程式檔的 filepath。

**HullShaderFile**  
COM 字串，其中包含輪廓著色器原始程式檔的 filepath。

**DomainShaderFile**  
COM 字串，其中包含網域著色器原始程式檔的 filepath。

**psRed**  
圖元著色器輸出：紅色色彩元件的值。

**psGreen**  
圖元著色器輸出：綠色色彩元件的值。

**psBlue**  
圖元著色器輸出：藍色色彩元件的值

**psAlpha**  
圖元著色器輸出： Alpha 色彩元件的值

**LabelPSRed**  
COM 字串，其中包含與圖元著色器輸出的紅色色彩元件相關聯的標籤名稱。

**LabelPSGreen**  
COM 字串，其中包含與圖元著色器輸出的綠色色彩元件相關聯的標籤名稱。

**LabelPSBlue**  
COM 字串，其中包含與圖元著色器輸出的藍色色彩元件相關聯的標籤名稱。

**LabelPSAlpha**  
COM 字串，其中包含與圖元著色器輸出的 Alpha 色彩元件相關聯的標籤名稱。

**pixelKillReason**  
圖元著色器輸出：已終止圖元輸出的原因。

**pixelOccluded**  
如果圖元是 pixels occluded，則為 true;否則為 false。

**fbRed**  
畫面格緩衝區：合併圖元著色器輸出之前，畫面格緩衝區的紅色色彩元件的值。

**fbGreen**  
畫面格緩衝區：合併圖元著色器輸出之前，畫面格緩衝區的綠色色彩元件的值。

**fbBlue**  
畫面格緩衝區：合併圖元著色器輸出之前的畫面格緩衝區藍色色彩元件值。

**fbAlpha**  
畫面格緩衝區：合併圖元著色器輸出之前，畫面格緩衝區 Alpha 色彩元件的值。

**LabelFBRed**  
COM 字串，其中包含與畫面格緩衝區的紅色色彩元件相關聯的標籤名稱。

**LabelFBGreen**  
COM 字串，其中包含與畫面格緩衝區的綠色色彩元件相關聯的標籤名稱。

**LabelFBBlue**  
COM 字串，其中包含與畫面格緩衝區的藍色色彩元件相關聯的標籤名稱。

**LabelFBAlpha**  
COM 字串，其中包含與畫面格緩衝區的 Alpha 色彩元件相關聯的標籤名稱。

**拓撲**  
繪製呼叫的頂點拓撲 (三角形清單、三角形區域等) 。

**頂點**  
COM 字串，包含從這個基本物件開始的頂點緩衝區。 頂點緩衝區會遵循管線階段中指定的輸入配置格式。

**vertexSize**  
單一頂點的大小（以位元組為單位）。

**InputLayout**  
COM 字串，其中包含與繪製呼叫相關聯的 InputLayoutStruct 結構序列。

**HResult**  
DirectX Hresult。 發生問題時，這可以用來顯示錯誤。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

 

 



