---
description: 強烈建議您在第一次嘗試安裝封裝之前，先對每個新的或新修改的安裝套件執行驗證。
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: 套件驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848772"
---
# <a name="package-validation"></a>套件驗證

強烈建議您在第一次嘗試安裝封裝之前，先對每個新的或新修改的安裝套件執行驗證。

封裝驗證封裝含下列三個進程：

-   [內部驗證](internal-validation.md)
-   [字串集區驗證](string-pool-validation.md)
-   [內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)

合併模組應使用 [驗證合併模組](validating-merge-modules.md)中描述的方法進行驗證。

Evalcom2.dll 提供的 COM 物件可執行安裝封裝和合併模組的驗證作業。 主要物件會執行 C/c + + 程式的介面。 如需詳細資訊，請參閱 [驗證自動化](validation-automation.md)。

 

 



