---
description: 建立網路提供者或認證管理員之後，您必須向系統註冊。
ms.assetid: 4c58671d-d11d-4f32-866b-e278fc8e6114
title: 註冊網路提供者和認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec3b3eff5fc396a112986d8c736dba095701a02ffb9e72c21422b83e3596235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118919586"
---
# <a name="registering-network-providers-and-credential-managers"></a>註冊網路提供者和認證管理員

建立網路提供者或認證管理員之後，您必須向系統註冊。 這是必要的，因此 MPR 會知道安裝了哪些網路提供者。 當 MPR 啟動時，它會檢查登錄，並載入其找到的任何網路提供者或認證管理員。

由於網路提供者和認證管理員是相關的，因此它們會在登錄的相同子機碼中進行註冊。 事實上，網路提供者 Dll 也可以是認證管理員。

如需有關您應該為網路提供者或認證管理員建立之登錄機碼的詳細資訊，請參閱驗證登錄機 [碼](authentication-registry-keys.md)。

 

 



