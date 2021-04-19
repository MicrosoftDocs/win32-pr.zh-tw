---
description: 若要讓認證安全性支援提供者通訊協定 (CredSSP) 委派認證，您必須指定可委派給哪些伺服器。
ms.assetid: 15ed9a62-2eee-4f29-92c5-ccf2754cdf13
title: CredSSP 群組原則設定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a159b7a162df3eda692462a3d3972159e61797e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987634"
---
# <a name="credssp-group-policy-settings"></a>CredSSP 群組原則設定

若要讓 [認證安全性支援提供者通訊協定 (CredSSP) ](credential-security-support-provider.md) 委派認證，您必須指定可委派給哪些伺服器。 若要指定這些伺服器，請修改群組原則編輯器中的設定 (GPE) Microsoft Management Console (MMC) 嵌入式管理單元。 控制委派的 GPE 設定位於 [電腦設定] 底下， **\| 系統管理範本 \| 系統 \| 認證委派**。

> [!Caution]  
> 這不是限制委派。 CredSSP 會將使用者的完整認證傳遞給沒有任何條件約束的伺服器。

 

群組原則設定會控制下列認證類型的委派。



| 認證類型                                                                                                                                 | Description                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="Default_credentials"></span><span id="default_credentials"></span><span id="DEFAULT_CREDENTIALS"></span>預設認證<br/> | 使用者第一次登入 Windows 時所取得的認證。<br/>                   |
| <span id="Fresh_credentials"></span><span id="fresh_credentials"></span><span id="FRESH_CREDENTIALS"></span>新認證<br/>         | 當使用者執行應用程式時，系統會提示使用者輸入認證。<br/>       |
| <span id="Saved_credentials"></span><span id="saved_credentials"></span><span id="SAVED_CREDENTIALS"></span>儲存的認證<br/>         | 使用 [認證管理員](credential-manager.md)儲存的認證。<br/> |



 

若要在與特定群組原則設定相關聯的類別中包含伺服器，請將該伺服器的 [*服務主體名稱*](/windows/desktop/SecGloss/s-gly) (SPN) 新增至該群組原則設定的伺服器清單。 SPN 可以包含單一萬用字元。

 

