---
description: 如果您的網路提供者需要支援流覽其網路資源，它應該會執行下列功能。 MPR 會呼叫這些函式來列舉資源。
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: 列舉函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f119256c4976e393795b45caf2fab9e7cec5353fed54718ef0be8db994ef2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008236"
---
# <a name="enumeration-functions"></a>列舉函數

如果您的網路提供者需要支援流覽其網路資源，它應該會執行下列功能。 MPR 會呼叫這些函式來列舉資源。

不需要網路提供者來執行任何列舉函數。 但是，如果網路提供者執行的是 [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)、 [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)或 [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)，則也必須執行其他兩個列舉函數。



| 函式                                                     | 描述                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | 開啟網路資源或現有連接的列舉。                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | 在 [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)所傳回的控制碼上執行列舉。                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | 關閉列舉。                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | 判斷提供者是否為回應指定網路資源之要求的正確提供者，並傳回資源類型的相關資訊。 |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | 傳回流覽階層中指定之網路資源的父系。                                                                                         |



 

 

 



