---
description: CMediaType 類別會管理媒體類型。 此類別繼承 AM \_ 媒體 \_ 類型結構。 它可以轉換成類型為媒體類型的變數 \_ \_ 。
ms.assetid: ea3d03a1-cca4-4a6e-9d1d-4cebe710f913
title: 'CMediaType 類別 (Mtype) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f91578f91840c316347c6266e678357e31c8a284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998792"
---
# <a name="cmediatype-class"></a>CMediaType 類別

![cmediatype 類別階層](images/mtype01.png)

`CMediaType`類別會管理媒體類型。 此類別繼承 [**AM \_ 媒體 \_ 類型**](/windows/win32/api/strmif/ns-strmif-am_media_type) 結構。 它可以轉換成類型為 **\_ 媒體 \_ 類型** 的變數。



| 公用方法                                                      | Description                                                                    |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CMediaType**](cmediatype-cmediatype.md)                         | 函式方法。                                                            |
| [**~ CMediaType**](cmediatype--cmediatype.md)                       | 函式方法。                                                             |
| [**設定**](cmediatype-set.md)                                       | 設定另一種媒體類型的媒體類型。                                   |
| [**IsValid**](cmediatype-isvalid.md)                               | 判斷是否已將主要類型指派給這個物件。              |
| [**類型**](cmediatype-type.md)                                     | 抓取主要型別。                                                      |
| [**>advanced.field.settype**](cmediatype-settype.md)                               | 指定主要類型。                                                      |
| [**Subtype**](cmediatype-subtype.md)                               | 抓取子類型。                                                         |
| [**SetSubtype**](cmediatype-setsubtype.md)                         | 指定子類型。                                                         |
| [**IsFixedSize**](cmediatype-isfixedsize.md)                       | 判斷樣本的大小是否固定或變數大小。                |
| [**IsTemporalCompressed**](cmediatype-istemporalcompressed.md)     | 判斷資料流程是否使用時態性壓縮。                            |
| [**GetSampleSize**](cmediatype-getsamplesize.md)                   | 抓取範例大小。                                                     |
| [**SetSampleSize**](cmediatype-setsamplesize.md)                   | 指定固定樣本大小，或指定樣本具有變數大小。 |
| [**SetVariableSize**](cmediatype-setvariablesize.md)               | 指定範例沒有固定的大小。                               |
| [**SetTemporalCompression**](cmediatype-settemporalcompression.md) | 指定是否使用時態壓縮來壓縮範例。           |
| [**格式**](cmediatype-format.md)                                 | 抓取格式區塊的指標。                                       |
| [**FormatLength**](cmediatype-formatlength.md)                     | 抓取格式區塊的長度。                                      |
| [**SetFormatType**](cmediatype-setformattype.md)                   | 指定格式類型。                                                     |
| [**FormatType**](cmediatype-formattype.md)                         | 抓取格式類型。                                                     |
| [**SetFormat**](cmediatype-setformat.md)                           | 指定格式區塊。                                                    |
| [**ResetFormatBuffer**](cmediatype-resetformatbuffer.md)           | 刪除格式區塊。                                                      |
| [**AllocFormatBuffer**](cmediatype-allocformatbuffer.md)           | 配置格式區塊的記憶體。                                         |
| [**ReallocFormatBuffer**](cmediatype-reallocformatbuffer.md)       | 將格式區塊重新配置為新的大小。                                    |
| [**InitMediaType**](cmediatype-initmediatype.md)                   | 初始化媒體類型。                                                    |
| [**MatchesPartial**](cmediatype-matchespartial.md)                 | 判斷此媒體類型是否符合部分指定的媒體類型。        |
| [**IsPartiallySpecified**](cmediatype-ispartiallyspecified.md)     | 判斷是否已部分定義媒體類型。                             |
| 運算子                                                           | 說明                                                                    |
| [**運算子 =**](cmediatype-operator-.md)                          | 多載指派運算子來複製媒體類型。                        |
| [**operator = =**](cmediatype-operator--.md)                        | 測試 `CMediaType` 物件是否相等。                               |
| [**operator！ =**](cmediatype-operator-neq.md)                      | 測試 `CMediaType` 物件是否不相等。                             |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Mtype (包含： .h) </dt> </dl>                                                                                     |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




