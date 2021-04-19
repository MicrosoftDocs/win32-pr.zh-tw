---
description: 當 (SSP) 安全性套件建立安全性支援提供者時，您不應該允許加入網域的用戶端使用下列格式的兩個元件服務提供者名稱 (SPN) 來驗證網域控制站。
ms.assetid: 6CD3BC5E-F9B2-4E8E-9DEE-064AE8837DFB
title: 使用三部分主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8760ba740843c62c39a98e7e4683d25410a94ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970154"
---
# <a name="using-three-part-principal-names"></a>使用三部分主體名稱

當 (SSP) 安全性套件建立安全性支援提供者時，您不應該允許加入網域的用戶端使用下列格式的兩個元件服務提供者名稱 (SPN) 來驗證網域控制站。

-   <*通訊協定* >/<*主機名稱*>

用戶端應該一律藉由指定網域來進行驗證。

-   <*通訊協定* >/<*主機名稱* >/<*功能變數名稱*>

加入網域的用戶端若以兩部分 SPN 登入，可能就可以模擬網域控制站。 如果您允許兩部分 Spn，您應該建立包含足夠資訊的記錄專案，讓系統管理員能夠識別呼叫者。

 

 



