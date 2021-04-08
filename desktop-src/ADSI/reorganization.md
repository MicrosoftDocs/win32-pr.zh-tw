---
title: 重組
description: 銷售組織已移至新的組織 \ 8212;\ 0034;銷售與支援。 \ 0034;Julie Bankert 已升階至副總裁，將帶領新的組織。
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- 重新組織 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020793"
---
# <a name="reorganization"></a>重組

銷售組織已移至新的組織-「銷售和支援」。 Julie Bankert 已升階至副總裁，將帶領新的組織。 Joe Worden 是企業系統管理員，必須將 Sales OU 移至新的 OU、銷售和支援人員。


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



使用此程式碼範例，銷售組織單位中的所有物件（包括子組織單位）都會移至新的組織單位。

現在，Joe 可將 Julie 移至銷售和支援組織單位。


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



請注意，Active Directory 會自動更新 Julie Bankert 和 Chris 灰色之間的經理直接報告連結。

**若要建立 Active Directory 報表**

1.  開啟 Visual Basic 版本6.0，當系統提示您輸入專案類型時，請選取 [ **資料項目目**]。
2.  在 [ **資料項目目**] 上，按兩下 [ **資料 Environment1**]。
3.  在 [ **資料環境** ] 視窗中，以滑鼠右鍵按一下連線物件 **(connection1.txt)** 然後選取 [ **屬性**]。
4.  選取 [ **Microsoft 目錄服務 OLE DB 提供者**]，然後按一下 **[下一步]**。
5.  選取 [ **使用 Windows NT 整合式安全性**]，然後按一下 **[確定]**。 這會建立連線物件。
6.  再以滑鼠右鍵按一下 [ **資料環境** ] 視窗，選取 [ **加入命令**]。 以滑鼠右鍵按一下 [ **Command1** ] 物件，然後選取 [ **屬性**]。 [下列 **Command1 屬性** ] 對話方塊隨即出現。

    ![command1 屬性對話方塊](images/adadsi3.png)

7.  按一下 [ **SQL 語句** ] 選項按鈕，然後輸入下列內容：

    SELECT Name，telephoneNumber FROM ' LDAP：//DC = Fabrikam，DC = com ' WHERE objectCategory = ' Person ' AND objectClass = ' user '

    會建立 **命令** 物件。 將 **命令** 物件加入至報表。

8.  按兩下 [**專案**] 視窗中的 [**資料 report1.rdl** ]。
9.  將 **Command1** 物件從 [ **DataEnvironment1** ] 視窗拖曳到 [**資料包表**] 視窗中的 [**詳細** 資料] 區段。
10. 在 [ **DataReport1 屬性**] 的 [**資料來源**] 中，從下拉式功能表中選取 [ **DataEnvironment1** ]，然後在 [ **DataMember** ] 欄位中選取 [ **Command1** ]。
11. 在 [專案] 視窗中，以滑鼠右鍵按一下 [ **資料項目目**]，然後選取 [ **DataProject 屬性**]。
12. 在 [ **DataProject 專案屬性** ] 對話方塊視窗的 [ **啟始物件**] 下，從下拉式功能表中選取 [ **DataReport1** ]。 按一下 [確定]  以儲存。
13. 編譯。 將會出現下列 [ **DataReport1** ] 對話方塊。

    ![datareport1 對話方塊](images/adadsi4.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[聯結異質資料](joining-heterogeneous-data.md)
</dt> </dl>

 

 




