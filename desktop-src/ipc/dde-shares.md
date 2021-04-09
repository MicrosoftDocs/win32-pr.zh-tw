---
description: DDE 共用是一種機器資源。
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: DDE 共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849527"
---
# <a name="dde-shares"></a>DDE 共用

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

DDE 共用是一種機器資源。 它們類似于檔案共用，因為它們是用來控制對資源的存取。 使用檔案共用時，資源為檔案。 使用 DDE 共用時，資源會動態地交換資料。 交換的資料類型取決於提供資料的伺服器應用程式，以及要求資料的用戶端應用程式。

伺服器會呼叫 [**NDdeShareAdd**](nddeshareadd.md) 函式來建立 dde 共用，此共用儲存在 dde 共用資料庫管理員中， (DSDM) 。

用戶端會藉由連線至 DDE 共用來啟動 DDE 交談。 用戶端必須呼叫 [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) 函式來初始化 DDEML，然後呼叫 [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) 函式以連接至 DDE 共用。 在 **DdeConnect** 呼叫中，用戶端會指定服務名稱，如下所示：

\\\\*ComputerName* \\NDDE $

其中 *ComputerName* 是執行伺服器應用程式的電腦名稱稱。 NDDE $ 表示提供給 [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) 的主題是名為 *ComputerName* 的遠端電腦上的 DDE 共用名稱。

有三種類型的 DDE 共用：舊樣式、新樣式和靜態。 一般只支援靜態型別。 靜態共用的名稱使用下列慣例： *共用* 名 $。

 

 
