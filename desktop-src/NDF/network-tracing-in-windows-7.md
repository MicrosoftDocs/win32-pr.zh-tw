---
title: Windows 7 中的網路追蹤
description: Windows 7 (NDF) 擴充網路診斷架構，以提供快速的方法來疑難排解網路連線問題，方法是在一個步驟中啟用所有所需資訊的收集，以及利用 Windows 的事件追蹤 (ETW) 將網路事件封包記錄在單一檔案中。
ms.assetid: 7d331362-ff26-4ca0-aa45-07cc97304c7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e3abb4283262703123f8e7060a09af0b810477b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382801"
---
# <a name="network-tracing-in-windows-7"></a>Windows 7 中的網路追蹤

當網路堆疊的複雜性增加時，通常很難快速追蹤和診斷堆疊內的問題。 Windows 7 (NDF) 擴充網路診斷架構，以提供快速的方法來疑難排解網路連線問題，方法是在一個步驟中啟用所有所需資訊的收集，以及利用 [Windows 的事件追蹤 (ETW) ](../etw/event-tracing-portal.md) 將網路事件記錄 & 單一檔案中的封包。

相關事件和封包會在網路堆疊的各種元件中，針對指定的活動（例如流覽網站）群組在一起。 此進程的輸出是 (ETL) 檔的事件追蹤記錄。 藉由允許在這個檔案中一次查看與特定活動相關的所有事件，就能大幅降低隔離及診斷網路問題所需的時間。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|
| [Windows 7 中的網路追蹤：架構](network-tracing-in-windows-7-architecture.md)                                |
| [在 Windows 7 中使用網路追蹤進行疑難排解的工具](tools-for-troubleshooting-network-tracing-in-windows-7.md) |
| [Windows 7 中的網路追蹤：案例](network-tracing-in-windows-7-scenarios.md)                                      |



 

 

 