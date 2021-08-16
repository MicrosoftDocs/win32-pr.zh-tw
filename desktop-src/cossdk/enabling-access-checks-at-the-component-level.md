---
description: 在元件層級啟用存取檢查
ms.assetid: b9ff5296-9076-4492-833c-7402b7090f8f
title: 在元件層級啟用存取檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3063873923d3d4c491312ca4efccd9bcd665b46bf1bdfc882b69dbe4942757f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047466"
---
# <a name="enabling-access-checks-at-the-component-level"></a>在元件層級啟用存取檢查

如果您的應用程式包含不需要安全性檢查的元件，您可能會決定停用該元件的角色檢查以改善效能。 或者，在進行調試時，停用安全性可能會很有説明，讓您可以專注于程式功能的其他層面。

依預設，當您安裝元件時，會啟用元件層級的存取檢查。 不過，只有在啟用 [應用層級的存取檢查](enabling-access-checks-for-an-application.md) ，以及當 [安全性層級](setting-a-security-level-for-access-checks.md) 設定為 **在進程和元件層級執行存取檢查** 時，才會生效。

**若要啟用或停用元件層級的存取檢查**

1.  在 [元件服務] 系統管理工具的主控台樹中，找出包含您要停用 (或啟用) 角色檢查之元件的 COM + 應用程式。 展開樹狀結構中的 [view]，以查看 [ **元件** ] 資料夾中的元件。

2.  以滑鼠右鍵按一下您要啟用角色檢查的元件，然後按一下 [ **屬性**]。

3.  在 [元件屬性] 對話方塊中，按一下 [ **安全性** ] 索引標籤。

4.  選取 [ **強制執行元件層級存取檢查** ] 以強制執行元件層級的檢查。

5.  按一下 [確定]。

新設定將會在應用程式下次啟動時生效。

> [!Note]  
> 從 Windows Server 2003 中，建立 com + 應用程式時，預設會停用元件層級的存取檢查。 預設會在應用層級啟用存取檢查，並且在元件層級預設為停用。 先前，在應用層級依預設會停用存取檢查，而且在元件層級預設為啟用。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[將角色指派給元件、介面或方法](assigning-roles-to-components--interfaces--or-methods.md)
</dt> <dt>

[設定 Role-Based 安全性](configuring-role-based-security.md)
</dt> <dt>

[定義應用程式的角色](defining-roles-for-an-application.md)
</dt> <dt>

[啟用應用程式的存取檢查](enabling-access-checks-for-an-application.md)
</dt> <dt>

[設定存取檢查的安全性等級](setting-a-security-level-for-access-checks.md)
</dt> </dl>

 

 



