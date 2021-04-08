---
title: 語音引擎選取專案
description: 語音引擎選取專案
ms.assetid: f5afedc6-093f-4247-a5c8-277d6b2d646c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a548f0201ba37c8acb867091cc690a913277ff06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839863"
---
# <a name="speech-engine-selection"></a>語音引擎選取專案

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

字元的語言識別項設定會決定其預設的語音輸入語言;Microsoft Agent 會針對符合該語言的已安裝引擎要求 SAPI。 如果用戶端應用程式未指定語言喜好設定，Microsoft 代理程式將會嘗試使用主要語言識別項來尋找符合使用者預設語言識別項 (的語音辨識引擎，然後) 次要語言識別項。 如果沒有符合此語言的引擎可使用，則會停用該字元的語音。

您也可以使用 [**SRModeID**](srmodeid-property.md) 屬性) 來指定 (的模式識別碼，以要求特定的語音辨識引擎。 但是，如果該模式識別碼的語言識別項不符合用戶端的語言設定，則呼叫會失敗 (在控制項) 中引發錯誤。 然後，語音辨識引擎會保留用戶端最後一個成功設定的引擎，如果沒有，則為符合目前系統語言識別項的引擎。 如果仍沒有相符的結果，則不會提供該用戶端的語音輸入。

當使用者按下接聽熱鍵或輸入主動用戶端呼叫 [**接聽**](listen-method.md) 方法時，Microsoft 代理程式會自動載入語音辨識引擎。 不過，您也可以在設定或查詢其模式識別碼、設定或查詢 [語音命令] 視窗的屬性、查詢 [**SRStatus**](srstatus-property.md)，或是啟用語音時，以及使用者顯示 [Advanced Character] 選項的 [語音輸入] 頁面時載入引擎。 不過，Microsoft 代理程式只會持續載入用戶端所使用的語音引擎。

 

 




