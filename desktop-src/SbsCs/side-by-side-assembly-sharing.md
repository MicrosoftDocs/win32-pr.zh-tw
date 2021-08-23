---
description: 下圖說明兩個應用程式如何使用傳統的元件共用方法共用元件。
ms.assetid: 2b9c6511-ae79-498f-a20c-ccb32a623d42
title: 並存元件共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59dcfbb40040b51fc2e17d3707d4a76c7ea5ddadf1806e41b7a7fbd81860ae15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141807"
---
# <a name="side-by-side-assembly-sharing"></a>並存元件共用

下圖說明兩個應用程式如何使用傳統的元件共用方法共用元件。 當應用程式安裝的元件版本（通常是 DLL）無法回溯相容時，就會發生傳統的元件共用問題。 剛剛安裝的應用程式可運作，但相依于先前 DLL 版本的應用程式可能無法再運作。

![代表共用元件的兩個應用程式](images/sxs1.png)

隔離應用程式和並存元件方案可讓相同 Win32 元件的不同版本在相同的系統上同時執行，而不會發生衝突。 藉由指定應用程式應該使用的並存元件版本，開發人員可保證其測試的設定一律會在使用者的電腦上重複。 下圖說明並列共用的位置。

![並行元件共用的執行](images/sxs2.png)

如需詳細資訊，請參閱 [關於隔離應用程式和並存元件](about-isolated-applications-and-side-by-side-assemblies.md)。

 

 



