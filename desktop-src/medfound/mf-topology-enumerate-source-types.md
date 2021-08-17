---
description: 指定拓撲載入器是否列舉媒體來源所提供的媒體類型。
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: 'MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc9ff7cf9e1497f0d15f68e68c254483f0c9f074e2ce4204e9d77d84aee4ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691294"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性

指定拓撲載入器是否列舉媒體來源所提供的媒體類型。

## <a name="data-type"></a>資料類型

**UINT32**

使用下列其中一個值。



| 值                                                                                                                                    | 意義                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | 請勿列舉來源媒體類型。<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | 列舉來源媒體類型。<br/>        |



 

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>備註

媒體來源上的每個串流都可以提供一種以上的媒體類型。 類型清單是透過資料流程描述項上的 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面來列舉。

拓撲載入器嘗試媒體來源媒體類型的順序是由兩個屬性所控制：

-   MF \_ 拓撲 \_ 列舉 \_ 拓撲上的來源 \_ 類型屬性。
-   來源節點上的 [**MF \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) 屬性。

如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性為 **FALSE** 或未設定，拓撲載入器會使用資料流程目前的媒體類型。 它不會列舉可能類型的清單。 如果目前的媒體類型與下游拓撲節點不相容，而且找不到任何的解碼器/轉換器組合，拓撲解析就會失敗。

如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性為 **TRUE**，拓撲載入器會列舉來源的媒體類型，直到找到相容的類型。 在此情況下，作業的確切順序取決於來源節點上的 [**mf \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) 屬性是否包含 **mf \_ connect \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標。

如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型為 **TRUE** ，且已設定 **mf \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標，拓撲載入器會在移至下一個媒體類型之前耗盡每個媒體類型，如下所示：

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型為 **TRUE** ，但未設定 **mf \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** ，拓撲載入器會嘗試與每個媒體類型的直接連線，然後使用轉換器來嘗試每個媒體類型，最後嘗試每個媒體類型使用以下的解碼器：

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型為 **FALSE**，則會忽略 **mf \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標。

基於 \_ \_ \_ \_ 與現有應用程式的相容性，MF 拓撲列舉來源類型的預設值為 **FALSE**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

### <a name="example"></a>範例

以下是說明 **MF \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標的範例。 假設拓撲的 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性設為 **TRUE**。

媒體來源提供下列類型：

-   T1、T2、T3

媒體接收接受下列類型：

-   T3，T4

案例1：已設定 **MF \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標。

1.  拓撲載入器會嘗試與 T1 的直接連接。 接收會拒絕 T1。
2.  拓撲載入器會插入接受 T1 和輸出 T4 的解碼器。 接收會接受 T4。
3.  最終拓撲包含：媒體來源→解碼器→媒體接收器。

案例2：未設定旗標。

1.  拓撲載入器會嘗試與 T1 的直接連接。 接收會拒絕 T1。
2.  拓撲載入器會嘗試與 T2 的直接連接。 接收會拒絕 T2。
3.  拓撲載入器會嘗試與 T3 的直接連接。 接收會接受 T3。
4.  最終拓撲包含：媒體來源→媒體接收器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[拓撲屬性](topology-attributes.md)
</dt> </dl>

 

 




