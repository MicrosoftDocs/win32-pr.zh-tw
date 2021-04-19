---
description: 資料流程物件是與呼叫會話相關聯之媒體資料流程或資料流程的抽象概念。
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: 資料流程物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979898"
---
# <a name="stream-objects"></a>資料流程物件

資料流程物件是與呼叫會話相關聯之媒體資料流程或資料流程的抽象概念。 在 stream 和子資料流程物件上公開的介面和方法可讓應用程式執行非常詳細的控制項，例如暫停串流、將新的媒體類型新增至通訊會話，或調整特定會議參與者的音訊音量。

資料流程和子資料流程是資料流程的兩種主要類型。 標準執行的介面和方法類似于兩者，但 substreaming 允許較低層級的控制。  (Msp) 的所有媒體服務提供者都必須執行基本的資料流程控制介面，但支援子串流是選擇性的。

此外，某些服務提供者會為數據流執行 [提供者特定的介面](provider-specific-interfaces.md) 。 例如，IPConf MSP 提供參與者層級的控制項。 如需摘要，請參閱 [IPCONF MSP 介面](ipconf-msp-interfaces.md) 。 如需其他可能會執行的介面，請參閱服務提供者的檔。

MSP 和 TAPI 會在初始設定傳出或傳入會話的期間，建立用於呼叫的資料流程物件。 應用程式會負責識別這些資料流程的適當終端機，並選取終端機至資料流程。

請注意，在某些情況下，MSP 可能會要求應用程式在特定呼叫會話作業之前停止或暫停串流。

串流介面記載于 [媒體服務提供者介面 (MSPI) 參考](media-service-provider-interface-mspi-reference.md)中。

[選取終端](select-a-terminal.md)機程式碼範例會示範如何列舉資料流程，以及如何在其上選取終端機。

 

 



