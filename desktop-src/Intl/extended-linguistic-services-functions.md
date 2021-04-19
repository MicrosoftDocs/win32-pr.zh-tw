---
description: ELS 支援下表中定義的函數。
ms.assetid: d62ab664-a75a-4d06-aefb-a3311ea7d4a7
title: 擴充的語言服務函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5b8acff7601955f8ed6e37f430caa0a52aa880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985196"
---
# <a name="extended-linguistic-services-functions"></a>擴充的語言服務函數

ELS 支援下表中定義的函數。



| 函式                                                 | 描述                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MappingCallbackProc**](/windows/desktop/api/Elscore/nc-elscore-pfn_mappingcallbackproc)       | 應用程式定義的回呼函式，會以非同步方式處理 **MappingRecognizeText** 函數所產生的資料。                 |
| [**MappingDoAction**](/windows/desktop/api/Elscore/nf-elscore-mappingdoaction)               | 導致 ELS 服務在文字辨識發生之後執行動作。                                                                |
| [**MappingFreePropertyBag**](/windows/desktop/api/Elscore/nf-elscore-mappingfreepropertybag) | 釋放在 ELS 文字辨識操作期間配置的記憶體和資源。                                                                 |
| [**MappingFreeServices**](/windows/desktop/api/Elscore/nf-elscore-mappingfreeservices)       | 釋放配置給應用程式的記憶體和資源，以與一或多個 ELS 服務互動。                                            |
| [**MappingGetServices**](/windows/desktop/api/Elscore/nf-elscore-mappinggetservices)         | 根據應用程式指定的準則，取得可用的 ELS 平臺支援服務清單，以及相關聯的資訊。 |
| [**MappingRecognizeText**](/windows/desktop/api/Elscore/nf-elscore-mappingrecognizetext)     | 在 ELS 服務上呼叫以辨識文字。                                                                                                   |



 

 

 



