---
description: 在開始開發 Microsoft Windows HTTP 服務 (WinHTTP) 應用程式之前，您必須先決定是否要使用 C/c + + API 或 COM 介面。
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: 選擇 WinHTTP 介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7772959bd76dc7a257abc180c915f99df988a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472354"
---
# <a name="choosing-a-winhttp-interface"></a>選擇 WinHTTP 介面

在開始開發 Microsoft Windows HTTP 服務 (WinHTTP) 應用程式之前，您必須先決定是否要使用 C/c + + API 或 COM 介面。 下表摘要說明每個方法的相關優點和缺點。




|  | C/C + + API | COM 介面 | 
|--|-----------|---------------|
| 優點 | <ul><li>您可以在區塊中處理回應，這會更有效率。</li><li>POST 作業也可以在區塊中處理，以加速處理時間。</li><li>自動代理支援。</li><li>存取 WinHTTP 的完整功能集。</li><li>您可以輕鬆地處理二進位資料。</li></ul> | <ul><li>建立應用程式很容易，而且需要比 C/c + + API 更少的程式程式碼。</li><li>指令碼語言可以使用此介面。</li></ul> | 
| 缺點 | <ul><li>處理更為複雜。</li><li>C/c + + API 需要的步驟多於 COM 介面，才能執行相同的動作。</li><li>設定要求需要更多程式碼。</li></ul> | <ul><li>COM 介面不提供對 WinHTTP 完整功能集的存取權。</li><li>很難處理某些指令碼語言中的二進位資料類型，例如 VBScript 和 JScript。</li><li>COM 介面不支援自動代理。</li><li>應用程式必須使用 COM APARTMENT_THREADED 模型。</li><li>在開始處理回應之前，必須先接收和緩衝處理整個回應。</li></ul> | 




 

 

 



