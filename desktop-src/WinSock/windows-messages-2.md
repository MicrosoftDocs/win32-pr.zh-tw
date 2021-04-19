---
description: Windows 通訊端1.1 引進了非同步選擇機制，可提供不涉及輪詢或封鎖的網路事件指示。
ms.assetid: d536f796-c532-4b57-8dc7-3415661b736b
title: Windows 訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac0f60bb597a7dd92c0039dd805a971bb8587ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969232"
---
# <a name="windows-messages"></a>Windows 訊息

Windows 通訊端1.1 引進了非同步選擇機制，可提供不涉及輪詢或封鎖的網路事件指示。 [**WSPAsyncSelect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85))函式可用來註冊一或多個網路事件（如上所列）的興趣，並提供要用於通知的視窗控制碼。 當指定的網路事件發生時，會將用戶端指定的 Windows 訊息傳送至指定的視窗。 服務提供者必須使用 [**WPUPostMessage**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpupostmessage) 函式來完成此工作。

在 Windows 中，這可能不是最有效率的通知機制，對不想開啟任何視窗的守護程式和服務而言很方便。 為了解決此問題，我們引進了下列所述的事件物件信號機制。

 

 
