---
title: 將主機電腦上的 [以服務方式登入] 許可權授與許可權
description: 當安裝服務在網域使用者帳戶下執行時，帳戶必須擁有在本機電腦上以服務方式登入的許可權。
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef53e68feb9312bb8efdca285716aa5b6ea077e2e85f6c5538eb13532b51a8ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188952"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a>將主機電腦上的 [以服務方式登入] 許可權授與許可權

當安裝服務在網域使用者帳戶下執行時，帳戶必須擁有在本機電腦上以服務方式登入的許可權。 請注意，此登入許可權僅適用于本機電腦，必須在每部主機電腦的本機 LSA 原則中授與。 如果您的服務是以 LocalSystem 的身分執行（依預設會授與此許可權），則不需要執行此步驟。

如需如何以程式設計方式授與登入服務許可權的詳細資訊，請參閱 [LSAPrivs 範例程式碼](https://www.google.com/#q=LSAPrivs)。

 

 




