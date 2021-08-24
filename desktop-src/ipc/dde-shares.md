---
description: DDE 共用是一種機器資源。
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: DDE 共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e3416235f78e48c68b7d2e35c7ac042f8ff5d6eac79cc2471efa5ea12d82b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602118"
---
# <a name="dde-shares"></a>DDE 共用

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

DDE 共用是一種機器資源。 它們類似于檔案共用，因為它們是用來控制對資源的存取。 使用檔案共用時，資源為檔案。 使用 DDE 共用時，資源會動態地交換資料。 交換的資料類型取決於提供資料的伺服器應用程式，以及要求資料的用戶端應用程式。

伺服器會呼叫 [**NDdeShareAdd**](nddeshareadd.md) 函式來建立 dde 共用，此共用儲存在 dde 共用資料庫管理員中， (DSDM) 。

用戶端會藉由連線至 DDE 共用來啟動 DDE 交談。 用戶端必須呼叫 [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) 函式來初始化 DDEML，然後呼叫 [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) 函式以連接至 DDE 共用。 在 **DdeConnect** 呼叫中，用戶端會指定服務名稱，如下所示：

\\\\*ComputerName* \\NDDE $

其中 *ComputerName* 是執行伺服器應用程式的電腦名稱稱。 NDDE $ 表示提供給 [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) 的主題是名為 *ComputerName* 的遠端電腦上的 DDE 共用名稱。

有三種類型的 DDE 共用：舊樣式、新樣式和靜態。 一般只支援靜態型別。 靜態共用的名稱使用下列慣例： *共用* 名 $。

 

 
