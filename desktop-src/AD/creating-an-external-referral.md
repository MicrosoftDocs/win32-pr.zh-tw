---
title: 建立外部參考
description: 如果已建立外部交叉參考物件，且網域控制站使用它來產生參考，則交叉參考物件會在下列屬性中提供兩個重要的資料元素。
ms.assetid: 9805390c-9e8d-4afd-bffc-43abf6055413
ms.tgt_platform: multiple
keywords:
- 外部參考 Active Directory
- Active Directory 範例 Active Directory，建立外部參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 801a9306c374a0c22d206e9a0f9dbb8cd240da0c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681680"
---
# <a name="creating-an-external-referral"></a>建立外部參考

如果已建立外部 [**交叉**](/windows/desktop/ADSchema/c-crossref) 參考物件，且網域控制站使用它來產生參考，則 **交叉** 參考物件會在下列屬性中提供兩個重要的資料元素。 如需可能發生這種情況的詳細資訊，請參閱上一節。



| 屬性                           | 描述                                                                                                                                                         |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | 指定伺服器或網域，該伺服器或網域可以提供 [**nCName**](/windows/desktop/ADSchema/a-ncname)中指定之命名內容的資料。                                           |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | 指定根于 [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)所指定的伺服器或網域之網域、架構或設定容器的分辨名稱。 |



 

例如，如果 DNS 位址為 serv1.northwest.Fabrikam.com 的伺服器提供根目錄為 CN = MyContainer，OU = MyDOM，O = Fabrikam 的命名內容，請將 [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) 設定為該伺服器的 DNS 位址，並將 [**nCName**](/windows/desktop/ADSchema/a-ncname) 設定為網域、架構或設定容器的分辨名稱。

如需詳細資訊和顯示如何建立外部參考的程式碼範例，請參閱 [建立外部交叉參考物件的範例程式碼](example-code-for-creating-an-external-crossref-object.md)。

 

 