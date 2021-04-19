---
description: 在 Microsoft 電話語音中，電話語音服務提供者是在與電話語音應用程式不同的進程中執行。
ms.assetid: ccc40d3c-6764-469a-baac-fa625d664ea7
title: 電話語音服務提供程式 UI DLL 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdab33dd9c9630aed7d7aed168982cfac2daee2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969351"
---
# <a name="the-telephony-service-provider-ui-dll-interface"></a>電話語音服務提供程式 UI DLL 介面

在 Microsoft 電話語音中，電話語音服務提供者是在與電話語音應用程式不同的進程中執行。 服務提供者會透過電話語音服務提供者介面與 TAPISRV 通訊 (TSPI) 並在其處理常式中執行;應用程式介面至 TAPI，會載入至應用程式內容中。

TAPI 的元件使用各種處理序間通訊機制，在應用程式與服務提供者之間傳遞函式要求和訊息。 應用程式和服務提供者可能不只會在不同的進程中執行，而是在完全不同的系統上執行。 因此，服務提供者無法在進程中或甚至是在執行的電腦上顯示對話方塊;您必須在應用程式執行所在的電腦上，從應用程式內容中叫用 UI。

本節定義在應用程式內容中載入及叫用服務提供者 UI 函式的機制。 當應用程式不會以其他方式在應用程式中開啟對話方塊時，也會定義一個機制，讓服務提供者可以在應用程式內容中，以自發的方式開啟對話方塊。 第二個案例的範例是，當數據機用來作為互動式語音通話的撥號程式時，資料數據機服務提供者所顯示的 [ **交談/掛斷** ] 對話方塊，而且必須通知使用者選擇電話，並通知服務提供者何時放置數據機 onhook。

 

 



