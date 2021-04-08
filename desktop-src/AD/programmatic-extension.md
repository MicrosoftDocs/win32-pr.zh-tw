---
title: 程式設計延伸
description: 程式設計擴充有許多優點，但應用程式是不透明的;系統管理員必須信任安裝應用程式隨附的檔。
ms.assetid: e2837757-f887-4d17-a9d2-8989533a3d8e
ms.tgt_platform: multiple
keywords:
- 程式設計延伸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac30017271626e9b4afe8a510f3424e9bb70013
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671255"
---
# <a name="programmatic-extension"></a>程式設計延伸

LDIF 檔案的優點是系統管理員可以檢查它的功能。 不過，架構也可以透過程式設計的方式擴充。 程式設計延伸有許多優點，但應用程式是不透明的;系統管理員必須信任安裝應用程式隨附的檔。 使用程式設計架構延伸可能是使用它們的應用程式部署的障礙。 程式設計延伸是不變的;它是 Windows NT 可執行檔。 二進位檔不能被篡改，不同于 LDIF 或 .csv 檔案，這些檔案可以不小心或惡意的方式編輯。

LDIF 檔案的優點包括：

-   應用程式可以偵測和復原錯誤，並提供使用者意見反應。
-   應用程式可以處理 Unicode，而不需要採用 Base64 編碼。
-   應用程式可利用 Windows Installer 的安裝程式 Api。
-   您可以簽署應用程式以建立真實性。

 

 




