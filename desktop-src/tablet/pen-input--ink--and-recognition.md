---
description: Tablet PC 有一個有趣的新功能，就是手寫筆的輸入系統。
ms.assetid: 8432617a-5ae7-44cb-a5f7-f3b2d8885846
title: 畫筆輸入、筆跡和辨識
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a46d865e40d1779edaa2607b1754c45659609b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104568295"
---
# <a name="pen-input-ink-and-recognition"></a>畫筆輸入、筆跡和辨識

Tablet PC 有一個有趣的新功能，就是手寫筆的輸入系統。 所有 Tablet PC 電腦在畫面下方都有一個接受畫筆輸入的數位板。 這種新的輸入機制需要您思考如何特別針對 Tablet PC 建立應用程式。  (API) 的 Tablet PC 平臺應用程式開發介面可協助您進行此作業。

## <a name="collection-data-management-and-recognition"></a>集合、資料管理和辨識

Tablet PC 平臺可以分成三個不同的區域：

-   筆墨集合 (用來從數位板) 收集筆墨的物件。
-   筆墨資料管理 (用來管理所收集之筆墨) 的物件。
-   筆跡辨識 (物件，用來將所收集的筆墨轉換成其他類型的資料，例如文字) 。

下圖將概要說明 Tablet Collection API 如何 (畫筆 API) 、筆墨資料管理 API (筆墨 API) 和筆跡辨識 API (辨識 API) 在 Tablet PC 平臺中一起運作。

![顯示畫筆 api、筆墨 api 和辨識 api 如何一起運作的圖例](images/aabc298b-fd64-435b-87bc-eb7cd11524e8.jpg)

Tablet PC 平臺 API 適用于受控 Api 和 COM 程式庫。 下列主題描述 API 中的物件，並說明應用程式如何使用這些物件：

-   [筆墨集合](ink-collection.md)
-   [筆墨資料](ink-data.md)
-   [筆跡辨識](ink-recognition.md)
-   [筆墨分析](ink-analysis.md)
-   [Windows Server 2008 R2 中的手寫辨識](handwriting-recognition-in-windows-server-2008-r2.md)

 

 



