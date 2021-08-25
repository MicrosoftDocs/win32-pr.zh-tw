---
description: 如果您的 COM + 應用程式使用以角色為基礎的安全性，則需要完成幾項工作。
ms.assetid: f53b9945-cd34-4afc-a03a-dd72b0af160d
title: 設定 Role-Based 安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aba7df6b11bf44b53adaa9776435e43eabe3188fccb789a01d996f45331298dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859058"
---
# <a name="configuring-role-based-security"></a>設定 Role-Based 安全性

如果您的 COM + 應用程式使用以角色為基礎的安全性，則需要完成幾項工作。 在您的應用程式中設計元件時，您會定義協助保護這些元件存取權所需的角色。 您也可以決定要將哪些角色指派給應用程式的元件、介面和方法。 在應用程式整合期間，您可以使用 [元件服務] 系統管理工具，將定義的角色加入至應用程式，並將每個角色指派給適當的元件、介面和方法。

在設定以角色為基礎的安全性時，您會執行下列步驟：

1.  在應用層級啟用存取檢查。 開啟應用程式的安全性檢查。 如需如何執行此步驟的詳細資訊，請參閱 [啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md) 。
2.  設定存取檢查的安全性層級。 在進程或進程和元件層級設定安全性。 如需如何執行此步驟的詳細資訊，請參閱 [設定存取檢查的安全性層級](setting-a-security-level-for-access-checks.md) 。
3.  在元件層級啟用存取檢查。 開啟元件、介面和方法層級的安全性檢查。 如需如何執行此步驟的詳細資訊，請參閱在 [元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md) 。
4.  定義應用程式的角色。 建立應用程式的角色。 如需如何執行此步驟的詳細資訊，請參閱 [定義應用程式的角色](defining-roles-for-an-application.md) 。
5.  將角色指派給元件、介面或方法。 將角色指派給應用程式內的特定資源。 如需如何執行此步驟的詳細資訊，請參閱 [將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定軟體限制原則](configuring-the-software-restriction-policy.md)
</dt> <dt>

[設定模擬等級](setting-an-impersonation-level.md)
</dt> </dl>

 

 



