---
description: 下表依類別順序依重要性列出 TAPI 第3版 COM 介面。
ms.assetid: fafb6d6e-934e-4942-8b90-dacb7ba09752
title: 通話和媒體控制項快速參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ed3105612205d6d516b8d0c5e4f0a7bf9719b3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106986667"
---
# <a name="call-and-media-controls-quick-reference"></a>通話和媒體控制項快速參考

\[[IPCONF MSP 介面](ipconf-msp-interfaces.md)無法在 windows Vista、windows Server 2008 和後續版本的作業系統中使用。 RTC 用戶端 API 提供類似的功能。\]

下表依類別順序依重要性列出 TAPI 第3版 COM 介面。 這些介面會根據 TAPI 3 的五個基本呼叫控制物件來分組： TAPI、Address、Terminal、Call 和 CallHub。 其餘介面會根據自動呼叫散發進行分組 (ACD) 介面，可提供話務中心功能;列舉值介面和獨立物件。



| 介面群組                                          | Description                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [TAPI 物件介面](tapi-object-interfaces.md)         | TAPI 物件是 TAPI 3 的主要物件。                                                                                                                                                                                                              |
| [位址物件介面](address-object-interfaces.md)   | Address 物件代表可以進行或接收呼叫的實體。 相關聯的介面和方法可讓應用程式取得和設定位址的相關資訊，例如它是否有呼叫端識別碼支援。                             |
| [終端物件介面](terminal-object-interfaces.md) | 終端物件代表呼叫終止或起始點的接收或來源。 相關聯的介面和方法可讓應用程式取得和設定終端機的相關資訊，例如其目前是否正在使用中。 |
| [呼叫物件介面](call-object-interfaces.md)         | 呼叫物件代表呼叫，並且會在呼叫存在時建立。 相關聯的介面和方法會取得和設定有關呼叫的資訊，例如目前的撥號狀態。                                                           |
| [電話物件介面](phone-object-interfaces.md)       | 電話物件是代表實際電話裝置及其所有控制項的實體。                                                                                                                                                             |
| [IPConf MSP 介面](ipconf-msp-interfaces.md)           | 「IP 會議 MSP」會針對在呼叫物件上公開的參與者控制項，實行數個介面。                                                                                                                                          |
| [CallHub 物件介面](callhub-object-interfaces.md)   | CallHub 物件代表多方呼叫的協力廠商觀點。 相關聯的介面和方法會取得並設定有關呼叫的資訊，例如呼叫中樞是否為使用中。                                                          |
| [列舉值介面](enumerator-interfaces.md)           | COM 標準列舉值介面。                                                                                                                                                                                                                         |
| [事件介面](./event-interfaces.md)            | 事件介面也會顯示其物件或函式群組。                                                                                                                                                                                |
| [獨立物件](stand-alone-objects.md)               | TAPI 3 的其他獨立物件提供操作的介面和方法，例如協助電話語音或事件處理。                                                                                                                    |



 

 

 
