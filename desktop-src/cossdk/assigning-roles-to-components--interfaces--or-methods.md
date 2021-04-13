---
description: 將角色指派給元件、介面或方法
ms.assetid: 687d5692-4a83-4de8-b99d-859aaaddd16d
title: 將角色指派給元件、介面或方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5efb66c9de865cbfcdc6e9cb047af92c95f6bc0a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104385966"
---
# <a name="assigning-roles-to-components-interfaces-or-methods"></a>將角色指派給元件、介面或方法

您可以透過 [元件服務] 系統管理工具，將角色明確指派給 COM + 應用程式中可看見的任何專案。 這麼做可確保屬於該角色成員的任何使用者都可以存取該專案及其包含的任何其他專案。 例如，如果您將「讀取者」角色指派給某個元件，「讀取器」的任何成員都可以存取該元件，以及它所公開的任何介面和方法。 「讀取器」會顯示為任何這些介面和方法的繼承角色。

只有當您將角色指派給呼叫端，或是將角色指派給方法的介面或方法的元件時，呼叫端才可以存取方法，在此情況下，此方法會繼承角色。 如果未指派任何角色，而且已啟用存取檢查，則對方法的所有呼叫都將會失敗。

您必須先為應用程式 [定義](defining-roles-for-an-application.md) 角色，才能指派角色。 針對應用程式定義的所有角色，都會出現在應用程式內任何元件、方法和介面的 [**安全性**] 索引標籤上，針對 **選取的專案 (s 明確設定的角色)** 視窗中。

**將角色指派給元件、方法或介面**

1.  在 [元件服務] 系統管理工具的主控台樹中，找出已定義角色的 COM + 應用程式。 展開樹狀結構，以根據您指派角色的目標來查看應用程式的元件、介面或方法。

2.  以滑鼠右鍵按一下您要指派角色的專案，然後按一下 [ **屬性**]。

3.  在 [屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

4.  在 [ **為選取的專案明確設定的角色 (s)** ] 方塊中，選取您要指派給專案的角色。

5.  按一下 [確定]  。

任何您已為專案明確設定的角色，都會由它所包含的任何較低層級專案繼承，並顯示在這些專案 **(s) 視窗中所選取專案繼承的角色** 中。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[定義應用程式的角色](defining-roles-for-an-application.md)
</dt> <dt>

[啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md)
</dt> <dt>

[在元件層級啟用存取檢查](enabling-access-checks-at-the-component-level.md)
</dt> <dt>

[設定存取檢查的安全性等級](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



