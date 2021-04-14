---
title: 群組函式
description: 全域群組包含一個網域中的使用者帳戶，這些使用者帳戶會群組在一個群組帳戶名稱下。
ms.assetid: 2199258d-bde9-4fdb-b9c1-147616420fbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7696755cd5f5cbe75de11d386cb238fa3bd5d35d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382509"
---
# <a name="group-functions"></a>群組函式

*全域群組* 包含一個網域中的使用者帳戶，這些使用者帳戶會群組在一個群組帳戶名稱下。 全域群組只能包含成員 (從建立全域群組的網域) 的使用者;它不能包含本機群組。 全域群組可在自己的網域中，也可以在任何信任網域內使用。

網路管理群組功能會控制全域群組。 群組函數如下所示。



| 函式                                     | 描述                                                                       |
|----------------------------------------------|-----------------------------------------------------------------------------------|
| [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd)           | 建立全域群組。                                                           |
| [**NetGroupAddUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadduser)   | 將一位使用者新增至現有的全域群組。                                        |
| [**NetGroupDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdel)           | 移除群組是否有任何成員的全域群組。                  |
| [**NetGroupDelUser**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupdeluser)   | 從全域群組移除一個使用者名稱。                                        |
| [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)         | 列出伺服器上的所有全域群組。                                              |
| [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)   | 傳回特定全域群組的相關資訊。                              |
| [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers) | 列出特定全域群組的所有成員。                                   |
| [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo)   | 設定全域群組的一般資訊。                                    |
| [**NetGroupSetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetusers) | 指派成員給新的全域群組;取代現有群組的成員。 |



 

When you call the [**NetGroupAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupadd) function to create a global group, you must supply a group name. 一開始，新的群組沒有任何成員。

使用者帳戶會自動隸屬于特殊的全域群組網域使用者。 此群組中的成員資格是由 [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)、 [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)和 [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) 函數間接控制。

通用群組帳戶資訊可在下列層級取得：

-   [**群組 \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_0)
-   [**群組 \_ 資訊 \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1)
-   [**群組 \_ 資訊 \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_2)
-   [**群組 \_ 資訊 \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_3)
-   [**群組 \_ 資訊 \_ 1002**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1002)
-   [**群組 \_ 資訊 \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_info_1005)

1002和1005層級僅適用于 [**NetGroupSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupsetinfo) 函數。

全域群組成員資訊可在下列資訊層級取得：

-   [**群組 \_ 使用者 \_ 資訊 \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-group_users_info_0)

如需詳細資訊，請參閱網路管理 [本機群組功能](local-group-functions.md)。

如果您正在針對 Active Directory 進行程式設計，您可以呼叫特定 Active Directory 服務介面 (ADSI) 方法，以取得您可以藉由呼叫網路管理群組功能達成的相同功能。 如需詳細資訊，請參閱 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup)。

 

 