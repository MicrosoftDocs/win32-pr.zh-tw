---
title: Message duration 參數
description: 應用程式通常會使用快顯視窗，簡短地向使用者顯示重要的通知訊息。 應用程式會建立視窗、顯示應用程式定義的持續時間，然後終結視窗。
ms.assetid: a3f7a8d8-78e7-4fb0-8ee2-bd9341857153
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2a99a43ace763da94944da334b0865c768cc920
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375568"
---
# <a name="message-duration-parameter"></a>Message duration 參數

應用程式通常會使用快顯視窗，簡短地向使用者顯示重要的通知訊息。 應用程式會建立視窗、顯示應用程式定義的持續時間，然後終結視窗。

由於具有視覺障礙或認知狀況的使用者可能需要更多時間來讀取通知快顯視窗，因此應用程式不應該對持續時間進行硬式編碼。 相反地，應用程式應該根據 **SPI \_ GETMESSAGEDURATION** 系統參數的值來設定持續時間。 若要取得此參數，請使用 [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) 函數。

輔助技術應用程式可以設定 **SPI \_ SETMESSAGEDURATION** 系統參數，根據使用者輸入來設定訊息持續時間。

 

 