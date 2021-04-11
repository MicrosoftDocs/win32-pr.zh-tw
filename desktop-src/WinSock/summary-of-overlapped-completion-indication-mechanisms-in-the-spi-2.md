---
description: Windows 通訊端中重迭的完成指示機制的摘要， (Winsock) SPI。
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: SPI 中重迭完成指示機制的摘要
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113000"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>SPI 中重迭完成指示機制的摘要

下表摘要說明重迭通訊端的完成語義，顯示各種 *lpOverlapped*、 **hEvent** 和 *lpCompletionRoutine* 的組合。



| *lpOverlapped* | **hEvent**     | *lpCompletionRoutine* | 完成指示                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | 不適用 | 忽略               | 作業會以同步方式完成，也就是說，它的行為會如同 nonoverlapped 通訊端一樣。                                                                                                                                 |
| 非 Null       | NULL           | NULL                  | 作業已完成重迭，但沒有 Windows 通訊端2支援的完成機制。 完成埠機制 (如果在此情況下可以使用支援的) ，否則就不會有完成通知。 |
| 非 Null       | 非 Null       | NULL                  | 作業完成重迭，由訊號事件物件發出通知。                                                                                                                                                      |
| 非 Null       | 忽略        | 非 Null              | 作業完成重迭，藉由排程完成常式來通知。                                                                                                                                               |



 

 

 



