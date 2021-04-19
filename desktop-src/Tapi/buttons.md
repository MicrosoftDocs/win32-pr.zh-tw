---
description: Microsoft 電話語音會將電話按鈕和燈模型為按鈕的燈配對。
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: " (電話語音 API) 的按鈕"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993058"
---
# <a name="buttons-telephony-api"></a> (電話語音 API) 的按鈕

Microsoft 電話語音會將電話的按鈕和燈模型為按鈕的燈配對。 旁邊沒有燈泡的按鈕，或使用遺失燈或按鈕的虛擬指標來指定沒有按鈕的燈。 具有多個燈的按鈕會使用多個按鈕的燈配對來建立模型。

您可以設定和取出與電話按鈕相關聯的資訊。 按下按鈕時，服務提供者會將 [**電話 \_ 按鈕**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) 訊息傳送至 TAPI 回呼函式。 此訊息的參數是手機裝置的控制碼，以及按下按鈕的按鈕/燈泡識別碼。 鍵盤按鍵 ' 0 ' 到 ' 9 '、' \* ' 和 ' \# ' 是指派固定的按鈕/燈泡識別碼0到11。

函式 [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) 會設定與手機裝置上的按鈕相關聯的資訊。 [**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) 會傳回與手機裝置上按鈕相關聯的資訊。 \_當按下電話上的按鈕時，服務提供者會將電話按鈕訊息傳送至 TAPI 回呼函式。

與按鈕相關聯的資訊在 TSPI 時並不會包含任何語義意義。 它適用于針對指定的電話裝置解讀這項資訊的裝置特定應用程式，或向使用者顯示（例如在應用程式的說明系統中）。

 

 
