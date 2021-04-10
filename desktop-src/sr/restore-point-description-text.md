---
title: 還原點描述文字
description: 當應用程式呼叫 SRSetRestorePoint 函式時，它可以提供任何文字做為還原點的描述;但是，下表顯示建議的描述文字。
ms.assetid: e6e1974b-c162-4019-9349-936f3786cb9b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e90fd1b7d5776c8c3798a68946382cc702b3bd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183607"
---
# <a name="restore-point-description-text"></a>還原點描述文字

當應用程式呼叫 [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) 函式時，它可以提供任何文字做為還原點的描述;但是，下表顯示建議的描述文字。



| 系統修改                            | 還原點類型      | Description            |
|------------------------------------------------|-------------------------|------------------------|
| 應用程式安裝                       | 應用程式 \_ 安裝    | 安裝的 *AppName*    |
|  (新增/移除功能) 的應用程式修改 | 修改 \_ 設定        | 設定的 *AppName*   |
| 移除應用程式                            | 應用程式 \_ 卸載  | 已移除 *AppName*      |
| 設備磁碟機安裝                     | 設備 \_ 磁碟機 \_ 安裝 | 安裝的 *DriverName* |



 

安裝程式（例如 Windows Installer 和 InstallShield）會將這些慣例用於描述文字：

-   產品名稱後面接著動詞;例如，安裝了 *AppName*。
-   您可以單獨使用產品名稱 (*appname*) 或產品名稱，也可以使用 (*MyCompany appname*) 的公司名稱。

 

 




