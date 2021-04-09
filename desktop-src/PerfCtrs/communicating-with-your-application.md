---
description: 一般而言，提供者會代表應用程式提供資料。
ms.assetid: 65ea6099-79df-4baa-9752-7df032ccc9a0
title: 與您的應用程式通訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6def58d3e03676f3b1b46ba3ebd756eb3adc6196
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849297"
---
# <a name="communicating-with-your-application"></a>與您的應用程式通訊

一般而言，提供者會代表應用程式提供資料。 例如，伺服器可能會建立效能 DLL 來提供其計數器資料。 應用程式與其提供者之間的通訊，會因使用者模式和核心模式應用程式而有所不同。 提供者會在使用者模式中執行。 因此，使用者模式應用程式（例如列印和顯示應用程式）可以使用任何技術進行處理序間通訊，例如具名管道、檔案對應或 RPC。 不過，核心模式應用程式必須提供將效能資料傳回給提供者的 IOCTL 介面。

> [!WARNING]
> 請勿使用 COM 作為 IPC 機制。 系統無法保證呼叫介面之執行緒的 COM 初始化狀態。 因此，DLL 可能無法成功初始化 COM 並收集資料。

 

 

 



