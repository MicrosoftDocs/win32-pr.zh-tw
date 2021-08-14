---
description: 透過協力廠商連結監視的工作站集會被模型化為線路裝置，也可能是關聯的電話裝置。
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: 站
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad9874542a63f05e124ea5df833aa0a433c03713cc3a2d7bb1ca3a471174e86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760713"
---
# <a name="stations"></a>站

透過協力廠商連結監視的工作站集會被模型化為線路裝置，也可能是關聯的電話裝置。 如果模型化終端 (DN) 支援一個以上的目錄編號，線路裝置可以有多個位址。 相同 DN 上的多個呼叫外觀可以模型化為支援多個呼叫的單一位址。

交換器上兩個電臺之間的呼叫會有兩個呼叫控制碼，一種是提供第一個站 (在其線路裝置上的呼叫視圖) ，另一個則是從第二站裝置上的第二站 () 。 例如，應用程式在伺服器上的協力廠商 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) 會被導向至與撥打電話的來源裝置相關聯的線路裝置;在 ([**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) 中指定的位址上，會針對該行建立呼叫控制碼，以控制在支援多個 DNs) 的電話上使用的 DN。 當將呼叫提供給目的地位址時，會建立新的呼叫控制碼，顯示 *提供* 狀態的呼叫;應用程式會知道它是相同呼叫的另一個觀點，而 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **dwCallID** 成員對兩個呼叫都相等。 當呼叫中斷時，這兩個呼叫都會 *閒置* ;您可以透過在其中一個呼叫控制碼上執行 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ，從協力廠商應用程式中卸載呼叫。

 

 



