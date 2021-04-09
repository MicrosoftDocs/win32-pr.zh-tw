---
title: 關於自訂檔案和串流處理常式
description: 關於自訂檔案和串流處理常式
ms.assetid: 6a00c8db-3ac6-4826-a373-52b6b7d1652f
keywords:
- Windows (VFW) 自訂檔案處理常式的影片
- Windows (VFW) 、自訂串流處理常式的影片
- Windows (VFW) 的影片，檔處理常式
- 適用于 Windows (VFW) 、串流處理常式的影片
- 適用于 Windows) 、自訂檔案處理常式的 VFW (影片
- 適用于 Windows) 、自訂串流處理常式的 VFW (影片
- 適用于 Windows) 的 VFW (影片，檔處理常式
- 適用于 Windows) 、串流處理常式的 VFW (影片
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94e1872aa8a2f5c55df0db43860e318c792801e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840800"
---
# <a name="about-custom-file-and-stream-handlers"></a>關於自訂檔案和串流處理常式

您的應用程式可以使用自訂檔案處理常式從檔案讀取或寫入至非標準格式的檔案。 若要這樣做，您的應用程式只會在開啟檔案或設定檔案介面時，使用您的檔處理常式名稱。 AVIFile 程式庫接著會使用來自檔案處理常式的函式，而不是來自另一個檔案處理常式的函式。 非標準格式會顯示為應用程式的標準 AVI 資料，或使用自訂檔案處理常式的任何其他應用程式。

同樣地，您的應用程式可以使用自訂資料流程處理常式來讀取非標準格式的資料流程。 資料流程（不論是構成音訊、影片、MIDI、文字或自訂資料）是 AVI 檔案的元件。 例如，包含影片順序的 AVI 檔案、英文的聲段和法文的聲帶都包含三個數據流。 您的應用程式可以指定 AVI 檔中的資料流程來處理，並將每個資料流程導向至可以最佳方式處理適當多媒體資料類型的處理常式。

> [!Note]  
> 您必須將自訂資料流程和檔案處理常式放在一或多個 Dll 中，並與主要應用程式檔分開。

 

 

 




