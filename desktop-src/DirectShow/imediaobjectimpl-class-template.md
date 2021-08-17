---
description: IMediaObjectImpl 類別範本提供 IMediaObject 介面的基底實作為基底。 如需使用此範本的詳細資訊，請參閱使用 DMO 類別範本。
ms.assetid: 81d45b8d-8373-4e42-b768-f6126feb935d
title: 'IMediaObjectImpl 類別範本 (Dmoimpl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71b166836ff4da6100f61fca5d3a0c2887462b37adcbdd2ec61abeb919553a59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015576"
---
# <a name="imediaobjectimpl-class-template"></a>IMediaObjectImpl 類別範本

`IMediaObjectImpl`類別樣板提供 [**IMediaObject**](/previous-versions/windows/desktop/api/Mediaobj/nn-mediaobj-imediaobject)介面的基底實作為基底。 如需使用此範本的詳細資訊，請參閱[使用 DMO 類別範本](using-the-dmo-class-template.md)。

此 `IMediaObjectImpl` 範本會公開下列成員。



| Nested 類別                              | 描述                                  |
|-------------------------------------------|----------------------------------------------|
| [**LockIt**](imediaobjectimpl-lockit.md) | 鎖定和解除鎖定 DMO 的 Helper 類別。 |



 



| 方法                                                                      | 描述                                                          |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**CheckTypesSet**](/previous-versions/ms807621(v=msdn.10))                     | 判斷所有非選用的資料流程是否都有媒體類型。 |
| [**InputType**](/previous-versions/ms807633(v=msdn.10))                             | 抓取指定輸入資料流程目前的媒體類型。       |
| [**InputTypeSet**](/previous-versions/ms807638(v=msdn.10))                       | 查詢是否在輸入資料流程上設定媒體類型。           |
| [**InternalAcceptingInput**](/previous-versions/ms809095(v=msdn.10))   | 查詢輸入資料流程是否可以接受更多輸入。               |
| [**InternalCheckInputType**](/previous-versions/ms809096(v=msdn.10))   | 查詢輸入資料流程是否可以接受指定的媒體類型。       |
| [**InternalCheckOutputType**](/previous-versions/ms809098(v=msdn.10)) | 查詢輸出資料流程是否可以接受指定的媒體類型。      |
| [**鎖定**](/previous-versions/ms809100(v=msdn.10))                                       | 鎖定 DMO                                                        |
| [**OutputType**](/previous-versions/ms807644(v=msdn.10))                           | 抓取指定輸出資料流程目前的媒體類型。      |
| [**OutputTypeSet**](/previous-versions/ms807649(v=msdn.10))                     | 查詢是否在輸出資料流程上設定媒體類型。          |
| [**Unlock**](/previous-versions/ms809101(v=msdn.10))                                   | 解除鎖定 DMO                                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Dmoimpl。h</dt> </dl>                                                                     |
| 程式庫<br/> | <dl> <dt>Dmoguids .lib;</dt><dt>Msdmo .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DMO參考](dmo-reference.md)
</dt> <dt>

[使用 DMO 類別範本](using-the-dmo-class-template.md)
</dt> </dl>

 

 
