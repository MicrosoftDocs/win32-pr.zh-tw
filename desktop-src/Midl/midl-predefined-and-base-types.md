---
title: MIDL 預先定義和基底類型
description: MIDL 支援下列基底和預先定義的類型。
ms.assetid: 72da24b6-253d-4032-ba0c-58b2542701fc
keywords:
- MIDL、預先定義和基底的資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6ecbc76b3f680f0fffbabcff38e8562475e26be8ae4ac583a78c614d1651151
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067078"
---
# <a name="midl-predefined-and-base-types"></a>MIDL 預先定義和基底類型

MIDL 支援下列基底和預先定義的類型。



| 資料類型                                  | 描述                                                                                                                                                                                             | 預設簽署     |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|
| [**布林**](boolean.md)                 | 8位。 與 [**oleautomation**](oleautomation.md) 介面不相容;請改用 VARIANT \_ BOOL。                                                                                               | 不帶正負號         |
| [**位元組**](byte.md)                       | 8位。                                                                                                                                                                                                 | (不適用) |
| [**char**](char-idl.md)                   | 8位。                                                                                                                                                                                                 | 不帶正負號         |
| [**雙**](double.md)                   | 64位浮點數。                                                                                                                                                                           | (不適用) |
| [**錯誤 \_ 狀態 \_ t**](error-status-t.md) | 32位不帶正負號整數，用於傳回錯誤處理的狀態值。                                                                                                                                 | 不帶正負號         |
| [**浮動**](float.md)                     | 32位浮點數。                                                                                                                                                                           | (不適用) |
| [**處理 \_ t**](handle-t.md)              | 系結的基本控制碼類型。                                                                                                                                                                      | (不適用) |
| [**Hyper**](hyper.md)                     | 64位整數。                                                                                                                                                                                         | 簽署人           |
| [**int**](int.md)                         | 32位整數。 在16位平臺上，不能出現在沒有大小限定詞的遠端函式中，例如 [**short**](short.md)、 [**small**](small.md)、 [**long**](long.md) 或 [**hyper-v**](hyper.md)。 | 簽署人           |
| **\_\_int8**                               | 8位整數。 相當於 **small**。                                                                                                                                                                 | 簽署人           |
| **\_\_int16**                              | 16位整數。 相當於 **short**。                                                                                                                                                                | 簽署人           |
| **\_\_時會**                              | 32位整數。 相當於 [**long**](long.md)。                                                                                                                                                     | 簽署人           |
| [**\_\_int3264**](--int3264.md)           | 32位平臺上的32位整數，在64位平臺上為64位。                                                                                                                       | 簽署人           |
| [**\_\_int64**](--int64.md)               | 64位整數。 相當於 [**超級**](hyper.md)。                                                                                                                                                   | 簽署人           |
| [**long**](long.md)                       | 32位整數。                                                                                                                                                                                         | 簽署人           |
| [**short**](short.md)                     | 16-bt 整數。                                                                                                                                                                                          | 簽署人           |
| [**小**](small.md)                     | 8位整數。                                                                                                                                                                                          | 簽署人           |
| [**void**](void.md)                       | 指出程式不會傳回值。                                                                                                                                                   | (不適用) |
| **無效 \***                                | 僅限內容控制碼的32位指標。                                                                                                                                                                | (不適用) |
| [**wchar \_ t**](wchar-t.md)                | 16位的寬字元預先定義型別。                                                                                                                                                             | 不帶正負號         |



 

 

 




