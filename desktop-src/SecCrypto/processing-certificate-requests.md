---
description: 說明憑證服務如何處理憑證要求。
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: 處理憑證要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2c8e8acacbb001803cf3ce8d7e1263e920673eb912a04105ec8bb2772953a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977400"
---
# <a name="processing-certificate-requests"></a>處理憑證要求

憑證服務會在處理 [*憑證要求*](../secgloss/c-gly.md)時執行下列步驟：

1.  要求接收。

    用戶端會將 [*憑證要求*](../secgloss/c-gly.md) 傳送到中繼應用程式，並將其格式化為 PKCS \# 10 格式要求，並將它提交至伺服器引擎。

2.  要求核准。

    伺服器引擎會呼叫 [原則模組](policy-modules.md)，此模組會查詢要求屬性、決定要求是否已獲授權，並設定選用的憑證屬性。

3.  憑證的形式。

    如果要求已核准，則伺服器引擎會接受要求和原則模組所要求的任何屬性，並建立完整的憑證。

4.  憑證發佈。

    伺服器引擎會將已完成的憑證儲存在憑證服務資料庫中，並通知中繼應用程式要求狀態。 如果結束 [模組](exit-modules.md) 有這樣的要求，伺服器引擎會通知它有憑證發佈事件。 這可讓結束模組執行進一步的作業，例如將憑證發佈至外部憑證儲存機制 (例如目錄服務) 。 同時，中繼會從憑證服務取得已發佈的憑證，並將其傳回給用戶端。

下圖顯示憑證 [*要求*](../secgloss/c-gly.md) 如何由憑證服務處理。

![處理憑證要求](images/certflow.png)

 

 
