---
description: 當 (SSP) 安全性套件建立安全性支援提供者時，您不應該允許加入網域的用戶端使用下列格式的兩個元件服務提供者名稱 (SPN) 來驗證網域控制站。
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: 使用三部分主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05ddc9ce552e71d97c5e795b7405e97803991133a96e7b3fac3e1a81bc45d5ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915180"
---
# <a name="using-three-part-principal-names"></a>使用三部分主體名稱

當 (SSP) 安全性套件建立安全性支援提供者時，您不應該允許加入網域的用戶端使用下列格式的兩個元件服務提供者名稱 (SPN) 來驗證網域控制站。

-   <*通訊協定* >/<*主機名稱*>

用戶端應該一律藉由指定網域來進行驗證。

-   <*通訊協定* >/<*主機名稱* >/<*功能變數名稱*>

加入網域的用戶端若以兩部分 SPN 登入，可能就可以模擬網域控制站。 如果您允許兩部分 Spn，您應該建立包含足夠資訊的記錄專案，讓系統管理員能夠識別呼叫者。

 

 



