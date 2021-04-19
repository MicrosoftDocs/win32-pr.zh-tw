---
description: 預測撥號是通常會在撥接中心電話語音伺服器上執行的應用程式。
ms.assetid: c8d0b2b5-61eb-4ab0-b09d-c54c282b730e
title: 預測撥號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576ebffff5d4b9925fd50ecce082e4f515065c5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106995862"
---
# <a name="predictive-dialing"></a>預測撥號

預測撥號是通常會在撥接中心電話語音伺服器上執行的應用程式。 它會使用電話號碼清單（通常是從資料庫取得）來嘗試撥出電話;當呼叫 *完成* 時，會自動將呼叫指派給代理程式進行處理。 應用程式可以在交換器上使用 *預測撥號埠* ，也就是可以撥出電話並具有特殊功能 (透過 DSP 的裝置，因此) 偵測通話進度的聲音以及其他通話狀態的徵兆。 在預測撥號埠上進行呼叫時，通常會在呼叫達到特定狀態或偵測到特定媒體類型時，自動傳送至交換器上的另一個裝置;此目標裝置可以是處理外寄呼叫之代理程式的佇列。

應用程式會透過 \_ [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)中 **dwAddrCapFlags** 成員的 LINEADDRCAPFLAGS PREDICTIVEDIALER 位，將裝置識別為具有預測撥號功能。 **LINEADDRESSCAPS** 中的 **dwPredictiveAutoTransferStates** 成員會指出可將預測撥號埠傳送給自動傳送呼叫的狀態。如果這個成員為零，則表示自動傳輸無法使用，而且在偵測到適當的撥號狀態 (或媒體類型或其他準則) 時，應用程式會負責明確地傳送呼叫。 交換器製造商最好能夠同時提供自動和手動傳輸，並允許應用程式選取慣用的機制，但服務提供者必須建立舊設備的行為模型。 單一的預測撥號埠 (線路裝置/位址) 可支援同時進行數個撥出電話，如 **LINEADDRESSCAPS** 中的 **dwMaxNumActiveCalls** 成員所示。 您也可以在任何裝置上使用預測撥號功能，其使用的是預測撥號信號處理器的共用集區，這些處理器會橋接到要求時所撥打的行。

當 LineMakeCall 函式在能夠預測撥號的行上使用[](/windows/desktop/api/Tapi/nf-tapi-linemakecall)函式時 (有 LINEADDRCAPFLAGS \_ PREDICTIVEDIALER 設定的埠) 並且會使用 LINECALLPARAMFLAGS PREDICTIVEDIAL 要求預測撥號 \_ ，然後以預測的方式進行呼叫，並提供增強的通話進度偵測。 在傳遞至 **lineMakeCall** 的 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)結構中定義其他欄位和常數，以控制預測撥號埠的行為。 **DwPredictiveAutoTransferStates** 成員會指出行呼叫指出，進入呼叫其中任何一項時，預測撥號埠應該會自動將呼叫傳送至指定的目標 (bits 必須是 [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)) 中所指出支援之自動傳輸狀態的適當子集。如果您想要監視撥號狀態本身，並在到達所需的條件時使用 [**lineBlindTransfer**](/windows/desktop/api/Tapi/nf-tapi-lineblindtransfer)來傳送呼叫，則應用程式可以讓欄位保持設定為0。 應用程式必須在 **LINECALLPARAMS** 中由 **dwTargetAddressSize** 和 **dwTargetAddressOffset** 成員所定義的變數欄位中，指定應自動傳送呼叫的目標位址。

應用程式也可以設定撥出電話的超時時間，讓服務提供者在沒有回應時，自動將它們轉換成中斷線上狀態。 這是使用 [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams)中的 **dwNoAnswerTimeout** 成員來控制。

 

 



