---
title: 列舉物件
description: 若要查看容器的子物件（例如組織單位） (OU) ，請列舉容器物件。
ms.assetid: 06995281-d269-42ce-839f-2938a2f6af22
ms.tgt_platform: multiple
keywords:
- 列舉物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c26b78f084f95ac59c909b326be10d42c4a6696a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839204"
---
# <a name="enumerating-objects"></a>列舉物件

若要查看容器的子物件（例如組織單位） (OU) ，請列舉容器物件。 為了與檔案系統相類似，子物件會對應至目錄中的檔案，而容器（父物件）會對應至目錄本身。 當您想要取得物件的父物件時，也可以使用列舉作業。

當您列舉物件時，實際上會系結至目錄中的物件，並在每個物件上傳回 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面。

下列程式碼範例顯示如何列舉容器的子系。


```VB
Dim ou As IADs
' Bind to an object using its DN.
On Error GoTo Cleanup

Set ou = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=COM")

For each child in ou
    Debug.Print child.Name
Next

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set ou = Nothing
```



您可以篩選從列舉傳回的物件類型。 例如，若只要顯示使用者和群組，請在列舉之前使用下列程式碼範例。


```VB
Ou.Filter = Array("user", "group")
```



如果您有物件參考，則可以使用 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) [**父**](iads-property-methods.md) 屬性取得物件的父系。 下列程式碼範例顯示如何系結至父物件。


```VB
parentPath = obj.Parent
Set parent = GetObject(parentPath)
```



如需詳細資訊，請參閱 [列舉 ADSI 物件](enumerating-adsi-objects.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[搜尋物件](searching-for-objects.md)
</dt> </dl>

 

 




