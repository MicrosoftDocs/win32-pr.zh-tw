---
description: 您可以定義應用程式所需的安全性許可權，以判斷該應用程式的安全性原則。
ms.assetid: 0348684f-aebd-4d2d-a69b-85fea551c0cd
title: 定義應用程式的角色
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f8e46eb2cb857a2b2dee2aabe41cb571e12ed98
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991632"
---
# <a name="defining-roles-for-an-application"></a>定義應用程式的角色

您可以定義應用程式所需的安全性許可權，以判斷該應用程式的安全性原則。 若要這樣做，請將特殊許可權的符號層級宣告為角色，也就是定義應用程式的角色，然後 [將角色指派](assigning-roles-to-components--interfaces--or-methods.md) 給應用程式內的特定資源。 這項設計是在部署應用程式時完成的，而系統管理員則會將實際的使用者和使用者群組填入角色。 如需更詳細的資訊，請參閱以 [角色為基礎的安全性管理](role-based-security-administration.md)。

**將角色加入至應用程式**

1.  在 [元件服務] 系統管理工具的主控台樹中，找出您要新增角色的 COM + 應用程式。 展開樹狀結構，以查看應用程式的資料夾。

2.  以滑鼠右鍵按一下應用程式的 [ **角色** ] 資料夾，指向 [ **新增**]，然後按一下 [ **角色**]。

3.  在 [ **角色**] 對話方塊中，于提供的方塊中輸入新角色的名稱。

4.  按一下 [確定]  。

> [!Note]  
> 將角色新增至應用程式之後，您必須確定將角色指派給適當的元件、介面和方法。 否則，如果已選擇並啟用以角色為基礎的安全性，而且已新增但未指派角色，則對應用程式的所有呼叫都會失敗。 如需詳細資訊，請參閱 [將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md)
</dt> <dt>

[在元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[設定存取檢查的安全性等級](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



