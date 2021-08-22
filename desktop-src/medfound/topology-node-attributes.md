---
description: 拓撲節點屬性
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: 拓撲節點屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd366c03607c4fc6646a09dae8571e6e4847a45b985f4996d28c15a828937
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034666"
---
# <a name="topology-node-attributes"></a>拓撲節點屬性

下列屬性適用于拓撲節點。

## <a name="general-topology-node-attributes"></a>一般拓撲節點屬性



| 屬性                                                                       | 描述                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ CONNECT \_ 方法**](mf-toponode-connect-method-attribute.md)   | 指定拓撲載入器如何連接此拓撲節點，以及此節點是否為選擇性節點。                                                        |
| [**MF \_ TOPONODE \_ 解碼器**](mf-toponode-decoder-attribute.md)                  | 指定拓撲節點的物件是否為解碼器。                                                                                                  |
| [**MF \_ TOPONODE \_ 解密器**](mf-toponode-decryptor-attribute.md)              | 指定拓撲節點的基礎物件是否為解密程式。                                                                                     |
| [**MF \_ TOPONODE \_ DISCARDABLE**](mf-toponode-discardable-attribute.md)          | 指定管線是否可以從拓撲節點卸載範例。                                                                                    |
| [**MF \_ TOPONODE \_ 錯誤 \_ MAJORTYPE**](mf-toponode-error-majortype-attribute.md) | 包含拓撲節點的主要媒體類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。 |
| [**MF \_ TOPONODE \_ 錯誤 \_ 子類型**](mf-toponode-error-subtype-attribute.md)     | 包含拓撲節點的媒體子類型。 因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。    |
| [**MF \_ TOPONODE \_ ERRORCODE**](mf-toponode-errorcode-attribute.md)              | 包含此拓撲節點最近連接失敗的錯誤碼。                                                                  |
| [**已 \_ 鎖定 MF TOPONODE \_**](mf-toponode-locked-attribute.md)                    | 指定是否可在此拓撲節點上變更媒體類型。                                                                                  |
| [**MF \_ TOPONODE \_ MARKIN \_ 這裡**](mf-toponode-markin-here-attribute.md)         | 指定管線是否在此節點套用標記。                                                                                             |
| [**MF \_ TOPONODE \_ MARKOUT \_ 這裡**](mf-toponode-markout-here-attribute.md)       | 指定管線是否在此節點套用標記。                                                                                            |



 

## <a name="source-node-attributes"></a>來源節點屬性



| 屬性                                                                                       | 描述                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ MEDIASTART**](mf-toponode-mediastart-attribute.md)                            | 指定簡報的開始時間（相對於啟動媒體來源檔案），以 100-毫微秒單位表示。 |
| [**MF \_ TOPONODE \_ MEDIASTOP**](mf-toponode-mediastop-attribute.md)                              | 指定簡報的停止時間，相對於啟動媒體來源檔案，以 100-毫微秒單位表示。  |
| [**MF \_ TOPONODE \_ 展示 \_ 描述項**](mf-toponode-presentation-descriptor-attribute.md) | 包含媒體來源之展示描述項的指標。                                           |
| [**MF \_ TOPONODE \_ 序列 \_ ELEMENTID**](mf-toponode-sequence-elementid-attribute.md)           | 指定包含來源節點的元素。                                                                |
| [**MF \_ TOPONODE \_ 來源**](mf-toponode-source-attribute.md)                                    | 包含與拓撲節點相關聯之媒體來源的指標。                                           |
| [**MF \_ TOPONODE \_ 串流 \_ 描述項**](mf-toponode-stream-descriptor-attribute.md)             | 包含媒體來源的資料流程描述元指標。                                                 |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**](mf-toponode-workqueue-id-attribute.md)                       | 指定拓撲節點的工作佇列。                                                                       |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md)    | 指定 MMCSS 拓撲節點的多媒體類別排程器服務 () 工作。                                  |
| [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | 指定拓撲節點的 MMCSS 工作識別碼。                                                            |



 

## <a name="transform-node-attributes"></a>轉換節點屬性



| 屬性                                                                             | 描述                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ D3DAWARE**](mf-toponode-d3daware-attribute.md)                      | 指定與拓撲節點相關聯的轉換是否支援 (DXVA 的 DirectX Video 加速)  |
| [**MF \_ TOPONODE \_ 清空**](mf-toponode-drain-attribute.md)                            | 指定何時清空轉換。                                                                     |
| [**MF \_ TOPONODE \_ FLUSH**](mf-toponode-flush-attribute.md)                            | 指定何時清除轉換。                                                                     |
| [**MF \_ TOPONODE \_ 轉換 \_ OBJECTID**](mf-toponode-transform-objectid-attribute.md) | 類別識別碼 (與此拓撲節點相關聯之轉換的 CLSID) 。                          |



 

## <a name="output-node-attributes"></a>輸出節點屬性



| 屬性                                                                                  | 描述                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**MF \_ TOPONODE \_ 停用預先進行 \_**](mf-toponode-disable-preroll-attribute.md)            | 指定媒體會話是否在此拓撲節點所代表的媒體接收器上使用預先進行。            |
| [**\_ \_ \_ 移除時的 MF TOPONODE NOSHUTDOWN \_**](mf-toponode-noshutdown-on-remove-attribute.md) | 指定當輸出節點從拓撲中移除時，媒體會話是否會關閉媒體接收器。 |
| [**MF \_ TOPONODE \_ RATELESS**](mf-toponode-rateless-attribute.md)                           | 指定與此拓撲節點相關聯的媒體接收器是否 rateless。                                 |
| [**MF \_ TOPONODE \_ STREAMID**](mf-toponode-streamid-attribute.md)                           | 與此拓撲節點相關聯之資料流程接收的資料流程識別碼。                                     |



 

## <a name="tee-node-attributes"></a>T 節點屬性



| 屬性                                                                  | 描述                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [**MF \_ TOPONODE \_ PRIMARYOUTPUT**](mf-toponode-primaryoutput-attribute.md) | 指出哪些輸出是 t 節點上的主要輸出。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 



