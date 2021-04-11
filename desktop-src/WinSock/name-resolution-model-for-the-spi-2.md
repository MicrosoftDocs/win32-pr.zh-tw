---
description: Windows 通訊端的名稱解析和註冊模型 (Winsock) SPI。
ms.assetid: b173b63e-42c7-4f85-b55f-1f7b3bff7c4f
title: SPI 的名稱解析模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e79593f56cd11671b3c16ef9098d455bf548505
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113033"
---
# <a name="name-resolution-model-for-the-spi"></a>SPI 的名稱解析模型

在開發與通訊協定無關的用戶端/伺服器應用程式時，有兩個基本的需求存在於名稱解析和註冊方面：

-   伺服器一半的應用程式 (在此稱為服務，) 在 (中註冊其存在，或可) 一個或多個命名空間存取。
-   用戶端應用程式在命名空間中尋找服務的能力，並取得所需的傳輸通訊協定和定址資訊。

針對習慣開發以 TCP/IP 為基礎的應用程式的人，這可能只需要查閱主機位址，然後使用同意的埠號碼。 不過，其他網路設定可允許服務的位置、用於服務的通訊協定，以及在執行時間探索到的其他屬性。 為了容納現有名稱服務中的功能範圍，Windows 通訊端2介面採用如下所述的模型。

「 *命名空間* 」（namespace）是指將 (與一個或多個人易記名稱的通訊協定) 的最小值相關聯的功能，以及定址網路服務的屬性。 許多命名空間目前可廣泛使用，包括網際網路的網域名稱系統 (DNS) 、NetWare 目錄服務 (NDS) 、X 500 等等。這些命名空間的組織和實行方式有很大的差異。 從 Windows 通訊端名稱解析的觀點來看，某些屬性特別重要。

 

 



