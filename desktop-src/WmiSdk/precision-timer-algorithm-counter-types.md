---
description: 精確度計時器演算法計數器類型會取得比系統計時器更精確的讀數。
ms.assetid: f7159645-6287-47a3-895e-20dae6e0892a
ms.tgt_platform: multiple
title: 精確度計時器演算法計數器類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137d136db0b4dd579dfec4673b09ce216bef4042d9356b3938b79e7817e3d83a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131030"
---
# <a name="precision-timer-algorithm-counter-types"></a>精確度計時器演算法計數器類型

精確度計時器演算法計數器類型會取得比系統計時器更精確的讀數。 提供資料的服務也會提供時間戳記，以消除由於從效能 DLL 捕獲系統時間戳記和收集資料所經過的小和變動時間，而造成的錯誤。 精確度計時器的這個基底時間戳記是效能 \_ 精確度 \_ 時間戳記屬性，必須緊接在效能 \_ 精確度 \_ 計時器屬性之後。



| CounterType 常數                                                                                         | 描述                                                                                                                  |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [效能 \_PRECISION \_ SYSTEM \_ 計時器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))Decimal 541525248<br/> | 類似于性能 \_ 計數器 \_ 計時器，不同之處在于它會使用計數器定義的時間基底，而不是系統時間戳記。             |
| [效能 \_有效位數 \_ 100ns \_ 計時器](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10))十進位542573824<br/>  | 類似于效能 \_ 100NSEC \_ 計時器，不同之處在于它會使用100ns 個計數器定義的時間基底，而不是系統100ns 時間戳記。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[WMI 效能計數器類型](wmi-performance-counter-types.md)
</dt> </dl>

 

