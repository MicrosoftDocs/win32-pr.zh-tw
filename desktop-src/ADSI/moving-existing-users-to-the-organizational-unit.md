---
title: 將現有的使用者移至組織單位
description: 當企業系統管理員（Joe Worden）將 Windows NT 4.0 網域升級為 Active Directory 時，所有使用者和群組都會遷移至 Fabrikam 網域中的 [使用者] 容器。
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- 將現有的使用者移至組織單位的 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104182986"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a>將現有的使用者移至組織單位

當企業系統管理員（Joe Worden）將 Windows NT 4.0 網域升級為 Active Directory 時，所有使用者和群組都會遷移至 Fabrikam 網域中的 [使用者] 容器。 Joe 現在可以將這些使用者和群組移至適當的組織單位。 您也可以使用 ADSI 在相關的 Windows 2000 網域之間移動物件。

在下列程式碼範例中，Joe 會將 "jeffsmith" 移至銷售組織。


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



[**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere)方法會取得要移動之物件的 ADsPath，而新的物件名稱 (RDN) 。 若要保留相同的名稱，您可以為 *bstrNewName* 參數指定 **Null** (**vbNullString**) 。 若要在移動時重新命名物件，請為 *bstrNewName* 參數指定新的相對分辨名稱。 例如，若要將 jeffsmith 移至銷售組織，並在相同的作業中將 "jeffsmith" 物件重新命名為 "jeff \_ smith"，Joe 會執行下列程式碼：


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[在組織單位中建立新的使用者](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




