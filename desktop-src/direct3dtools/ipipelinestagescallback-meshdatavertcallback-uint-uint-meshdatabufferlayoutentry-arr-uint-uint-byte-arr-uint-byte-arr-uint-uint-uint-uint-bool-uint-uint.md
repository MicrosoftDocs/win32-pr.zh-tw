---
description: 回呼，會通知主機 assocaited 要求所傳回的管線階段網格資訊。
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback：： MeshDataVertCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510008"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback：： MeshDataVertCallback 方法

回呼，會通知主機 assocaited 要求所傳回的管線階段網格資訊。

## <a name="syntax"></a>語法


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a>參數

*numVertices*   
結果中的頂點數目。

*numBufferLayoutEntries*   
結果中的緩衝區版面設定項目數目。

*count1 \_ 專案*   
緩衝區版面配置 entires。 這些描述著色器輸出簽章。

*大步*   
整個輸出區塊 (stride) 的大小。

*numVBBytes*   
頂點緩衝區的大小（以位元組為單位）。

*count4 \_ pVBData*   
頂點緩衝區。

*numIBBytes*   
索引緩衝區的大小（以位元組為單位）。

*count6 \_ pIBData*   
索引緩衝區。

*indexSize*   
每個索引的大小（以位元組為單位）。

*IBOffset*   
索引緩衝區中的位移，指定要開始使用索引的位置。

*baseVertex*   
頂點緩衝區中的位移，指定應該開始使用頂點的位置。

*minVertex*   

*IBIndexesVB*   
如果使用索引緩衝區，則為 true;否則為 false。

*numIndices*   
使用的索引數目。

*拓撲*   
著色器的 topolology。 這與關聯繪製呼叫的拓撲不一定相同。

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>標頭</p></td><td>Vspixengine。h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>另請參閱

[**IPipeLineStagesCallback**](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
